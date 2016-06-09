# How to Make Groovy as Fast as Java 

2016 年 6 月 5 日

> original at (link)[https://www.linkedin.com/pulse/how-make-groovy-fast-java-david-e-jones]

## Introduction

As an optionally typed JVM based language Groovy offers syntax and construct features that make development more efficient for a wide variety of tools and applications. The downside to Groovy is the runtime overhead for type checking and conversions, and certain other Groovy magic. For lower level or frequently run code in certain cases it is best to write in plain Java but for most code Groovy has options to make your code run just as fast as Java.

The tips in this article are based on my experience writing and optimizing Moqui Framework which currently has around 40k lines of Groovy code. In plain Java the code would easily be double or triple the size, and generally far more complex as well. Moqui was originally written in 100% Groovy aside from the framework API which is mostly interfaces and is written in Java. There are huge benefits to using Groovy for a framework like Moqui as there is a lot of complex functionality to implement and Groovy helps the code stay simple and small. This makes the framework more flexible and easier to write, improve, and maintain. With the limited resources of an unfunded open source project these are critical factors, but apply even to large teams working with much larger codebases.

The downside to this? The early releases of Moqui Framework were SLOW. Simple lower level operations like database finds ran (on my laptop) at around 8,000 per second and updates at around 3,000 per second. That was after some profiling and optimization. These were on an embedded database, so there was no network or serialization overhead involved (useful for better seeing the framework overhead). From profiling I could see a lot of time was spent in Groovy classes doing things like type checking and conversions, even when it was not needed.

It was fine for development and running lower traffic applications, and with an architecture designed to run across multiple application servers more hardware could be added to compensate, but the cost of hardware scaling is high both in terms of hardware related costs and in terms of application overhead to coordinate between larger numbers of servers.

The current Moqui Framework code, again running on my laptop, can do around 200,000 database find operations per second and around 50,000 updates per second. The before and after numbers are from test runs after running a number of times so the JVM just in time compilation and so on have done their thing. Other framework tools are also much faster (around an order of magnitude), including service calls and screen rendering.

Note that this article is based on Groovy version 2.4.6\. Things may change in future versions of Groovy, but the more general tips and techniques will still apply.

## Tools

The main tools you'll need are:

1\. A Groovy-aware IDE: I use IntelliJ IDEA from Jetbrains and it has very good Groovy support including inspectors for a wide variety of Groovy-specific issues. While optimizations can be done with a plain text editor, or one with just syntax highlighting, making some bigger changes can take a LOT of time without these inspectors. When applying certain changes (like @CompileStatic, see more below), various other code changes need to be made before your code will even compile and doing this with a simple text editor involves excessive change/build cycles.

2\. A Java Profiler: I use JProfiler from EJ Technologies. There are many good Java profilers out there, you just need something that will tell you how long each method takes to run and allows you to include/exclude classes and packages based on what you care about. For optimizing Groovy code you'll need to include measuring various Groovy classes (some mentioned below) so you can track the overhead of using Groovy versus Java.

3\. A Java Decompiler: I use JD-GUI (https://github.com/java-decompiler/jd-gui). While IDEA has a built-in decompiler for many methods it is not able to fully decompile, so you need something that lets you look at annotated bytecode as well. The reason for this is the profiler will tell you when a method is calling Groovy type checking, conversion, etc methods a lot, but it won't tell you where in the method these are called. Until you know what Groovy does really well you won't be able to tell by just looking at your code. In some cases it is surprising when Groovy finds the need to do type conversion, such as assigning a null value.

## Step 1: Write Test Cases and Profile

The test cases I use are simply code that loops hundreds or thousands of times to isolate specific operations from other overhead. These need to be manually triggered (in my case through a web page) so that you can run them, look at timing details, and rerun them as needed. Before profiling you'll want to run them a few times, until the JIT compiler does its thing and the run times become consistent. Once your running application is in that state you can attach the profiler, run a few times more (again until the run times become consistent), and only then turn on CPU measuring in the profiler and run them to collect time data.

If you start your application, attach the profiler, and just run your tests once you'll get inconsistent numbers from the profiler and you won't be simulating how your code actually runs in production.

The main goal of the first pass is to have test cases for the most important parts of your code, and get an idea of what is taking the most time to run. Most profilers show hot spots to help narrow this down. These are the first to focus on when optimizing. Another thing to look at is the call tree and how long important or time sensitive code takes to run.

This requires a good knowledge of your codebase, what it does and how. Getting information from the profiler about what is slow often comes down to a sort of smell test, identifying code that takes a long time to run and either doesn't do anything specific or just shouldn't take so much time.

What to watch for depends a lot on what your code does and how. In framework development, and often in lower level tool code, one big things to watch for is checking configuration options and other data that determines code paths to run. Your code needs to be able to get to this data and check it quickly so that options and features don't make your code so slow that when speed is needed users end up find another option.

## Step 2: Use @CompileStatic

While Groovy has performance options that allow you to keep your code dynamically typed I never had good results with them. For Moqui Framework using the Indy compiler and runtime (for Java invokedynamic) actually made it significantly slower!

The best option for code that needs to run fast is the @CompileStatic annotation. When you apply this annotation you can't use Groovy features that depend on dynamic typing, but fortunately most of the more useful features still work just fine.

You will need to declare types, and subtypes for generics, just as you do in plain Java. You will also need to do explicit type conversions and casting in some cases. Type casting is the fastest while using the Groovy 'as' operator is the most convenient. Depending on how much a particular code block is run you may put more or less effort into handling types. When you really care about performance use type casting and make sure Groovy isn't doing any dynamic type checking or conversion. If it is making a difference you'll see it happening in the profiler, and you can pin down exactly where using a decompiler.

The @CompileStatic annotation can be added to individual methods as well as to entire classes. In my first pass using @CompileStatic I applied it only to methods that (based on profiling) were called a large number of times in my test cases. This is convenient for large classes that use Groovy features that don't work with @CompileStatic and need to all be changed, but there are certain cases where using it on selected methods doesn't work. The main place I found problems was with constructors. You'll see these quickly with odd runtime errors that I never found a way to fix other than pulling code out of the constructor into separate methods with @CompileStatic, or using the @CompileStatic annotation on the entire class (which has other benefits as well).

Eventually I went with the approach of mostly annotating classes with @CompileStatic and updating the entire class as needed to work with it.

## Step 3: Thorough Profiling and Optimization

Before applying the @CompileStatic annotation you may have so much Groovy overhead that it is difficult to find other code that can be optimized. With really low level code the Groovy dynamic typing overhead may be so significant that other optimizations make very little difference.

Now that you have @CompileStatic applied to the most important classes and methods you can really get into profiling and optimizing your code, and you have more in place to make changes that really make a difference.

One thing to watch for is iteration. In general code in iteration blocks is code that will run a higher number of times, especially with nested iteration (which may be in separate methods, etc). For code blocks that are run a high number of times that do iteration the overhead of iteration itself is something to keep an eye on. If your profiling results show a lot of time spent creating iterators and calling hasNext()/next() then you may be able to dramatically improve performance by using an array or ArrayList. This saves on the cost of creating the iterator and on repeatedly calling hasNext() by using a simple integer compare instead. When the code inside the iteration block is fairly simple this makes a huge different, you might see a code block run tens of times faster.

Another thing to watch for is method calls. Method calls are pretty fast in Java, but in low level frequently run code the overhead of method calls is significant. The two main places you'll run into this overhead is highly nested method calls from code that is overly structured or runs through too many generic interfaces when doing simple things, and very low level code that needs data and gets it through getter methods. In many cases getter methods are a good practice, but for low level code that uses internal data (like configuration data) these are often private classes so making member fields private just isn't helpful and there is no issue with accessing member fields directly to save the method call overhead. Note that to do this you'll need to make sure Groovy isn't using an automatic getter method! In some cases I even use simple objects written in Java to hold configuration and other data that is frequently used.

Whether writing in Groovy or Java another thing to watch for is classes that wrap primitive types (int/Integer, boolean/Boolean, etc) and the cost of boxing and unboxing. In most code this won't matter, but in low level code you'll see the overhead of method calls to get simple values or construct wrapper objects and these can have significant overhead that you might be able to avoid by just using primitive types.

## Step 4: Groovy Specific Optimization

While reviewing your profiler results you may see various Groovy methods calls among your hot spots. Here is a summary of some common Groovy methods and what you can do about them.

To see these in your profiling results make sure these Groovy packages and classes are not filtered out:

*   org.codehaus.groovy.runtime.ScriptBytecodeAdapter
*   org.codehaus.groovy.runtime.typehandling.DefaultTypeTransformation
*   org.codehaus.groovy.reflection.ClassInfo

### ScriptBytecodeAdapter.castToType()

Groovy calls the castToType() method any time it does not know the type of a value, or the type it determines is Object and you are assigning it to a field with a particular type. When using @CompileStatic this is minimized, but still happens even when it seems like Groovy should be able to determine the type at compile time. Avoiding these calls basically requires explicit type casting even in cases where you wouldn't have to in Java. You don't have to in Groovy, but to avoid the overhead of a castToType() call you must.

This is where a decompiler is most useful. You can see these methods called in the profiler, but finding where they are called by looking at your code is often not obvious, and sometimes surprising.

One such case is when assigning a null value. For example this results in a call to castToType():

**    String myString = null**

To avoid that you need to cast the null, and then will be no call to castToType():

**    String myString = (String) null**  

Another case is when getting a value from a Map or Collection such as an ArrayList. What is surprising is that this happens in Groovy even when generics and subtypes are used. The last two statements in this code result in calls to castToType:

**    Map<String, String> myMap = new HashMap<>()**  
**    ArrayList<String> myList = new ArrayList<>()**  
**    String mapValue = myMap.get("foo")**  
**    String listValue = myList.get(0)**  

With an explicit type cast Groovy no longer calls castToType():

**    String mapValue = (String) myMap.get("foo")**  
**    String listValue = (String) myList.get(0)**

Right now this seems to be the best way to handle it. It is non-intuitive and slightly cumbersome, but overall easy. The tricky part is tracking down where these happen. Hopefully this tip about improving performance will be unnecessary in some future version of Groovy, but for now it is part of how it works.

When you decompile and end up with bytecode instead of decompiled Java code here an example of what it looks like when you have a call to castToType() as part of a null assignment:

_    // 12: aconst_null_  
_    // 13: ldc_w 1717_  
_    // 16: invoke static 143 org/codehaus/groovy/runtime/ScriptBytecodeAdapter:castToType (Ljava/lang/Object;Ljava/lang/Class;)Ljava/lang/Object;_  
_    // 19: checkcast 1717 org/moqui/impl/entity/condition/EntityConditionImplBase_

Notice that you don't get many clues about the statement in question other than context, looking before and after for references, but you do at least get the type that Java expects and if you cast to that type the call to castToType() goes away (the Groovy static compiler doesn't generate it).

The castToType() method is also used when you explicitly cast from Object or some other class to a more specific class and the Groovy static compiler determines the original class to be something else. In these cases doing some other manual conversion is not likely be faster. Groovy does not support the approach in Java of doing an unchecked type cast. In Java you get a warning about this but can suppress it. In Groovy it always calls castToType() to check the type at runtime (a bit redundant with Java's default 'checkcast' bytecode).

### Math and ScriptBytecodeAdapter.asType()

The asType() method is used to coerce a value to a particular object type, and may result in type conversion. Without @CompileStatic this gets called a lot and is a common profiling hot spot. With @CompileStatic this is mostly used when using the 'as' operator.

To show an example of something that seems simple but in Groovy becomes complex consider these two statements (as an example):

**    long startTimeNanos = System.nanoTime()**  
**    long startTime = startTimeNanos/1000000L as long**  

First off it seems funny that the 'as long' is even needed. Without it when you compile you'll get an error like "[Static type checking] - Cannot assign value of type java.math.BigDecimal to variable of type long". In Groovy all math is done with BigDecimal unless one operand is a float or double. For business applications this is very convenient and results are more consistent and reliable than with floating point math. When trying to do simple primitive type based calculations like this it is a pain! The simple solution is to tell Groovy you want the result as a long. For convenience this is fine, for performance it is amazing the hurdles goes through to make this happen.

Here is an example of bytecode decompilation from JD-GUI for the second statements:

_    // 7: invokestatic 1341 java/lang/Long:valueOf (J)Ljava/lang/Long;_  
_    // 10: getstatic 1343 org/moqui/impl/entity/EntityValueBase:$const$0 Ljava/math/BigDecimal;_  
_    // 13: invokestatic 1348 org/codehaus/groovy/runtime/dgmimpl/NumberNumberDiv:div (Ljava/lang/Number;Ljava/lang/Number;)Ljava/lang/Number;_  
_    // 16: getstatic 1349 java/lang/Long:TYPE Ljava/lang/Class;_  
_    // 19: invokestatic 517 org/codehaus/groovy/runtime/ScriptBytecodeAdapter:asType (Ljava/lang/Object;Ljava/lang/Class;)Ljava/lang/Object;_  
_    // 22: invokestatic 1353 org/codehaus/groovy/runtime/typehandling/DefaultTypeTransformation:longUnbox (Ljava/lang/Object;)J_

Here we've got a call to Long.value() to box the primitive long, NumberNumberDiv.div() on a Groovy class to do the division, then the call to asType() using the Long.class type to convert the type and round it, and then a longUnbox() to get back to the primitive.

The solution? Change the code to do a double operation, which Groovy will do native, and then call Math.round() to get the long value back:

**    long startTime = Math.round(startTimeNanos/1000000.0D)**

The bytecode coming out of the Groovy compiler is now MUCH cleaner:

_    // 7: l2d_  
_    // 8: ldc2_w 1338_  
_    // 11: ddiv_  
_    // 12: invokestatic 1345 java/lang/Math:round (D)J_

Now we just have native bytecode calls including ddiv for the double division and a single method call to Math.round(). The performance difference is huge.

This example covers much more than just the asType() call and demonstrates how to make math operations more efficient (using the float and double math trick). More generally for avoiding asType() calls find alternatives to using the 'as' operator and watch for other things in the profiler and decompiler that result in it.

### DefaultTypeTransformation.booleanUnbox()

This is the method called when you have an expression that is used as a boolean but the data type of the result of the expression is not a boolean. This is a very handy feature in Groovy, coercion to a boolean, but has a performance penalty that can be avoided in low-level code. Usually this is in an 'if' or similar expression such as this code where the if is equivalent to (myString != null && myString.length() > 0):

**    String myString = ...**  
**    if (myString) { ... }**  

These can be changed to a compare to null and if necessary a check if empty (using size(), length(), etc method). Doing so is a fair amount faster than the call to booleanUnbox(), and a lot faster if you are just doing a null check.

### ClassInfo.getMetaClass() and $getStaticMetaClass()

All classes implemented with Groovy have a meta class that Groovy uses at runtime. This is necessary for certain Groovy features, but is in place and retrieved at runtime even if you don't use those language features.

You'll generally see these as hot spots in your profiling for classes written in Groovy that are constructed a large number of times. For classes with otherwise simple initialization these represent a lot of overhead. The only way to avoid them seems to be not using Groovy and instead to move these specific classes to plain Java. For some classes this is easily done and worth doing, for more complex classes the value of writing in Groovy may outweigh this performance overhead so it is simply something to be aware of and accept.

There are proposals and requests in the Groovy mailing lists about options to disable this, and a mechanism to disable it per class would be ideal.

## Conclusion

Groovy has many advantages over plain Java and for those already familiar with Java it is easy to progressively learn. The main benefits of Groovy come down to efficiency and convenience for developers, usually at the cost of runtime performance. With a bit of knowledge and effort that doesn't have to be the case. Groovy code can run as fast as Java code.

This begs the question: does the extra effort of optimizing Groovy code cancel out the development efficiency it offers? From my experience the answer is a clear no, Groovy is still far more efficient. Even writing in plain Java profiling and optimization is very important, there are just a few twists to doing it with Groovy and a few simple extra things to watch for. Most of what you will do profiling code written in Groovy is the same as what you would do with plain Java code. In general it is best to write first to get things working, then profile and optimize rather than trying to optimize as you go. Groovy fits in well with this practice as the initial development takes far less time. As a generality in the time you write and optimize Groovy code you would have barely finished writing plain Java code and still have to do optimization. Add in the greater effort for maintaining Java code over time and Groovy is even more clearly a better choice.

This article is mostly meant for those working on lower level code. For those who focus on applications and want to largely avoid all of this trouble, take a look at Moqui Framework (http://www.moqui.org). Moqui is a modern framework for fast, scalable enterprise applications that introduces more efficient practices for developers and addresses more than just the persistence and web tiers of a typical framework with a strong service oriented logic layer and native integrations with a wide variety of tools.

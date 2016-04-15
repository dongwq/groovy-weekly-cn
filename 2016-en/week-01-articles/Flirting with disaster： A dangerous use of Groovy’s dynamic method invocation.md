
## Flirting with disaster: A dangerous use of Groovy’s dynamic method invocation


I learned something interesting about about Groovy recently.I was tasked with building a tool for advanced admin users,to provide them an easy way to run batch jobs.It was designed so that users could point their browser at either `/service/algorithm1` or /`service/algorithm2`.The request is handled by a controller,written in Groovy,which simply verifies that the parameter is either “`algorithm1`” or “`algorithm2`”.If that condition is met,the controller simply delegates to a service-layer class to actually process the request. The Strings “`algorithm1`” and “`algorithm2`” also happen to be the names of methods provided by the service class.So,in an attempt to be clever and avoid a bunch of conditional statements,I thought it’d be cool to implement the controller logic like this:    


	if (param in [‘algorithm1’, ‘algorithm2’]) {
	   service.”${param}”()
	}
 

How slick is that?!I was tempted to take the rest of the day off after coming up with that beauty.I was feeling pretty,pretty proud of myself.I submitted a pull request and waited for the code-review kudos to come rolling in.And the approvals did come,except from one guy on the team who was not as big a fan of Groovy as I am.He was concerned that the line `service.”${param}”()` amounted to a security hole.He worried that someone could invoke arbitrary code by exploiting that line of code.Instead of my beautiful “dynamic” code,he preferred something like:    

	if (param == ‘algorithm1’) {
	    service.algorithm1()
	} else if (param == ‘algorithm2’) {
	    service.algorithm2()
	} else {  /* throw an error */ }
	 

Boring!Now,this teammate is a smart guy whose opinion I respect,so I was a bit troubled by his suggestion.My initial,almost visceral,reaction was to dismiss his concern as fear-of-the-unfamiliar (since he once said he was not very familiar with Groovy).I tried to assuage his concern.My reasoning went something like this:    

1) The expression `${param}` would have to evaluate to a `String` whose value matches the name of a method of the service class.It couldn’t cause arbitrary code to be executed – only a method of the service class could be invoked.    
2) Besides,it’s guarded with the `if param in ['algorithm1', 'algorithm2']` clause.Chill, brah!    

Ultimately,I figured,his suggestion/concern was just a code-style preference.But I wasn’t quite comfortable with my shallow argument-from-arrogance.I decided to fire up the Groovy console to test my claims.It’s a good thing I did,because they were not correct!While my implementation did guard against proceeding when the param value is anything other than “algorithm1” or “algorithm2”,my first argument was dead wrong.  Let’s look at an example:    

	class Greeting {
	  void sayHello() {
	    println "Hello"
	  }
	  
	  void sayGoodbye() {
	    println "Goodbye"
	  }
	}

	def greeting = new Greeting()

Here we just create a class with two simple methods and then create an instance of that class.   

Now let’s see if we can execute arbitrary code using the dynamic method invocation technique.First,let’s create a `GString` that contains arbitrary Groovy code but that should ultimately resolve to the `String` “`sayHello`”:    

	def param = "${ new File('/Users/me/Documents/Financial').eachFile { file -> println('Sending this file to malicious server: ' + file.name) }; 'sayHello' }"
 

Great, now let’s see what happens when we try to execute it:    

	greeting."${param}"()
 

Whoa, it works!My teammate was right,I was wrong,I’ll take my crow breaded and fried,please.Go ahead,fire up `groovyConsole` and try it for yourself.You’ll want to change the `/Users/me/Documents/Financial` bit to a directory path on your system.You should see that for each file in the specified directory,the message `Sending this file to malicious server: <fileName>` is printed out.Finally,the `greeting.sayHello()` method is invoked.    

While my initial implementation guarded against this kind of attack with the `if param in ['algorithm1', 'algorithm2']` condition,I decided to use the approach suggested by my teammate instead.It’s conceivable that some unsuspecting developer may come in later and remove that guard or change it to something like   

	if(param.contains('sayHello')) {
	 greeting."${param}"()
	} 

My takeaway: Don’t let the appeal of clever techniques cloud your judgement with respect to more important concerns,such as security and performance.I should have recognized the danger of code like `greeting.”${param}”`.Doing anything with user-input should be treated with the utmost suspicion,even in a “secure” environment such as the system I was working with.Thankfully, I had an alert teammate who called me on it.    

## UPDATE:

The main assumption in this article is that you’re starting with a `GString`.Now,hopefully your web framework would not plop user-input into `GString`s,but into plain old `String`s.If that is the case,then the “danger” mentioned in the article isn’t really there.For example, this code:         

	String plainString = new String(“new File(‘/Users/me/Documents/Financial’).eachFile { file -> println(‘Sending this file to malicious server: ‘ + file.name) }; ‘sayHello'”)
	assert plainString.class == java.lang.String
	greeting.”${plainString}”()
	 

should result in `groovy.lang.MissingMethodException`,as I initially expected. So…. nevermind?Heh,maybe,but I think it’s still an interesting thing to watch out for.   


 
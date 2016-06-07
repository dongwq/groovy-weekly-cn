# Easy Database Manipulation with Groovy and Gradle

# 借助Groovy和Gradle简化数据库操作  

> [原文链接](https://www.javacodegeeks.com/2016/02/easy-database-manipulation-groovy-gradle.html)   

## Groovy:  The “Enterprise Hipster” Language

## Groovy:  企业领域的时髦语言   

Not everyone sees the Java programming language as sexy.  However, the Java virtual machine is a dominant force everywhere, from the most conservative enterprise to the most whimsical startup.  There are myriad alternative languages today that compile to Java bytecode.  There are JVM-based versions of [Python](http://www.jython.org/), [Ruby](http://jruby.org/), and [multiple](https://blogs.oracle.com/nashorn/) [implementations](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Rhino) of JavaScript.  There are entirely new languages, such as [Kotlin](http://kotlinlang.org/) from JetBrains and [Ceylon](http://www.ceylon-lang.org/) from RedHat.  Clojure has recently re-awakened interest in Lisp, and of course Scala is largely responsible for the 2000’s shift toward functional programming on the server-side.

并非所有人都认为Java语言很性感。但是，Java语言从传统企业到激进的创业公司中都占据统治地位。现在有无数种可以编译成Java字节码的语言。有[JPython](http://www.jython.org/)，[JRuby](http://jruby.org/)和其他[各种](https://blogs.oracle.com/nashorn/)基于JVM实现的[Javascript]((https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Rhino))。更有全新的语言，比如JetBrains公司的[Kotlin](http://kotlinlang.org/)以及RedHat的[Ceylon](http://www.ceylon-lang.org/)。Clojure唤醒了人们对Lisp语言的兴趣，Scala语言很大程度上促使服务端开发转向函数式编程。


Groovy, the granddaddy of them all, is today almost invisible in its ubiquity.  When it first appeared 13 years ago, Groovy was an instant hit.  The language, and the related Grails web framework, combined the emerging popularity of Ruby on Rails with an extremely shallow learning curve for Java developers.  Virtually overnight, Groovy completely replaced BeanShell, the previous JVM-scripting alternative.
Groovy是上面这些可以编译成java字节码语言的老祖宗，它无处不在。13年它出现的时候引起了轰动。用Groovy编写的Grails web框架融合了新兴的Rbuy on Rails的特点，降低了java开发者的学习曲线。好像一夜之间，Groovy语言就完全取代了JVM基础的基本语言——BeanShell。


Enthusiasm for the Rails model eventually waned, and strongly-typed languages became the trend once more.  Quite frankly, many people who flocked to Groovy simply because it was “new” continued to move on to newer things.  However, Groovy didn’t fade away.  Rather, it settled into a mature role as the “enterprise hipster” language.  You find it everywhere.  Almost any application on the JVM that exposes a scripting interface does so with Groovy as the first-class citizen.  Groovy is extremely popular with QA in the automated testing space, is deeply baked into the Spring framework, and is the basis for the fast-growing Gradle build system.

   
对Raisl模型的热情最终还是消退了，强类型的语言再一次变成主流。坦白地说，很多人只是因为Groovy是新的语言才转移到Groovy上的。但是Grovoy是不会消失的。甚至，Groovy已经是企业领域时髦语言。你可以在任何地方发现它。大多数运行在JVM上需要提供脚本接口的项目都是用Groovy编写的。Groovy在自动化测试中非常流行，Groovy已经深深融合进Spring框架，Groovy是快熟成长的Gradle编译系统的基础。

We don’t hype Groovy as much as we used to, but it’s absolutely entrenched in the Java ecosystem, and is continuing to expand.  It’s a stable, safe bet, for which it’s easy to find talent (or quickly train it on-the-job).  While there are more trendy buzzwords to put on your resume today, there seems little risk of Groovy flaming out and going away anytime soon.  Groovy “just works”, and is a really convenient tool that every Java developer should have in his or her toolbox.
我们不会像以前那样大肆宣传Groovy，但是Groovy在Java生态系统中绝对是根深蒂固的，并且它还在不断成长中。很容易找到优秀的Groovy人才，也很容易教会员工使用Groovy。虽然有很多时髦的技术词汇可以放在你的简历中，但是Groovy很稳定，不会突然火热一下就消失了，所以为什么不把Groovy这么时髦的词汇放在你的简历中呢？Groovy是一个很方便的工具，所以每一个Java程序员都应该把它放到你的工具箱中。   

## Gradle as a Groovy App Server

## Gradle作为Groovy应用服务器

History aside, let’s talk about a recent use case that lead me to dust off my Groovy skills.  I needed to quickly stand up a registry of “key-value” config parameters, for a number of applications running within a number of environments.  I wanted to capture these parameters in source control as a collection of properties files.  One file for each application, nested within a subdirectory for each environment:
不谈历史了，谈谈最近的实际案例。


- …
- qa-env/
    - application-a.properties
    - application-b.properties
    - …

- staging-env/
    - application-a.properties
    - application-b.properties
    - …
- …

Whenever a change to these properties files is committed in source control, I would like Jenkins (or some other continuous integration server) to sync its values with a runtime “registry”.  That registry might eventually become something like etcd, or Consul and Vault, but we can get things started quickly with a traditional MySQL database.
Since most of our continuous integration build jobs are Gradle-based these days, and since Gradle is Groovy-native, we can bake this “sync” job into a Gradle build.  With a JavaExec-based task, pointing to a Groovy script, you can leverage Gradle as a Groovy app server!
build.gradle


	apply plugin: 'groovy'

	repositories {
	    mavenCentral()
	    mavenLocal()
	}

	// [1] Declare a localGroovy() dependency, to use 
	//     the Groovy library that ships with Gradle.
	dependencies { 
	    compile localGroovy() 
	    compile("mysql:mysql-connector-java:5.1.35") 
	    compile("com.h2database:h2:1.4.187") 
	    testCompile("junit:junit:4.12") 
	} 

	// [2] Create a task of type 'JavaExec', referencing 
	//     a Groovy script and any input arguments. 
	task runScript(type: JavaExec) { 
	    description 'Run a Groovy script to sync the environment config registry with the properties files in source control' 
	    classpath = sourceSets.main.runtimeClasspath 
	    main 'com.mypackage.SyncScript' 
	    args Arrays.asList('jdbc:mysql://registry/db', 'com.mysql.jdbc.Driver', 'user', 'password').toArray() 
	} 

	// [3] Tell Gradle to invoke your Groovy script task. 
	defaultTasks 'runScript'


Presto!  It’s fairly trivial to write a Gradle build script that executes some arbitrary Groovy code.  Since the preferred way to run Gradle these days is through a thin wrapper script, you can deliver this solution straight from your source control repo to anywhere without Gradle being installed.
In other words, the above is all you need to make Jenkins run a Groovy script whenever there’s a commit to its source control repository.
Groovy SQL
Now for the really neat part, the Groovy “sync” script itself.  This script scans an arbitrary number of per-environment directories, scans an arbitrary number of per-application property files within each directory, and syncs those properties with a MySQL database table.


	// Iterate through each per-environment directory
	new File('config').eachDir { File environmentDirectory ->

		// Iterate through each per-application properties file
		environmentDirectory.eachFileMatch FileType.FILES, ~/.+\.properties/, { File applicationFile ->

			def environment = environmentDirectory.name
			def application = applicationFile.name.replace('.properties', '')
			println "Processing properties for env: '$environment', application: '$application'"

			// Parse the file into a java.util.Properties object
			def properties = new Properties()
			applicationFile.withInputStream { stream -> properties.load(stream) }

			...
			
		}
	}

Java 8 Streams have made this sort of thing more friendly and readable in pure-Java land, but it still can’t touch the simplicity of Groovy’s extensions to classes like File.  The eachDir() and eachFileMatch() add-on methods make it easy to iterate through all of the directories, and scan for files having the extension “.properties“.  The withInputStream() method helps us load the contents of each file into a java.util.Properties object with a one-liner.
Aside from extensions to java.io.File, Groovy offers its own groovy.sql.Sql class to facilitate JDBC operations.  This reduces much of the boilerplate needed to construct a database query, and allows us to process its ResultSet within a closure:

	database = groovy.sql.Sql.newInstance(jdbcUrl, jdbcUsername, jdbcPassword, jdbcDriver)
	database.resultSetConcurrency = ResultSet.CONCUR_UPDATABLE

	// Iterate through the properties, and sync MySQL
	properties.entrySet().each {
		def name = it.key
		def value = it.value
		def existingRecordQuery = '''
	SELECT environment, service, property_name, property_value FROM environment_properties
	WHERE environment = ? AND service = ? AND property_name = ?
	'''
		database.query(existingRecordQuery, [environment, service, name]) { ResultSet rs ->
			if (rs.next()) {
				def existingValue = rs.getString('property_value')
				if (existingValue.equals(value)) {
					// Existing property value is unchanged.  No-op.
				} else {
					// Existing property value has changed.  Update.
					rs.updateString('property_value', value)
					rs.updateRow()
				}
			} else {
				// New property.  Insert.
				rs.moveToInsertRow()
				rs.updateString('environment', environment)
				rs.updateString('service', service)
				rs.updateString('property_name', name)
				rs.updateString('property_value', value)
				rs.insertRow()
			}
		}
	}

	// TODO: Remove from the database properties that have 
	//       been removed from the properties file.

	
Several interesting things are happening here:
On line 2, we change the concurrency setting to ResultSet.CONCUR_UPDATABLE.  A lot of Java developers are unaware that Java even supports this!
This setting allows you to update, insert, or delete rows in a ResultSet object, without having to construct additional JDBC statements.  See examples of this happening on lines 20 and 29.  Much of the convenience of an ORM, with the simplicity of raw JDBC!
As you can see on lines 8-11, Groovy allows for multi-line string literals with triple quote marks.  This makes it it much more readable to include long strings of SQL in your source code.
On line 12, we see that groovy.sql.Sql allows you to execute a statement and deal with its result within a closure.  One convenience is that the underlying JDBC statement will be closed automatically at the end.
Conclusion
This particular use case is very specific, but it showcases multiple concepts that are broadly useful in isolation.  Groovy is a very powerful language, that may be welcome in environments where other alternatives are not.  It’s native to Gradle, which is fast becoming the Java ecosystem’s most dominant build tool, and so Groovy is easy to leverage through your continuous integration server.  Finally, Groovy comes with a full library of classes, and extensions to core Java classes, that really strip out much of the boilerplate and complexity of common tasks.
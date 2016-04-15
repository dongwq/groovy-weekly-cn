
## Changing the embedded server in Grails 3
 
I have a pet project that I’ve written in Grails 3. I run it on an already-busy cloud server via [the fat jar](https://spring.io/blog/2014/03/07/deploying-spring-boot-applications#embedded-web-server-deployment).I kept the default Tomcat configuration but soon I kept getting out of memory errors.I wanted to use something more lightweight.So I started looking how to change out Tomcat for something else in Grails 3,but I couldn’t find anything.But Grails 3 is just Spring Boot, right?   

I found [this page](https://docs.spring.io/spring-boot/docs/current/reference/html/howto-embedded-servlet-containers.html#howto-use-undertow-instead-of-tomcat) on in the Spring Boot docs about changing from Tomcat to [Undertow](http://undertow.io/). I’ve used Undertow before and I really liked it. The documentation didn’t quite match what I had in my `build.gradle` file but it was really pretty easy. I simply changed this line:   


	compile "org.springframework.boot:spring-boot-starter-tomcat"


to this:   

	compile "org.springframework.boot:spring-boot-starter-undertow"   


And that was it — I recompiled and redeployed… and haven’t had a memory problem since.That was two months ago.The only difference I’ve seen is that [dbconsole](http://www.redtoad.ca/ataylor/2011/11/h2-database-console-in-grails-2/) doesn’t work while running in development mode, but that’s not a big deal to me.

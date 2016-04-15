## 替换Grails 3中的内置服务器

我有一个使用Grails 3技术的试验项目。我把这个项目打包成一个[胖jar](https://spring.io/blog/2014/03/07/deploying-spring-boot-applications#embedded-web-server-deployment)，然后部署到一个已经很繁忙的云服务器上去运行。项目使用默认的Tomcat配置，但是很快我就老是要处理内存错误。我想要使用一个更轻量级的服务器。我开始查找怎么替换Grails 3内置的服务器Tomcat,但是没有找到任何资料。但是Grails 3就是Spring Boot，不是吗？   

我在Spring Boot文档中找到怎么把Tomcat替换成[Undertow](http://undertow.io/)的[页面](https://docs.spring.io/spring-boot/docs/current/reference/html/howto-embedded-servlet-containers.html#howto-use-undertow-instead-of-tomcat)。我使用过Undertow，我很喜欢Undertow。这个文档跟`build.gradle`文件中的配置不是很匹配，但是它已经很简单了。我就把下面一句话：    


	compile "org.springframework.boot:spring-boot-starter-tomcat"

替换成：   

	compile "org.springframework.boot:spring-boot-starter-undertow"   


就这样子——然后我编译部署.....从那之后我就没有内存问题了。这是两个月前的事了。现在我发现在开发模式下[dbconsole](http://www.redtoad.ca/ataylor/2011/11/h2-database-console-in-grails-2/)不能工作，不过这对我来说并不是什么大问题。
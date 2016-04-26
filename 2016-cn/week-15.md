
# Grails Diary - Week 15 in 2016 <small>18-04-2016</small>

# Grails 周报 - 2016年第15周 <small>18-04-2016</small>

> original at (link)[http://grydeske.net/news/show/134]

> 源文档见(链接)[http://grydeske.net/news/show/134]

Last weeks edition of the Grails Diary was heavy on conference videos, slides and articles. This week, it is more of a release edition, including the release of a new set of utilities to assist when developing Groovy AST transformations.

上周的内容以会议视频，PPT和文章居多。本周的新发布内容较多，包括一系列Groovy AST相关的工具。

The Grails team has released bugfix version og the 3.0 and 3.1 line, to be exact [3.0.16](https://github.com/grails/grails-core/releases/tag/v3.0.16) and [3.1.5](https://github.com/grails/grails-core/releases/tag/v3.1.5). A couple of the issues are labelled with Blocker, so it is probably worth an upgrade if you are on Grails 3 now.

Grails团队发布了两个bug修复版本[3.0.16](https://github.com/grails/grails-core/releases/tag/v3.0.16) 和 [3.1.5](https://github.com/grails/grails-core/releases/tag/v3.1.5). 好多个bug问题都是打了Blocker标签的，相对比较重要，所以这两个版本推荐升级。

Along with releases of the framework, there is a couple of noteworthy plugin upgrades. Burt have released milestone 2 of the spring-security-ui plugin for Grails 3, with [updated documentation too](https://grails-plugins.github.io/grails-spring-security-ui/). Puneet Behl from To the New Digital, have published version 1.0.0.1 of the Elasticsearch plugin for Grails 3, also with [improved documentation](http://noamt.github.io/elasticsearch-grails-plugin/docs/index.html). The list of plugins updated to Grails 3 by Puneet is long and impressive!

与此同时，有几个值得关注的插件得到了更新。spring-security-ui插件发布了m2版本和[更新了相应的文档](https://grails-plugins.github.io/grails-spring-security-ui/)。Puneet Behlv发布了适用Grails 3的Elasticsearch插件的1.0.0.1版本和[文档](http://noamt.github.io/elasticsearch-grails-plugin/docs/index.html)。本周的插件更新列表比较长。

Mario García, who recently gave a great presentation on AST transformations at Greach, have released [Asteroid](https://github.com/grooviter/asteroid/), a set of utilities to make it easier to develop AST transformations in Groovy. The documentation is [found here.](http://grooviter.github.io/asteroid/)

Mario García做了一个非常不错的关于AST transformations的演讲，并发布了的相关项目[Asteroid](https://github.com/grooviter/asteroid/)
。这个项目可以帮助你更容易的使用AST transformations做开发，文档在[这里](http://grooviter.github.io/asteroid/)。

Thank you Groovy Podcast for the shoutout! Latest edition can be found in the video section, and the show notes for all the podcast episodes is available in [this repo.](https://github.com/pledbrook/groovypodcast) Witty and informative at the same time!

新一期的Groovy Podcast出来了。你可以在视频部分看到，并且可以在[这里]((https://github.com/pledbrook/groovypodcast)看到以往各期podcast的笔记。听聪明人聊技术，快乐成长每一天。

The first release candidate of Ratpack 1.3 is out, with upcomming [release notes available here](https://ratpack.io/versions/1.3.0). Jeff Beck advertised several of the new features at Greach, including the possibility to order dependent services. The slides and code from Jeff's talk is available in last weeks edition of the Grails Diary. Several dependencies have been updated including Netty and Groovy, a new include() method in the Groovy script DSL to compose an app from discrete scripts, and a new Promise.time() method to measure completion time of a promise.

Ratpack 1.3 rc1版本发布了，更新日志在[这里](https://ratpack.io/versions/1.3.0)。作者Jeff Beck在Greach大会上声称有几个重要的新特性
，比如依赖的服务之前可以排序了。它的讲演和PPT在上周的Grails周报中已经提到。这个版本的Ratpack同时更新了依赖的Netty和Groovy版本， 提供了一个基于Groovy DSL的include(), 这个脚本文件，可以拆分成多个小的了。提供了一个Promise.time()方法，可以用来试题一个promise的执行用时。

Tobias Gesellchen has updated his Docker client written in Groovy, so it now now supports named pipes on Windows 10 with Docker 1.11\. The project is [found here](https://github.com/gesellix/docker-client). This is the library behind his [gradle-docker-plugin](https://github.com/gesellix/gradle-docker-plugin).

Tobias Gesellchen更新了他用Groovy语言写的Docker客户端，这个版本使用Docker1.11，可以支持win 10的命名管道。项目源码在[这里](https://github.com/gesellix/docker-client)。他使用这个项目写了个Docker的Gradle插件[gradle-docker-plugin](https://github.com/gesellix/gradle-docker-plugin)。

#### Podcasts and Videos of Presentations
#### Podcasts 和 视频讲演

*   [Groovy Podcast Ep 26](https://www.youtube.com/watch?v=IqMhAiecaeU) (Ken Kousen and Baruch Sadogursky)

#### Blogs, Articles, etc.
#### 博客文章等

*   [如何升级到Grails 3](https://erichelgeson.github.io/blog/2016/04/17/upgrading-grails-3/) (Eric Helgeson)，这个值得一个哦
*   [Using Self Contained Node.js and npm instances with Gradle](https://objectpartners.com/2016/04/14/using-self-contained-node-js-and-npm-instances-with-gradle/) (Jeff Torson)
*   [2 Rookie Java Constants and Enums Pitfalls](https://tedvinke.wordpress.com/2016/04/14/2-rookie-java-constants-and-enums-pitfalls/) (Ted Vinke)
*   [Groovy Calamari - Issue 31](http://groovycalamari.com/issues/31) (Sergio del Amo)
*   [Deploying Grails 3 to WildFly 10](http://grails.io/post/142674392718/deploying-grails-3-to-wildfly-10#_=_) (Graeme Rocher)
*   [Latest jQuery with Grails 2 and the resources plugin](http://blog.exensio.de/2016/04/latest-jquery-with-grails-2-and.html) (Florian Mutter)
*   [Greach 2016, the Groovy Spanish conference](http://luiyo.blogspot.dk/2016/04/greach-2016-groovy-spanish-conference.html) (Luis García Castro)

[![](http://grydeske.net/fileUploader/show/43)](http://gr8conf.eu/#/)

#### New Grails 3 Plugins
#### 新的 Grails 3 插件

*   [hazelgrails](https://bintray.com/enesakar/plugins/hazelgrails/view) (1.0.2) Hazelcast Grails Integration

#### Updated Grails 3 Plugins
#### 更新的 Grails 3 插件

*   [boselecta](https://bintray.com/vahid/maven/boselecta/view) (3.0.4) Websocket autocomplete/ multi dependency selection plugin for grails 3
*   [jssh](https://bintray.com/vahid/maven/jssh/view) (3.0.2) Grails j2ssh plugin
*   [jenjir](https://bintray.com/vahid/maven/jenjir/view) (3.0.2) Grails Jenjir plugin
*   [ajaxdependancyselection](https://bintray.com/vahid/maven/ajaxdependancyselection/view) (1.2) Grails ajaxdependancyselection plugin
*   [views-gradle](https://bintray.com/grails/plugins/views-gradle/view) (1.0.8) Grails views-gradle plugin
*   [grails-views](https://bintray.com/grails/plugins/grails-views/view) (1.0.8) Grails Views
*   [spring-security-ui](https://bintray.com/grails/plugins/spring-security-ui/view) (3.0.0.M2) Grails spring-security-ui plugin
*   [elasticsearch](https://bintray.com/puneetbehl/plugins/elasticsearch/view) (1.0.0.1) Elasticsearch is a search server based on Lucene. It provides a distributed, multitenant-capable full-text search engine with an HTTP web inter?
*   [spring-security-jaxrs](https://bintray.com/budjb/grails-plugins/spring-security-jaxrs/view) (3.0.0) A plugin that allows the use of Spring Security features with JAX-RS resources.
*   [filterpane](https://bintray.com/ctoestreich/grails-plugins/filterpane/view) (3.0.6)
*   [aws-sdk](https://bintray.com/agorapulse/plugins/org.grails.plugins:aws-sdk/view) (1.10.69) Grails AWS SDK plugin

#### Updated Grails 2 Plugins
#### 更新的 Grails 2 插件

*   [Recurly Plugin](https://grails.org/plugin/recurly) Recurly Grails API.
*   [Grails Audit Trail Plugin](https://grails.org/plugin/audit-trail) This plugin lets you add an annotation to your domain classes so they will get a user and date stamp after a new insert or update.
*   [ElasticSearch Grails Plugin](https://grails.org/plugin/elasticsearch) The revived Elasticsearch plugin for Grails.
*   [Karman AWS Plugin](https://grails.org/plugin/karman-aws) Karman AWS provides an Amazon S3 Interface to the Karman API
*   [Karman Plugin](https://grails.org/plugin/karman) Karman is a standardized / extensible interface plugin for dealing with various cloud services including Local and S3.

#### Interesting Tweets
#### 相关的有推特

*   [@bsideup](https://twitter.com/bsideup/status/721971136494497793) @marioggar @ApacheGroovy did you know that you can use macro {} without 2.5? [https://github.com/bsideup/MacroGroovy](https://github.com/bsideup/MacroGroovy) it's the same impl (was merged to core)
*   [@kenkousen](https://twitter.com/kenkousen/status/721729439852339200) Reason enough to go right there [https://twitter.com/gr8conf/status/721725046348259328](https://twitter.com/gr8conf/status/721725046348259328)
*   [@_bobbyratliff](https://twitter.com/_bobbyratliff/status/721507238691479554) My favorite slide from @codeJENNerator at @TCCodeCamp 20: Monolithic vs. microservices: [https://speakerdeck.com/jlstrater/test-driven-approaches-to-documenting-restful-apis-1](https://speakerdeck.com/jlstrater/test-driven-approaches-to-documenting-restful-apis-1) [https://t.co/06bldbKiE4](https://t.co/06bldbKiE4)
*   [@codeJENNerator](https://twitter.com/codeJENNerator/status/721366298312114176) Slides for my #tccc20 #springrestdocs talk are available @ [https://speakerdeck.com/jlstrater/test-driven-approaches-to-documenting-restful-apis-1](https://speakerdeck.com/jlstrater/test-driven-approaches-to-documenting-restful-apis-1) No video. You'll just have to come see it at #gr8conf :)
*   [@digitalocean](https://twitter.com/digitalocean/status/721473803075915777) Using this guide, you can setup HTTP/2 for improved transfer speed for your server [http://do.co/22xQ0vn](http://do.co/22xQ0vn)
*   [@digitalocean](https://twitter.com/digitalocean/status/721350448003858434) With these security guides you can learn the best practices for securing your infrastructure [http://do.co/1L6HMHG](http://do.co/1L6HMHG) [https://t.co/HCkCDuKP1M](https://t.co/HCkCDuKP1M)
*   [@codepipes](https://twitter.com/codepipes/status/721112877231423488) The @spockframework book is now available in epub/kindle format as well.[https://www.manning.com/books/java-testing-with-spock](https://www.manning.com/books/java-testing-with-spock)
*   [@aalmiray](https://twitter.com/aalmiray/status/721072048051785728) next 3 months: Paris, Lugano, Rovijn, Sofia, Copenhagen, Krakow. Bringing #hackergarten, #groovy, #javafx near you. Let’s meet & hack!
*   [@ThePracticalDev](https://twitter.com/ThePracticalDev/status/721037975061164033) Maybe you will remember the entire codebase forever and nobody else will ever touch it. [https://t.co/HUEV5qPOZn](https://t.co/HUEV5qPOZn)
*   [@aalmiray](https://twitter.com/aalmiray/status/721008502878183424) THIS [https://github.com/griffon/griffon/commit/dc442a95b9967f628050bf1628a5bc22fd3f7172](https://github.com/griffon/griffon/commit/dc442a95b9967f628050bf1628a5bc22fd3f7172) #groovyfx
*   [@craigburke1](https://twitter.com/craigburke1/status/720997061647204352) If you want help migrating from bower installer #gradle to client dependencies #gradle throw an issue up here: [https://github.com/craigburke/client-dependencies-gradle](https://github.com/craigburke/client-dependencies-gradle)
*   [@alexsotob](https://twitter.com/alexsotob/status/720981236085354497) Using #Gradle is like #Git. At first it hurts but then you cannot live without it.
*   [@aalmiray](https://twitter.com/aalmiray/status/720907125413842944) Version 0.1.0 of undecorator has been released! Grab it now from #bintray [https://bintray.com/in-sidefx/maven/undecorator/0.1.0!](https://bintray.com/in-sidefx/maven/undecorator/0.1.0!) thanks @ArnaudNouard !
*   [@Lspacewalker](https://twitter.com/Lspacewalker/status/720666114108350464) [http://i.imgur.com/FVjyaqJ.png](http://i.imgur.com/FVjyaqJ.png) "Skynet will be written in Groovy" - @jbaruch 2016 from @groovypodcast #groovylang
*   [@niklaspasila](https://twitter.com/niklaspasila/status/720637529066745856) Getting familiar with @grailsframework. It already feels like I've used it for ages. #intuitive
*   [@mojavelinux](https://twitter.com/mojavelinux/status/720169261021290496) Welcome AsciidoctorJ Screenshot to the Asciidoctor organization on GitHub! Learn more here: [https://github.com/asciidoctor/asciidoctorj-screenshot](https://github.com/asciidoctor/asciidoctorj-screenshot)
*   [@ilopmar](https://twitter.com/ilopmar/status/720157544673644544) I'll give two talks at @JavaCro about @ApacheGroovy & also @spockframework [http://2016.javacro.hr/eng/](http://2016.javacro.hr/eng/) #IvánOnTour2016 [https://t.co/GykkDVBiqf](https://t.co/GykkDVBiqf)
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/720148327845781504) The type checking extensions in #groovylang are underrated. Look at crazy stuff #grailsfw 3.1 does with statically compiled json views. 1/2
*   [@bartoleo74](https://twitter.com/bartoleo74/status/720145015431892992) Greach 2016 [http://www.bmeweb.it/greach-2016/](http://www.bmeweb.it/greach-2016/) #greach #grailsfw #groovylang
*   [@bgoetzmann](https://twitter.com/bgoetzmann/status/719985445141159936) Hey, I got good reviews for my #Android app Cosmos Pictures developed in #groovylang [https://play.google.com/store/apps/details?id=com.odelia.cosmospictures&hl=en](https://play.google.com/store/apps/details?id=com.odelia.cosmospictures&hl=en)
*   [@brianjohnsendk](https://twitter.com/brianjohnsendk/status/719963171172311040) Currently jugglin' 4 different versions of @grailsframework. Thx @marc0der for making that easy as pie with @sdkmanager You da' boss!
*   [@RyanVanderwerf](https://twitter.com/RyanVanderwerf/status/719957580131373056) Will have to make it next year!! [https://twitter.com/JacobAae/status/719629263754944513](https://twitter.com/JacobAae/status/719629263754944513)
*   [@mariomddavid](https://twitter.com/mariomddavid/status/719951769242058752) @CubaPlatform made @ApacheGroovy a first-class citizen. Create #groovy business application with #oss easily: [http://bit.ly/20vKb29](http://bit.ly/20vKb29)
*   [@puneetbhl](https://twitter.com/puneetbhl/status/719897074821496832) @NCapito @grailsframework That's not true, we are using Grails from last 6 or more years to build products from scratch and it's awesome.

#### Conferences and meetups
#### 会议与见面会

*   [Groovy Users of Minnesota: Codenarc Revisited](http://www.meetup.com/groovymn/events/230230141/), Minneapolis, Mn, May 10th, 2016.
*   [GR8conf Europe & Gradle Event](http://gr8conf.eu/), Copenhagen - Denmark, June 1st -3rd, 2016.
*   [Gradle Summit](http://gradlesummit.com), Palo Alto - CA, June 23rd -24th, 2016.
*   [GR8conf US](http://gr8conf.us/), Minneapolis - USA, July 27th - 29th, 2016.
*   [G3 Summit](https://g3summit.com) , Fort Lauderdale - USA, November 27th - December 1st, 2016.- [CFP is open!](https://g3summit.com/home/speaker_request)


# Grails日志 - 2016年第四周<small>2016年2月1号</small>

> [源文档链接][http://grydeske.net/news/show/126]

Grails 3真的在飞速发展了。这周没有新的或更新的Grails 2插件，但是有一大把新的和更新的Grails 3插件。        

这周最大的新闻就是[Grails 3.1](https://github.com/grails/grails-core/releases/tag/v3.1.0)的发布了。Grails文档中有[一个章节](http://grails.github.io/grails-doc/3.1.x/guide/introduction.html#whatsNew31)讲述了Grails 3中的新特性，重点是对自定义构建环境(profile)的加强(包括发布和仓库)，新的REST API和AngularJS自定义构建环境，和GORM 5套件以及方便发布插件的插件。Graeme接受了[Groovy Podcast](https://www.youtube.com/watch?v=ZxExU0lbMUI&feature=youtu.be)的采访，讨论了Grails的历史和最新的3.1版本。        

Burt Beckwith在一篇[文章](https://plumbr.eu/blog/io/how-we-accidentally-doubled-our-jdbc-traffic-with-hibernate)中指出日志设置会引发Hibernate性能问题。这篇文章值得一读，因为Grails/GORM大多数情况下底层使用的就是Hibernate。       
  
Groovy开发团队正在Groovy邮件列表上讨论Groovy下一个主要版本的路线图和语言特点。 这需要做很多工作，也意味着源源不断的贡献。     


Power blogger Mr Haki (if you don't believe me, check the blog section) has updated four of his notebooks on leanpub: [Groovy Goodness](http://mrhaki.blogspot.dk/2016/02/groovy-goodness-notebook-is-updated.html) [Gradle Goodness](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-notebook-updated.html) [Spocklight](http://mrhaki.blogspot.dk/2016/02/spocklight-notebook-is-updated.html) and [Grails Goodness](http://mrhaki.blogspot.dk/2016/02/grails-goodness-notebook-updated.html)

超级博主Mr Haki（如果你不相信我，可以查看博客那章节）在leanpub更新了四篇笔记： [Groovy优点](http://mrhaki.blogspot.dk/2016/02/groovy-goodness-notebook-is-updated.html)、 [Gradle优点](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-notebook-updated.html)、 [Spocklight](http://mrhaki.blogspot.dk/2016/02/spocklight-notebook-is-updated.html)和[Grails 优点](http://mrhaki.blogspot.dk/2016/02/grails-goodness-notebook-updated.html)                                                                                                                                

Craig Burke分享了《关于Gradle的一切》的视频以及相关的[PPT](http://www.craigburke.com/gradle-intro/)和(代码)[(https://github.com/craigburke/gradle-intro)]。      

Phill Barber has tried to do a comparison of [Ratpack and Dropwizard](http://phillbarber.blogspot.com/2016/01/choosing-between-ratpack-and-dropwizard.html), and have measured performance and other metrics, and have Ratpack as his teams new framework.

Phill Barber对[Ratpack和Dropwizard](http://phillbarber.blogspot.com/2016/01/choosing-between-ratpack-and-dropwizard.html)的性能和其他指标作了比较，并决定把Ratpack作为他们团队的新框架。   

Peter Ledbrook is the instructor on a couple of [new courses on Groovy and Grails](http://blog.cacoethes.co.uk/groovyandgrails/a-new-approach-to-training), where instead of intensive one or more day training, the timespan is longer with feedback gradually. I'm interested in how Peters experiences with this style is, as it sounds promissing for long term retention of the material.

Peter Ledbrook是一系列Groovy和Grails新课程的指导，这些课程不是一天或几天的加强训良，而是根据反馈不断改进延续。我对Peters对这种模式的体验很感兴趣，因为这意味着长期的投入。     

After Spring One dropped the 2GX part, New No Fluff Just Stuff is instead having a dedicated Groovy, Grails and Gradle conference, the [G3 Summit](https://g3summit.com) this year in Fort Lauderdale late november/early december.

随着Spring One取消了2GX，New No Fluff Just Stuff已经取代并成为专注与Groovy,Grails和Gradle的会议， 今年将于11月末12月初在劳德代尔堡召开的[G3 Summit](https://g3summit.com)会议。   

Greach, the Spanish Groovy conference, has published [the agenda](http://greachconf.com/agenda/), with lots of interesting talks and speakers. I'll present a talk on Geb, and is really looking forward to visiting Spain again. Last year was a great experience! And the conference has extended the [early bird ticket](http://greachconf.com/#tickets) discount, with a few tickets, now that the agenda is out, - but hurry, there a only a few left!

Greach，西班牙Groovy会议，已经公布了[会议议程](http://greachconf.com/agenda/),在议程中可以发现很多有意思的演讲和演讲者。我也会在Geb上发表演讲，真的非常盼望再一次访问西班牙。去年在那里过得很开心。大会提供了更多折扣的少数[early bird ticket](http://greachconf.com/#tickets)票，现在议程已经出来——赶紧呀，真的只有一些票剩下了。   

The call for paper is still [open](http://cfp.gr8conf.org/login/auth), for both GR8Conf EU, GR8Conf US and a new mini conference in Warsaw, the GR8Day Warsaw on March 19th.

GR8Conf欧洲会议, GR8Conf美国会议和3月19号在华沙召开的GR8Day会议还在征文中。   


#### Podcasts and Videos of Presentations

*   [All About Gradle](https://www.youtube.com/watch?v=xyJvFqLLdXg) (Craig Burke from Pittsburgh Groovy Meetup)
*   [Groovy Podcast Special Edition: Grails project lead Graeme Rocher](https://www.youtube.com/watch?v=ZxExU0lbMUI&feature=youtu.be) (Ken Kousin with Graeme Rocher)
*   [Building Continuous Delivery: Rock-solid builds with Gradle](https://objectpartners.com/2016/02/01/building-continuous-delivery-rock-solid-builds-with-gradle/) (David Norton from Object Partners)
*   [Functional Programming Kata with Groovy](http://www.infoq.com/presentations/fp-groovy) (Scott Hickey from SpringOne 2gx 2015)
*   [Groovy AST Transformations](http://www.infoq.com/presentations/groovy-ast-transformations) (Paul King from SpringOne 2gx 2015)

#### Blogs, Articles, etc.

*   [Hooking into the Instance methods of the GORM API](http://www.tothenew.com/blog/hooking-into-the-instance-methods-of-the-gorm-api/) (Sandeep Poonia)
*   [Grails 3.1 Shipped Today -- here's what's new](http://www.ociweb.com/resources/news/2016/01/28/grails-31-released) (Danielle Johnson)
*   [Running TestFX tests in headless mode](http://www.jroller.com/aalmiray/entry/running_testfx_tests_in_headless) (Andres Almiray)
*   [Grails Goodness: Using Features When Creating An Application](http://mrhaki.blogspot.dk/2016/01/grails-goodness-using-features-when.html) (Hubert Klein Ikkink aka MrHaki)
*   [Spocklight: Grouping Assertions](http://mrhaki.blogspot.dk/2016/01/spocklight-grouping-assertions.html) (Hubert Klein Ikkink aka MrHaki)
*   [Choosing between Ratpack and Dropwizard.](http://phillbarber.blogspot.com/2016/01/choosing-between-ratpack-and-dropwizard.html) (Phill Barber)
*   [Grails Goodness: Getting More Information About A Profile](http://mrhaki.blogspot.dk/2016/01/grails-goodness-getting-more.html) (Hubert Klein Ikkink aka MrHaki)
*   [Groovy Goodness: Customising The Groovy Compiler](http://mrhaki.blogspot.dk/2016/01/groovy-goodness-customising-groovy.html) (Hubert Klein Ikkink aka MrHaki)
*   [Grails Goodness: Changing Gradle Version](http://mrhaki.blogspot.dk/2016/01/grails-goodness-changing-gradle-version.html) (Hubert Klein Ikkink aka MrHaki)
*   [Gradle Goodness: Getting Information About Buildscript Dependencies](http://mrhaki.blogspot.dk/2016/01/gradle-goodness-getting-information.html) (Hubert Klein Ikkink aka MrHaki)
*   [Groovy Goodness: Customise Groovydoc Output With Gradle](http://mrhaki.blogspot.dk/2016/01/groovy-goodness-customise-groovydoc.html) (Hubert Klein Ikkink aka MrHaki)
*   [Groovy Calamari - Issue 25](http://groovycalamari.com/issues/25) (Sergio del Amo)

#### New Grails 3 Plugins

*   [asynchronous-mail](https://bintray.com/kefirsf/plugins/asynchronous-mail/view) (2.0.0.RC1) The plugin realises asynchronous mail sending. It stores messages in a DB and sends them asynchronously by a quartz job.
*   [slack](https://bintray.com/mathifonseca/grails-plugins/slack/view) (2.0.0) Grails Slack Integration Plugin
*   [browser-detection](https://bintray.com/mathifonseca/grails-plugins/browser-detection/view) (3.0.0) Grails Browser Detection Plugin
*   [middleware](https://bintray.com/lduarte/plugins/middleware/view) (0.0.3) Grails middleware plugin
*   [remote-pagination](https://bintray.com/amitjain/plugins/remote-pagination/view) (0.5.0) Grails remote-pagination plugin

#### Updated Grails 3 Plugins

*   [views-gradle](https://bintray.com/grails/plugins/views-gradle/view) (1.0.0) Grails views-gradle plugin
*   [grails-views](https://bintray.com/grails/plugins/grails-views/view) (1.0.0) Grails Views
*   [grails-spring-websocket](https://bintray.com/zyro/maven/grails-spring-websocket/view) (2.3.0)
*   [neo4j](https://bintray.com/grails/plugins/neo4j/view) (5.0.1) GORM - Grails Data Access Framework
*   [mongodb](https://bintray.com/grails/plugins/mongodb/view) (5.0.1) GORM for MongoDB
*   [hibernate5](https://bintray.com/grails/plugins/hibernate5/view) (5.0.1) GORM - Grails Data Access Framework
*   [hibernate4](https://bintray.com/grails/plugins/hibernate4/view) (5.0.1) GORM - Grails Data Access Framework
*   [hibernate3](https://bintray.com/grails/plugins/hibernate3/view) (5.0.1) GORM - Grails Data Access Framework
*   [cassandra](https://bintray.com/grails/plugins/cassandra/view) (5.0.1) GORM - Grails Data Access Framework
*   [fields](https://bintray.com/grails/plugins/fields/view) (2.1.2) Grails fields plugin
*   [redis-gorm](https://bintray.com/grails/plugins/redis-gorm/view) (5.0.1) GORM - Grails Data Access Framework

#### Interesting Tweets

*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/693055377982767104) Thank you @pniederw for your work on @spockframework! Probably one of most useful tools I use everyday. #ThankAnOpenSourceContributorFriday
*   [@pledbrook](https://twitter.com/pledbrook/status/693025569437523968) I don’t think enough credit is given to the #Gradle upgrade experience. One of the few tools that doesn’t induce deep trepidation.
*   [@ysb33r](https://twitter.com/ysb33r/status/692825347159674880) I just got me @mrhaki's #ratpackweb book via @leanpub - [http://leanpub.com/ratpacked-notebook.](http://leanpub.com/ratpacked-notebook.) (Goeie werk, meneer!)
*   [@mittie](https://twitter.com/mittie/status/692394076809863168) Another great alternative for optional typing is #groovylang [https://twitter.com/ftomasse/status/692391818588246016](https://twitter.com/ftomasse/status/692391818588246016)
*   [@breskeby](https://twitter.com/breskeby/status/692385357170655233) Visit me in #berlin for an extraordinary 3 day #gradle In depth training class: [https://www.eventbrite.com/e/gradle-in-depth-training-berlin-tickets-19113147940](https://www.eventbrite.com/e/gradle-in-depth-training-berlin-tickets-19113147940) I promise, we’ll have a lot of fun!
*   [@grailsframework](https://twitter.com/grailsframework/status/692374779874164736) We now have 1400 people on our Slack channel. Don’t forget to signup! [http://slack-signup.grails.org](http://slack-signup.grails.org) #grailsfw #groovylang #grails
*   [@gradle](https://twitter.com/gradle/status/692010575874789376) Answer on @Quora by Vijay Bhore to Which should I learn first, maven, ant or gradle? [https://www.quora.com/Which-should-I-learn-first-maven-ant-or-gradle/answer/Vijay-Bhore?srid=uBb5](https://www.quora.com/Which-should-I-learn-first-maven-ant-or-gradle/answer/Vijay-Bhore?srid=uBb5)
*   [@pledbrook](https://twitter.com/pledbrook/status/691924833827950592) So, is GMaven+ the recommended plugin for compiling #groovylang files in a #Maven project?

#### Conferences and meetups

*   [Groovy & Grails Training](https://objectpartners.com/training/groovyandgrails/) , - Minneapolis, MN, February 24th - 26th, 2016
*   [GR8Day Warsaw 2016](http://www.meetup.com/Warsaw-Groovy-User-Group/events/227938015/), Warsaw - Poland, March 19th, 2016 - [CFP is open!](http://cfp.gr8conf.org/login/auth)
*   [Greach](http://greachconf.com/), Madrid - Spain, April 8th & 9th, 2016
*   [Spring I/O](http://www.springio.net/), Barcelona - Spain, May 19th - 20th, 2016
*   [GR8conf Europe & Gradle miniSummit](http://gr8conf.eu/), Copenhagen - Denmark, June 1st -3rd, 2016.- [CFP is open!](http://cfp.gr8conf.org/)
*   [Gradle Summit](http://gradlesummit.com), Palo Alto - CA, June 23rd -24th, 2016.
*   [GR8conf US](http://gr8conf.us/), Minneapolis - USA, July 27th - 29th, 2016.- [CFP is open!](http://cfp.gr8conf.org/)
*   [G3 Summit](https://g3summit.com) , Fort Lauderdale - USA, November 27th - December 1st, 2016.- [CFP is open!](https://g3summit.com/home/speaker_request)

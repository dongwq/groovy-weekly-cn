# Grails日志 - 2016年第七周<small>2016年2月22号</small>

> (原文档链接)[http://grydeske.net/news/show/128]     

Apache Groovy 2.4.6 has been released! And this release has solved a whooping 59 bugs, improved the documentation, and a number of general improvements around StreamingJsonBuilder, error-message for AST transformation, closures generated as public classes and more. See the [change log](http://groovy-lang.org/changelogs/changelog-2.4.6.html) for the full list of issues fixed. As always, the easiest way to upgrade is to use Sdkman, where Groovy 2.4.6 is already available.

Apache开源项目Groovy 2.4.6版本发布了！该版本解决了高达59个bug，完善了文档，提升`StreamingJsonBuilder`，AST转换的错误提示，闭包生成公共类等。[修改日志](http://groovy-lang.org/changelogs/changelog-2.4.6.html)记录了所有已经修复的问题，有兴趣可以查看一下。升级Groovy最简单的办法就是使用Sdkman，Sdkman从Groovy2.4.6版本就开始提供了。

Cedric Champeau is using the #ThankAnOpenSourceContributorFriday tag on Twitter, which is a great thing. He however recently rediscover the [Groovy FileTreeBuilder,](http://groovy-lang.org/dsls.html#_filetreebuilder) for generating a file directory structure - and found out he had written it [himself!](https://twitter.com/CedricChampeau/status/700731350970736640). I had not seen it before, but can think of a couple of times it could have helped me in the past! Thank you Cedric for this!

Cedric Champeau在推特上使用了#ThankAnOpenSourceContributorFriday标签。他最近重新发现了[Groovy FileTreeBuilder](http://groovy-lang.org/dsls.html#_filetreebuilder)生成文件目录结构的功能，还发现他以前亲自写过[Groovy FileTreeBuilder的文档](https://twitter.com/CedricChampeau/status/700731350970736640).我以前没有看过，但是想了一下发现我以前需要使用到`FileTreeBuilder`。很感谢Cedric。   

The Grails Slack channel now have way more than 1500 members. If you still have not joined, you can do it at [slack-signup.grails.org](http://slack-signup.grails.org).
Grails的Slack频道已经有超过1500位成员了。如果你还没有加入，你可以访问[slack-signup.grails.org](http://slack-signup.grails.org)地址进行操作。   
Should Spock Framework have a real logo? Participate in the [survey](http://goo.gl/forms/1UlVm2kBxZ) by Søren Berg Glasius, to determine if a Kickstarter project should be initiated.
Spock框架是不是应该要有一个真正的图标呢？请参加Søren Berg Glasius做的[调查访问](http://goo.gl/forms/1UlVm2kBxZ),Søren Berg Glasius想要知道是不是应该发布Kickstarter项目(类似于猪八戒的网站，在上面发布一个项目，做好之后给多少钱，现在Søren Berg Glasius就是想要知道要花多少钱开启这个项目。)
Several great answers have been posted on Quora this week. Rob Fletcher has answered: [What are some tips, tricks and gotchas when using Spock Framework for testing?](https://www.quora.com/What-are-some-tips-tricks-and-gotchas-when-using-Spock-for-testing/answer/Rob-Fletcher?srid=hyqW&share=a35d9892) , Robert Dobbes has replied to [What are the pros and cons of Apache Groovy?](https://www.quora.com/What-are-the-pros-and-cons-of-Groovy/answer/Robert-Dobbes?srid=Ln3), and Guilaume Laforge has taken care of [What is the purpose of 'def ' in Groovy programming language?](https://www.quora.com/What-is-the-purpose-of-def-in-Groovy-programming-language/answer/Guillaume-Laforge?share=8b28b64b).
这周Quora上有一些很棒的回答。Rob Fletcher回答了[使用Spock框架做测试的提示、技巧和疑难杂症](https://www.quora.com/What-are-some-tips-tricks-and-gotchas-when-using-Spock-for-testing/answer/Rob-Fletcher?srid=hyqW&share=a35d9892)，Robert Dobbes回复了[Apache Groovy的优缺点](https://www.quora.com/What-are-the-pros-and-cons-of-Groovy/answer/Robert-Dobbes?srid=Ln3)，Guilaume Laforge很好地回复了[Groovy语言中`def`的目的？](https://www.quora.com/What-is-the-purpose-of-def-in-Groovy-programming-language/answer/Guillaume-Laforge?share=8b28b64b)。   

The Betamax project, started by Rob Fletcher, used for recording and replaying external Web APIs has a new website [betamax.software](http://betamax.software), and sees a bit of love from new contributors.
Rob Fletcher发起的Betamax项目可以模拟发起和相应Web请求，这个项目现在有新的[网站](http://betamax.software)了,新的贡献者很喜欢这个项目。   
Ratpack 1.2.0 is now officially released, with lots of new inprovements described in [the version description.](https://ratpack.io/versions/1.2.0) The Ratpack team expects bi-monthly minor releases in the future, and the framework has reached 1000 stars on GitHub!
Ratpack 1.2.0正式发布了，在[版本描述](https://ratpack.io/versions/1.2.0)可以看出Ratpack有了很大的提升。Ratpack团队计划在将来每两个月发布一次小的更新，在GitHub上这个框架已经有1000个加星了。

Craig Burke is taking on the Javascript dependency resolution war, with his Gradle plugin to install from Npm or Bower, without NodeJs, the documentation is [at GitHub in the repo](https://github.com/craigburke/client-dependencies-gradle) and the plugin is in [the Gradle Plugin Portal](https://plugins.gradle.org/plugin/com.craigburke.client-dependencies)

Craig Burk正在解决Javascript依赖包问题，使用他做的Gradle插件就可以不用依赖NodeJs直接从Npm或Bower下载Javascript依赖包，该插件的文档在[Github](https://github.com/craigburke/client-dependencies-gradle)上并可以从[Gradle插件中心](https://plugins.gradle.org/plugin/com.craigburke.client-dependencies)下载插件。
The "Java Testing with Spock" book by Konstantinos Kapelonis is close to the release on [Amazon](http://www.amazon.com/Java-Testing-Spock-Konstantinos-Kapelonis/dp/1617292532), and available for pre-order.
Konstantinos Kapelonis的《使用Spock进行java测试》一书在[亚马逊](http://www.amazon.com/Java-Testing-Spock-Konstantinos-Kapelonis/dp/1617292532)上已经可以预定了，很快就可以销售了。
Oh, and so there should be no doubt: #unfollowdanveloper. Thank you [Groovy Podcast](https://www.youtube.com/watch?v=6VbPV2FRZUU) for the reprimand.
没有参加会议的开发者可以观看[Groovy Podcast](https://www.youtube.com/watch?v=6VbPV2FRZUU)了解详情。

The registration for the one day event: Warsaw GR8 Day is [open](http://www.meetup.com/Warsaw-Groovy-User-Group/events/227938015/)
一天的[华沙GR8日](http://www.meetup.com/Warsaw-Groovy-User-Group/events/227938015/)就要开始了，赶快预定酒店吧。  


#### Podcasts and Videos of Presentations

#### 会议的视频


*   [Groovy Podcast Ep. 23](https://www.youtube.com/watch?v=6VbPV2FRZUU) (Ken Kousin and Baruch Sadogursky live from DevNexus 2016)
*   [Gradle Plugin Basics](https://caster.io/episodes/gradle-plugin-basics/) (Annyce Davis)

#### Blogs, Articles, etc.


#### 博客，文章等

*   [借助Groovy和Gradle简化数据库操作](http://www.javacodegeeks.com/2016/02/easy-database-manipulation-groovy-gradle.html) (Steve Perkins)


*   [Grails Tips: How to install new Relic in a Grails 3 app?](http://sergiodelamo.es/grails-tips-how-to-install-new-relic-in-a-grails-3-app/) (Sergio del Amo)
*   [How to force IntelliJ IDEA to run Grails tests in the Test Environment](http://sergiodelamo.es/how-to-force-intellij-idea-to-run-grails-tests-in-the-test-environment/) (Sergio del Amo)
*   [Grails Tips: Increase Heap Space when running run-app in Grails 3 app](http://sergiodelamo.es/grails-tips-increase-heap-space-when-running-grails-run-app/) (Sergio del Amo)
*   [Grails Tips: How to customize the war name generated by “grails war” command?](http://sergiodelamo.es/grails-tips-how-to-customize-the-war-name-generated-by-grails-war-command/) (Sergio del Amo)
*   [Gradle Goodness: Build Script Using Java Syntax](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-build-script-using-java.html) (Hubert Klein Ikkink aka MrHaki)
*   [Don't be Careless With Groovy (Un)checked Exceptions](https://dzone.com/articles/dont-be-careless-with-groovy-unchecked-exceptions) (Marcin Pilaczynski)
*   [Gradle Goodness: Create Objects Using DSL With Domain Object Containers](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-create-objects-with-dsl.html) (Hubert Klein Ikkink aka MrHaki)
*   [Gradle Goodness: Using Nested Domain Object Containers](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-using-nested-domain.html) (Hubert Klein Ikkink aka MrHaki)
*   [Gradle Goodness: Running Groovy Scripts Using Groovy Command Line](https://dzone.com/articles/gradle-goodness-running-groovy-scripts-using-groov) (Hubert Klein Ikkink aka MrHaki)
*   [Multi-Project AspectJ Builds With Gradle and Eclipse](https://dzone.com/articles/multi-project-aspectj-builds-with-gradle-and-eclip) ( Jaime Metcher)
*   [Groovy Calamari - Issue 26](http://groovycalamari.com/issues/26) (Sergio del Amo)

#### Updated Grails 3 Plugins

*   [wschat](https://bintray.com/vahid/maven/wschat/view) (3.014) Grails wschat plugin
*   [quartz](https://bintray.com/grails/plugins/quartz/view) (2.0.6) Grails quartz plugin
*   [slack](https://bintray.com/mathifonseca/grails-plugins/slack/view) (3.0.0) Grails Slack Integration Plugin
*   [scaffolding](https://bintray.com/grails/plugins/scaffolding/view) (3.2.1) Grails scaffolding plugin

#### Updated Grails 2 Plugins

*   [GR8 CRM Campaign Management User Interface](https://grails.org/plugin/crm-campaign-ui) This plugin is a companion plugin to crm-campaign, a plugin part of the GR8 CRM plugin suite. It contains a Twitter Bootstrap based user interface for campaign management.
*   [GR8 CRM Campaign Services](https://grails.org/plugin/crm-campaign) This plugin provide storage and services for managing campaigns in GR8 CRM based applications. A campaign is something that has a message and a target group, for example an email campaign, a product discount or a web site banner. Custom plugins can provide other campaign types with Grails artifacts.
*   [UberDoc - Rest-API Documentation](https://grails.org/plugin/uberdoc) uberDoc is a very simple solution for creating API documentation based on annotations in domain objects and controllers, and Grails' messag

#### Interesting Tweets

*   [@jitpack](https://twitter.com/jitpack/status/701729615409258497) Even quicker Gradle builds on JitPack - caching Gradle distribution to avoid re-download. Thanks to @sdkmanager!
*   [@gradle](https://twitter.com/gradle/status/701498158073958401) Watch the video: how to manage #Jenkins environment using #Gradle [http://buff.ly/1WqwuyA](http://buff.ly/1WqwuyA)
*   [@RalfDMueller](https://twitter.com/RalfDMueller/status/701485924048310274) Got a @grailsframework app up and running with @jenkinsci on @openshift ! Grails rocks!
*   [@oscon](https://twitter.com/oscon/status/701232522080948224) You can mix Groovy w/ Java class-by-class or even line-by-line. Learn more w/ @kenkousen in a free webcast March 29: [http://oreil.ly/1ornq1B](http://oreil.ly/1ornq1B)
*   [@craigburke1](https://twitter.com/craigburke1/status/700778167926128640) It feels so wrong, but the fact that #groovylang lets me access private fields within a class can be so damn handy in pinch.
*   [@gradle](https://twitter.com/gradle/status/700727238522753024) Catch @bmuschko slides from #SpringOne2gx Building a #ContinuousDelivery Pipeline with #Gradle and #Jenkins [http://buff.ly/1SRqcKJ](http://buff.ly/1SRqcKJ)
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/700718602345910272) "lets you use #Groovy expressions in Evaluate and Watch windows when debugging Java application" Nice! [https://twitter.com/intellijidea/status/700717844745449472](https://twitter.com/intellijidea/status/700717844745449472)
*   [@antonarhipov](https://twitter.com/antonarhipov/status/700698912223600640) An Introduction to #JRebel and #Grails [http://buff.ly/1oPjIzm](http://buff.ly/1oPjIzm) #groovy
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/700596098814124032) I'm amazed by the number of tweets in Japanese about #gradle. I wish I could read them.
*   [@MGrzejszczak](https://twitter.com/MGrzejszczak/status/700423647719268352) We've got an official Twitter handle for @gr8day_warsaw conference! Follow it, visit [http://warsaw.gr8days.pl](http://warsaw.gr8days.pl) and cfp [http://cfp.gr8conf.org](http://cfp.gr8conf.org)
*   [@c0sin](https://twitter.com/c0sin/status/700219163873316864) @danveloper @glaforge You'd be surprised how deeply @ApacheGroovy is rooted into #FOSS projects. E.g. Apache Data stack @ASFbigtop, etc.
*   [@Lspacewalker](https://twitter.com/Lspacewalker/status/700167712727818242) @danveloper probably the reason why Groovy has a quiet adoption, it just works
*   [@gradle](https://twitter.com/gradle/status/700002480680280067) Ticketmaster: Android Gradle Success Story for Android developers who are looking for some inspiration around Gradle [http://buff.ly/1oI4R9E](http://buff.ly/1oI4R9E)
*   [@DailyGradle](https://twitter.com/DailyGradle/status/699971614998265858) For application plugin, get use to using ‘installDist’ task rather than ‘installApp’. Later will be removed in Gradle 3.0 #gradleTip
*   [@svpember](https://twitter.com/svpember/status/699966993630367745) Ratpack 1.2 ([https://ratpack.io/versions/1.2.0](https://ratpack.io/versions/1.2.0)) is out & I’m oddly most excited about the updated Pac4j integration: authentication AND authorization
*   [@madridgug](https://twitter.com/madridgug/status/699903641851809792) "@grailsframework 3: SpringBoot on Steroids". En #SpringMadridUG por @alvaro_sanchez. No te la pierdas! [http://www.meetup.com/es-ES/madrid-spring-user-group/events/227937890/](http://www.meetup.com/es-ES/madrid-spring-user-group/events/227937890/)
*   [@gradle](https://twitter.com/gradle/status/701451886076030979) Have a look at Gretty the Gradle web plugin that allows you to run various apps on multi containers:[http://buff.ly/1SRqiSK](http://buff.ly/1SRqiSK)
*   [@JennStrater](https://twitter.com/JennStrater/status/699831899003478017) Success!! I have my first example endpoint running with #springrestdocs and #grailsfw :)
*   [@angelmbanks](https://twitter.com/angelmbanks/status/699626031360188417) @sjmaple: #groovy = #java supercharged. #JVM #devnexus
*   [@danveloper](https://twitter.com/danveloper/status/699443178634665984) Have had amazing and excellent feedback from the technical reviewers of "Learning Ratpack”. Feeling very privileged to have their insights.
*   [@MGrzejszczak](https://twitter.com/MGrzejszczak/status/699272294644842496) Over the weekend I've created a small library for asserting JSONs (jsonassert). Maybe you'll find it handy! [https://github.com/marcingrzejszczak/jsonassert](https://github.com/marcingrzejszczak/jsonassert)
*   [@sbglasius](https://twitter.com/sbglasius/status/699191060669599744) Working on #gr8conf eu agenda with @glaforge - lots of fun, but too many talks, so hard to pick a great show! Thanks for all the submissions

#### Conferences and meetups

*   [Groovy & Grails Training](https://objectpartners.com/training/groovyandgrails/) , - Minneapolis, MN, February 24th - 26th, 2016
*   [GR8Day Warsaw 2016](http://www.meetup.com/Warsaw-Groovy-User-Group/events/227938015/), Warsaw - Poland, March 19th, 2016 - [CFP is open!](http://cfp.gr8conf.org/login/auth)
*   [Webcast: Seriously, Use Groovy NOW](http://www.oreilly.com/pub/e/3648?cmp=tw-prog-webcast-info-webcast_cmjrs), Online, March 29th, 2016
*   [Greach](http://greachconf.com/), Madrid - Spain, April 8th & 9th, 2016
*   [Spring I/O](http://www.springio.net/), Barcelona - Spain, May 19th - 20th, 2016
*   [GR8conf Europe & Gradle miniSummit](http://gr8conf.eu/), Copenhagen - Denmark, June 1st -3rd, 2016.
*   [Gradle Summit](http://gradlesummit.com), Palo Alto - CA, June 23rd -24th, 2016.
*   [GR8conf US](http://gr8conf.us/), Minneapolis - USA, July 27th - 29th, 2016.
*   [G3 Summit](https://g3summit.com) , Fort Lauderdale - USA, November 27th - December 1st, 2016.- [CFP is open!](https://g3summit.com/home/speaker_request)

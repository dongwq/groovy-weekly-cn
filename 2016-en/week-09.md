
# Grails Diary - Week 9 in 2016 <small>07-03-2016</small>

> original at (link)[http://grydeske.net/news/show/130]

This week has been busy with Grails releases! On the old 2.x maintenence track, version [2.5.4](https://github.com/grails/grails-core/releases/tag/v2.5.4) is out, fixing a problem with create-app and a few other issues. On the 3.0 track, [3.0.15](https://github.com/grails/grails-core/releases/tag/v3.0.15), solving a bunch of errors, including a StackOverflowError on the forward method on 404 handling. Last, on the latest branch, both version [3.1.2](https://github.com/grails/grails-core/releases/tag/v3.1.2) and [3.1.3](https://github.com/grails/grails-core/releases/tag/v3.1.3) are out, with a lot of work from the team, including upgrades to the newest groovy: 2.4.6 and the latest Spring Boot: 1.3.3\. All releases are available on [SdkMan.](http://sdkman.io/)

Jeff Scott Brown is searching for expertice in converting radeox to asciidoctor, as it seems like the Grails Documentation is the next candidate to be restyled. I think the GRails team would welcome any help for the process of updating the documentation!

Groovy is again this month doing well in the [Tiobe index,](http://www.tiobe.com/tiobe_index?page=index) at place number 17\. This is way ahead of other alternative JVM languages like Scala, Kotlyn, Frege etc. This is the 3rd. month in a row Groovy is in the top 20!

Griffon 2.6.0 has been released. The [release notes](http://griffon-framework.org/releasenotes/griffon_2.6.0.html) has all the info, including which dependencies have been upgraded, and updates to several JavaFx features.

Gradle Inc. is continuing the great work, and has the first release candidate ready for Gradle 2.12. The [release notes](https://docs.gradle.org/2.12-rc-1/release-notes), tells us we will have even faster build script compilation, ability to declare compile time only dependencies with Java plugin, and much more. The easiest way to try it out, is using [SdkMan.](http://sdkman.io/)

Craig Burke is making progres on the [client-dependencies-gradle](https://github.com/craigburke/client-dependencies-gradle) plugin, now ready in version 0.3.0, and ready to take on dependencies from bower, npm or git without installing node, npm or bower.

Steven Olsen has shared his slides on [Functional Groovy](http://slides.com/crazy4groovy/functional).

The GPars team has shared [guidelines](http://gparsdocs.de.a9sapp.eu/WebsiteStructure/index.html), for the conversion of their documentation from the old website and markdown into AsciiDoctor using the Gradle plugin. It also describes the use of Gretty to view changes locally. The new website is at [gpars.website](http://gpars.website).

["Learning Groovy"](https://leanpub.com/learninggroovy), the Leanpub book by Adam L. Davis is now 100% complete, and assumes the reader already is familiar with Java’s syntax and basic programming ideas.

The [agenda for GR8Day Warsaw](http://warsaw.gr8days.pl/#/agenda) is ready, packed with interesting talks on Ratpack, Grails, Griffon, Sshoogr, Groovy, Gradle and more. Quite impressive on a one day event! Registration is still open.

The first batch of [speakers for GR8conf EU](http://gr8conf.eu/#/speakers) is announced. Ken Kousin, who is a frequent speaker in the US, will be giving a keynote this year in Copenhagen.

#### Podcasts and Videos of Presentations

*   [Groovy Podcast Ep. 24](http://www.youtube.com/watch?v=ENraP2KtiAE) (Peter Ledbrook, Ken Kousin & Baruch Sadogursky)

#### Blogs, Articles, etc.

*   [Groovy Goodness: Customising The Groovy Compiler](http://blog.jdriven.com/2016/03/groovy-goodness-customising-the-groovy-compiler/) (Hubert Klein Ikkink aka MrHaki)
*   [Groovy Calamari - Issue 28](http://groovycalamari.com/issues/28) (Sergio del Amo)
*   [Gradle Goodness: Adding Custom Extension To Tasks](http://mrhaki.blogspot.dk/2016/03/gradle-goodness-adding-custom-extension.html) (Hubert Klein Ikkink aka MrHaki)
*   [Grails Tips: How to change the server url of a Grails 3 App?](http://sergiodelamo.es/grails-tips-how-to-change-the-server-url-of-a-grails-3-app/) (Sergio del Amo)
*   [Unit Testing URI-Based Grails Filters](https://objectpartners.com/2016/03/01/unit-testing-uri-based-grails-filters/) (Igor Shults)
*   [Grails Tips: How to change the default locale of your Grails 3 app?](http://sergiodelamo.es/grails-tips-how-to-change-the-default-locale-of-your-grails-3-app/) (Sergio del Amo)

![](http://grydeske.net/fileUploader/show/42)  

#### New Grails 3 Plugins

*   [html-cleaner](https://bintray.com/agorapulse/plugins/org.grails.plugins:html-cleaner/view) (1.0) Grails HTML Cleaner plugin
*   [grails-flyway](https://bintray.com/saw303/plugins/org.grails.plugins:grails-flyway/view) (0.2) Grails grails-flyway plugin
*   [paypal-payments](https://bintray.com/novadge/plugins/paypal-payments/view) (0.1.0) Accept and process payments with Paypal SDK

#### Updated Grails 3 Plugins

*   [grooscript](https://bintray.com/chiquitinxx/grooscript/org.grails.plugins:grooscript/view) (1.2.2) Grooscript Grails 3 Plugin
*   [jesque](https://bintray.com/ctoestreich/grails-plugins/jesque/view) (1.0.8) Grails Jesque Plugin
*   [views-gradle](https://bintray.com/grails/plugins/views-gradle/view) (1.0.4) Grails views-gradle plugin
*   [newrelic](https://bintray.com/agorapulse/plugins/org.grails.plugins:newrelic/view) (3.26.1) Grails NewRelic plugin
*   [grails-views](https://bintray.com/grails/plugins/grails-views/view) (1.0.4) Grails Views
*   [browser-detection](https://bintray.com/mathifonseca/grails-plugins/browser-detection/view) (3.1.0) Grails Browser Detection Plugin
*   [mail](https://bintray.com/grails/plugins/mail/view) (2.0.0.RC6) Grails mail plugin
*   [ember-asset-pipeline](https://bintray.com/bertramlabs/asset-pipeline/ember-asset-pipeline/view) (2.7.0) Compiles hbs or handlebars files for the asset-pipeline into the Ember.TEMPLATES cache
*   [asset-pipeline](https://bintray.com/grails/plugins/asset-pipeline/view) (3.1.0) Grails asset-pipeline plugin
*   [sass-asset-pipeline](https://bintray.com/bertramlabs/asset-pipeline/sass-asset-pipeline/view) (2.7.0)
*   [less-asset-pipeline](https://bintray.com/bertramlabs/asset-pipeline/less-asset-pipeline/view) (2.7.0) LESS Compiler for the Asset-Pipeline
*   [babel-asset-pipeline](https://bintray.com/errbuddy/plugins/babel-asset-pipeline/view) (1.4.5) Babel.js transformation for Asset-pipeline
*   [grails3-cors-interceptor](https://bintray.com/appcela/maven/grails3-cors-interceptor/view) (0.1.4) Add Cross-Origin Resource Sharing (CORS) headers for Grails 3 applications.

#### Updated Grails 2 Plugins

*   [Babel Asset-Pipeline Plugin](https://grails.org/plugin/babel-asset-pipeline) Adds babel transformation to Asset-Pipeline.
*   [Ember.js Asset-Pipeline Plugin](https://grails.org/plugin/ember-asset-pipeline) Provides Ember.js integration with asset-pipeline. Allows for handlebars precompilation as well as scaffolding for building an emberjs application.
*   [Handlebars Asset-Pipeline Plugin](https://grails.org/plugin/handlebars-asset-pipeline) Provides Handlebars precompiler support for the asset-pipeline static asset management plugin.
*   [CoffeeScript Asset-Pipeline Plugin](https://grails.org/plugin/coffee-asset-pipeline) Provides coffee-script support for the asset-pipeline static asset management plugin.
*   [SASS/SCSS Asset-Pipeline Plugin](https://grails.org/plugin/sass-asset-pipeline) Provides SASS/SCSS Compass support for the asset-pipeline static asset management plugin.
*   [LESS Asset-Pipeline Plugin](https://grails.org/plugin/less-asset-pipeline) Provides LESS support for the asset-pipeline static asset management plugin.
*   [Asset Pipeline Plugin](https://grails.org/plugin/asset-pipeline) The Asset-Pipeline is a plugin used for managing and processing static assets in Grails applications. Asset-Pipeline functions include processing and minification of both CSS and JavaScript files. It is also capable of being extended to compile custom static assets, such as CoffeeScript.
*   [Browser Detection Plugin](https://grails.org/plugin/browser-detection) This plugin helps you detect browsers, versions, language and operating systems from the request headers.
*   [Redis Session Plugin](https://grails.org/plugin/redis-database-session) Stores HTTP sessions in a Redis data store.

#### Interesting Tweets

*   [@danveloper](https://twitter.com/danveloper/status/706853417340239878) Running in the cloud isn't as simple as it used to be, and with Groovy we can adapt quickly. Excited for this talk! [https://t.co/3P2UqkwaCp](https://t.co/3P2UqkwaCp)
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/706846386910846976) @spockframework is really an amazing tool. How can one live without it?
*   [@ilopmar](https://twitter.com/ilopmar/status/706763548307955713) I'll be speaking next @gr8conf in Copenhagen #IvánOnTour2016 [https://twitter.com/gr8conf/status/706725577315618816](https://twitter.com/gr8conf/status/706725577315618816)
*   [@RalfDMueller](https://twitter.com/RalfDMueller/status/706234419124772864) Just finished upgrading all dependencies for the @GebFramework and @spockframework teaser talk @JavaLandConf
*   [@rafael_luque](https://twitter.com/rafael_luque/status/706217401810083840) BBVA Betatesters a tool built with #groovylang and #grailsfw in a banking environment [http://ow.ly/3zi8yb](http://ow.ly/3zi8yb)
*   [@gradle](https://twitter.com/gradle/status/706209203212435456) Learn how to become an advanced #Gradle build master with this hands-on course: [http://buff.ly/1SRr029](http://buff.ly/1SRr029)
*   [@sbglasius](https://twitter.com/sbglasius/status/705304575394320384) Just released v2.0.0.RC6 of the mail plugin for @grailsframework 3 [http://bit.ly/1oR5Rbs](http://bit.ly/1oR5Rbs) - major overhaul, CompileStatic, please test it.
*   [@glaforge](https://twitter.com/glaforge/status/705515863315718146) A new product from @SmartBear: an API testing engine w/ a REST API… scriptable with @ApacheGroovy [https://smartbear.com/product/ready-api/testserver/overview/](https://smartbear.com/product/ready-api/testserver/overview/)
*   [@gradle](https://twitter.com/gradle/status/706162914139447296) Did you know that #Gradle offers Advanced Gradle Fundamentals training: [http://buff.ly/1omSHTp](http://buff.ly/1omSHTp)
*   [@mittie](https://twitter.com/mittie/status/706103558127620096) <- planning for some surprises to mix into the @Groovylang talk at @JavaLandConf
*   [@waits_for_it](https://twitter.com/waits_for_it/status/705842084788334592) #groovylang is now #17 and doubling its numbers since last year [http://www.tiobe.com/tiobe_index?page=Groovy](http://www.tiobe.com/tiobe_index?page=Groovy)
*   [@domurtag](https://twitter.com/domurtag/status/705793548302548992) @pledbrook @groovypodcast I do enjoy the podcast, mostly for the @danveloper bashing
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/705767576723460098) Who the h* decided it was a good idea to show the script in the result of evaluation of script by default in groovyConsole?
*   [@pledbrook](https://twitter.com/pledbrook/status/705757557474926592) It looks like @groovypodcast is averaging ~800 downloads an episode. Wow. And thank you!
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/705745451539177476) Thanks @BenediktRitter for your work on Apache Commons! #ThankAnOpenSourceContributorFriday
*   [@rfletcherEW](https://twitter.com/rfletcherEW/status/705566667745538048) @groovypuzzlers do you have something like this? [https://gist.github.com/robfletcher/d9207087ca9665bfa0da](https://gist.github.com/robfletcher/d9207087ca9665bfa0da)
*   [@groovypuzzlers](https://twitter.com/groovypuzzlers/status/705565777508769793) OK, this is going to be the official opening clip of the #groovypuzzlers. [https://twitter.com/rlemaitre/status/705338866799087616](https://twitter.com/rlemaitre/status/705338866799087616)
*   [@GDBolinger](https://twitter.com/GDBolinger/status/705550329820020736) #grailsfw #remote work out there? Ping me. Would love to work on something cool.
*   [@danveloper](https://twitter.com/danveloper/status/705443202858360833) Don't fear #groovylang friends! Learning Ratpack copy edit phase is well underway! [https://twitter.com/groovypodcast/status/705344590589648898](https://twitter.com/groovypodcast/status/705344590589648898)
*   [@jeffscottbrown](https://twitter.com/jeffscottbrown/status/705387709792067586) Vibrant Grails User Guide seeks encounter with Radeox render engine that outputs Asciidoctor. #grailsfw #asciidoctor
*   [@bgoetzmann](https://twitter.com/bgoetzmann/status/705358872274444288) Here my project: a #grailsfw 3.1.1 app that uses grails-actuator-ui and Spring Core Security for a nice dashboard [https://bitbucket.org/bgoetzmann/odelia-gina-actuator](https://bitbucket.org/bgoetzmann/odelia-gina-actuator)
*   [@Lspacewalker](https://twitter.com/Lspacewalker/status/705129631830114304) Time travel is possible. I ask a question now and @tim_yates answers from the past via StackOverflow
*   [@Ape_PS](https://twitter.com/Ape_PS/status/705070782288777216) Deploying #grails app on #cloudfoundry is so effortless. It took me more time to write the tweet than to deploy :) @cloudfoundry #awesome
*   [@salenda](https://twitter.com/salenda/status/704994553347047424) We are pleased to keep contributing to the #groovylang and #grailsfw communities by sponsoring @gr8day_warsaw: [http://www.meetup.com/es-ES/Warsaw-Groovy-User-Group/events/227938015/?eventId=227938015](http://www.meetup.com/es-ES/Warsaw-Groovy-User-Group/events/227938015/?eventId=227938015)
*   [@TOTHENEW](https://twitter.com/TOTHENEW/status/704863809907855361) How to use closure in #Grails Programming? [http://bit.ly/1QeUKm0](http://bit.ly/1QeUKm0) #Groovy [https://t.co/MTCi6uyyDm](https://t.co/MTCi6uyyDm)
*   [@RealNickJacques](https://twitter.com/RealNickJacques/status/704736550743986176) "A full-stack developer is one who can add technical debt to any layer of the application" -My coworker
*   [@pledbrook](https://twitter.com/pledbrook/status/704701964228141057) I can’t believe I’ve only just come across this in the #spockfw user guide: [https://spockframework.github.io/spock/docs/1.0/extensions.html](https://spockframework.github.io/spock/docs/1.0/extensions.html) - lots of useful annotations.
*   [@Droidconit](https://twitter.com/Droidconit/status/704608370410561537) 6 tips to speed up your #Gradle build — Medium [http://buff.ly/1RxfllO](http://buff.ly/1RxfllO)
*   [@vasouv](https://twitter.com/vasouv/status/704430347002499072) Reading "Java Testing with Spock" by @codepipes. Am impressed by both #Groovylang and #Spock. Will start using Groovy in my projs I think...

#### Conferences and meetups

*   [GR8Day Warsaw 2016](http://www.meetup.com/Warsaw-Groovy-User-Group/events/227938015/), Warsaw - Poland, March 19th, 2016
*   [Webcast: Seriously, Use Groovy NOW](http://www.oreilly.com/pub/e/3648?cmp=tw-prog-webcast-info-webcast_cmjrs), Online, March 29th, 2016
*   [Greach](http://greachconf.com/), Madrid - Spain, April 8th & 9th, 2016
*   [Spring I/O](http://www.springio.net/), Barcelona - Spain, May 19th - 20th, 2016
*   [GR8conf Europe & Gradle miniSummit](http://gr8conf.eu/), Copenhagen - Denmark, June 1st -3rd, 2016.
*   [Gradle Summit](http://gradlesummit.com), Palo Alto - CA, June 23rd -24th, 2016.
*   [GR8conf US](http://gr8conf.us/), Minneapolis - USA, July 27th - 29th, 2016.
*   [G3 Summit](https://g3summit.com) , Fort Lauderdale - USA, November 27th - December 1st, 2016.- [CFP is open!](https://g3summit.com/home/speaker_request)


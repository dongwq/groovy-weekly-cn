
# Grails Diary - Week 20 in 2016 <small>23-05-2016</small>

> original at (link)[http://grydeske.net/news/show/138]

Welcome to this 121st edition of the Grails Diary, just 3 more and I have blogged as many editions as Burt did of the "This week in Grails" series back a few years ago, that was the inspiration for this blog series. The big topic this week is the discussion on Gradle now also supporting Kotlyn, but don't miss releases, presentations and other blogs.

Grails have a new release this week, [version 3.1.17](https://github.com/grails/grails-core/releases/tag/v3.1.7), with a couple of new features. First, there is a new REST API plugin profile, for creating plugins designed to serve REST APIs. The Application class of plugins is annotated with PluginSource, to avoid duplicate Application Loader classes generated. Finally, there is support for Hibernate 5.1, as the latest release of GORM is included.

The announcement that Gradle now also will supports build scripts written in Kotlyn have stirred a bit in the Groovy Ecosystem. You can find the announcements from [Gradle: Kotlin Meets Gradle](http://gradle.org/blog/kotlin-meets-gradle/) and from [Jetbrains: Gradle Meets Kotlin](http://blog.jetbrains.com/kotlin/2016/05/gradle-meets-kotlin) , as well as thoughts and responses from first [Dan Woods](http://danveloper.github.io/gradle-kotlin-groovy.html), then [Cédric Champeau](http://melix.github.io/blog/2016/05/gradle-kotlin.html) and also [Schalk Cronjé.](http://delivervalue.blogspot.co.uk/2016/05/about-gradle-kotlin-and-inner-fear.html) Links with titles are available in the blogs section.   
My personal opinion is that everyone should keep a decent tone in the discussion, as Gradle and all of the people at Gradle are doing a great job in building the best build tool in the JVM space. I don't see a polyglot buildscript language as a thread to the Groovy ecosystem, as I think the ecosystem consists of a very pleasant programming language, along with a long range of excellent frameworks for apps, testing and all kinds of tasks. If you attend my presentation at GR8Conf EU in a week and a half, I'll describe some of them, and how they are now used in the team I joined a year ago.

Not to forget in all of the Kotlyn fuzz, [Gradle 2.14 RC1](https://discuss.gradle.org/t/gradle-2-14-rc-1-is-now-available-for-testing/17635) is out, with a lot of new improvements. Performance is again improved, the deamon has been upgraded to be more robust and is now suited even for ci servers, IDEA support for Play projects and Java 6 is now officially deprecated. Some of the core plugins have been [partially converted to JAVA](https://discuss.gradle.org/t/gradle-plugins-converted-from-groovy-to-java/17634), but it appears it also happened by adding CompileStatic to some of the Groovy classes.

If you are working with ReactJS and Grails, the [Grails/React Starter project](https://github.com/ZacharyKlein/grails-react-starter) has been updated

In presentation news, Ivan Lopez have given a presentation at JavaCro on [From Java to Groovy: Adventure Time!](http://www.slideshare.net/ilopmar/javacro-2016-from-java-to-groovy-adventure-time) and Danny Hyun at JEEConf on [Rapid Java Web Application Development with Ratpack](http://danhyun.github.io/2016-jeeconf-rapid-ratpack-java/) ([pdf](https://danhyun.github.io/2016-jeeconf-rapid-ratpack-java/notes.pdf)) Manning have also shared a few slides on [Why You Should Get On Board with Spock](http://www.slideshare.net/ManningBooks/why-you-should-get-on-board-with-spock).

#### Podcasts and Videos of Presentations

*   [Groovy Podcast Special Edition: Ryan Verderwerf](https://www.youtube.com/watch?v=oeQY4NsG3XI) (Baruch Sadogursky)
*   [Grails Quickcast #3: Multi-Project Builds](https://dzone.com/articles/oci-and-dzone-present-a-grails-quickcast-3-multi-p) (Graeme Rocker)

#### Blogs, Articles, etc.

*   [Kotlin Meets Gradle](http://gradle.org/blog/kotlin-meets-gradle/) (Chris Beams)
*   [Gradle Meets Kotlin](http://blog.jetbrains.com/kotlin/2016/05/gradle-meets-kotlin) (Hadi Hariri)
*   [Gradle, Kotlin, and the Future of Groovy](http://danveloper.github.io/gradle-kotlin-groovy.html) (Dan Woods)
*   [Gradle and Kotlin, a personal perspective](http://melix.github.io/blog/2016/05/gradle-kotlin.html) (Cédric Champeau)
*   [About Gradle, Kotlin and Inner Fear.](http://delivervalue.blogspot.co.uk/2016/05/about-gradle-kotlin-and-inner-fear.html) (Schalk Cronjé)
*   [Groovy Calamari - Issue 36](http://groovycalamari.com/issues/36) (Sergio del Amo)
*   [Groovy Goodness: Creating Files And Directories With Nice DSL Using FileTreeBuilder](http://mrhaki.blogspot.dk/2016/05/groovy-goodness-creating-files-and.html) (Hubert Klein Ikkink aka MrHaki)
*   [Using Spring-Boot 1.4 testing features with Spock](http://groovy-coder.com/?p=111) (Kevin Wittek)
*   [All Things Groovy](https://www.linkedin.com/pulse/all-things-groovy-s%C3%B8ren-glasius?trk=mp-author-card) (Søren Glasius)

[![](http://grydeske.net/fileUploader/show/43)](http://gr8conf.eu/#/)  

#### New Grails 3 Plugins

*   [i18n-javascript](https://bintray.com/salex772/plugins/i18n-javascript/view) (0.4.1) Render all Grails i18n messages to Javascript
*   [grails-melody-plugin](https://bintray.com/sergiomichels/plugins/grails-melody-plugin/view) (1.59.0) Integrate JavaMelody monitoring into Grails application.

#### Updated Grails 3 Plugins

*   [force-ssl](https://bintray.com/bertramlabs/grails3-plugins/force-ssl/view) (3.0.2) Creates a simple annotation to mark controller/actions as SSL restricted and performs the appropriate redirect.
*   [http-requests-grails](https://bintray.com/budjb/maven/http-requests-grails/view) (1.0.0) The HTTP Requests Plugin provides the http-requests library and artefacts for filters and converters.
*   [grails-twilio](https://bintray.com/novadge/plugins/grails-twilio/view) (0.1.1) Provides SMS sending capabilities to a Grails application.
*   [swagger4jaxrs](https://bintray.com/donald-jackson/plugins/swagger4jaxrs/view) (3.0.2) Grails swagger4jaxrs plugin
*   [grails-views](https://bintray.com/grails/plugins/grails-views/view) (1.0.11) Grails Views
*   [views-gradle](https://bintray.com/grails/plugins/views-gradle/view) (1.0.11) Grails views-gradle plugin
*   [grails3-uploadr](https://bintray.com/pankajtandon/plugins/grails3-uploadr/view) (3.0.1) Plugin to upload multiple files from a web page. Uses HTML5 and CSS3
*   [redis-gorm](https://bintray.com/grails/plugins/redis-gorm/view) (5.0.7) GORM - Grails Data Access Framework
*   [neo4j](https://bintray.com/grails/plugins/neo4j/view) (5.0.7) GORM - Grails Data Access Framework
*   [mongodb](https://bintray.com/grails/plugins/mongodb/view) (5.0.7) GORM for MongoDB
*   [hibernate5](https://bintray.com/grails/plugins/hibernate5/view) (5.0.7) GORM - Grails Data Access Framework
*   [hibernate4](https://bintray.com/grails/plugins/hibernate4/view) (5.0.7) GORM - Grails Data Access Framework
*   [hibernate3](https://bintray.com/grails/plugins/hibernate3/view) (5.0.7) GORM - Grails Data Access Framework
*   [cassandra](https://bintray.com/grails/plugins/cassandra/view) (5.0.7) GORM - Grails Data Access Framework

#### Updated Grails 2 Plugins

*   [Facebook SDK Plugin](https://grails.org/plugin/facebook-sdk) The Facebook SDK Plugin allows your Grails application to use the Facebook Platform and develop Facebook apps on Facebook.com or on web sites (with Facebook Connect). It is a port of the official Facebook PHP SDK to Grails 2.0.
*   [Websocket Chat Plugin](https://grails.org/plugin/wschat) Default WebSocket Multi-chat room plugin, supports Admin privilages, kicking banning users. Webcam support for chrome/firefox. WebRTC (audio/video & screen) support 0.24+
*   [Grails DataTables Plugin](https://grails.org/plugin/grails-datatables) This plugin allows you to quickly add feature-rich tables to your Grails application. It uses the excellent DataTables plugin for jQuery created by SpryM
*   [Smart Case Plugin](https://grails.org/plugin/smart-case) Provides an easy way to convert between cases for Strings and variable names
*   [Grails Cloudinary Plugin](https://grails.org/plugin/cloudinary) Simplifies the usage of the cloudinary service at http://cloudinary.com

#### Interesting Tweets

*   [@TOTHENEW](https://twitter.com/TOTHENEW/status/734763879364988928) DON'T MISS THIS! @hseth - Our #grailsfw champ will be delivering a session on "THE GR8 ROAD TO #FAME" at @gr8conf [https://t.co/ZKDhuy0eyo](https://t.co/ZKDhuy0eyo)
*   [@GR8ConfUS](https://twitter.com/GR8ConfUS/status/734747077327134723) Excited that @graemerocher will be returning as our opening keynote speaker at @GR8ConfUS 2016! [http://ow.ly/FtUD300p2jD](http://ow.ly/FtUD300p2jD) #grailsfw
*   [@ysb33r](https://twitter.com/ysb33r/status/734719823645675520) It would be nice if there was a standard lifecycle task in #gradle to hook documentation into. Today use assemble, check or build?
*   [@gr8conf](https://twitter.com/gr8conf/status/734717913215737857) Join the #gr8conf discussion on the @grailsframework @SlackHQ channel here: [http://bit.ly/1NGHdpO](http://bit.ly/1NGHdpO) @ApacheGroovy @gradle
*   [@ar_gou](https://twitter.com/ar_gou/status/734703799051247616) I find #groovylang very appealing,easy to learn with a very consistent ecosystem.I don't get why other jvm langs are getting more advertised
*   [@kenkousen](https://twitter.com/kenkousen/status/734545521101131776) Also, I will be interviewing @CedricChampeau for the @groovypodcast this week and this might come up [https://twitter.com/CedricChampeau/status/734488449131122689](https://twitter.com/CedricChampeau/status/734488449131122689)
*   [@domurtag](https://twitter.com/domurtag/status/734510466752491520) Great article from @CedricChampeau about gradle's kotlin support and the future for #groovylang [http://melix.github.io/blog/2016/05/gradle-kotlin.html](http://melix.github.io/blog/2016/05/gradle-kotlin.html)
*   [@domurtag](https://twitter.com/domurtag/status/734504564745965569) @CedricChampeau very interesting post. Anyone who thinks you're not a suitable leader/member of groovy community is either a fool or a troll
*   [@RyanVanderwerf](https://twitter.com/RyanVanderwerf/status/734501135919112193) Thanks for the in depth article. Please don't leave the project because of ruffled feathers of others! [https://twitter.com/CedricChampeau/status/734488449131122689](https://twitter.com/CedricChampeau/status/734488449131122689)
*   [@ApacheGroovy](https://twitter.com/ApacheGroovy/status/734451550685368320) And the #groovylang website is now back online! Thanks for your patience, and sorry again for the inconvenience!
*   [@ilopmar](https://twitter.com/ilopmar/status/734272137138163712) . @JavaCro has been the 6th stop of #IvánOnTour2016\. In less than 2wks I'll be in Copenhagen for @gr8conf.Can't wait to see a lot of friends
*   [@ysb33r](https://twitter.com/ysb33r/status/734130609099001856) @rfletcherEW i have to say after using it that Spock still rules.
*   [@RalfDMueller](https://twitter.com/RalfDMueller/status/734107835777306624) Any Interest in a Grails 3 Course [http://therealdanvega.com/blog/2016/05/20/grails-3-course-interest](http://therealdanvega.com/blog/2016/05/20/grails-3-course-interest) via @therealdanvega
*   [@alvaro_sanchez](https://twitter.com/alvaro_sanchez/status/733602333574074370) Very well put together. Thinking that @gradle build scripts is what drives adoption to #groovylang is very naive [https://twitter.com/danveloper/status/733493061905350657](https://twitter.com/danveloper/status/733493061905350657)
*   [@sdkmanager](https://twitter.com/sdkmanager/status/733355369041408000) SDKMAN 4.0.36 rolling out. Fixes [https://github.com/sdkman/sdkman-cli/issues/425](https://github.com/sdkman/sdkman-cli/issues/425)
*   [@glaforge](https://twitter.com/glaforge/status/733323052856029184) @cedricchampeau @jbaruch @hans_d why not spend time optimizing Groovy static compilation in the context of Gradle? It’ll help both projects
*   [@jeffscottbrown](https://twitter.com/jeffscottbrown/status/733281475974430720) The team at @ObjectComputing keeps cranking out the releases… #grailsfw [https://twitter.com/grailsframework/status/733257189868077056](https://twitter.com/grailsframework/status/733257189868077056)
*   [@therealdanvega](https://twitter.com/therealdanvega/status/733133757671178241) My Complete Apache Groovy course is sitting at about 13 hours of awesome content right now #groovylang [http://www.learnapachegroovy.com](http://www.learnapachegroovy.com)
*   [@ysb33r](https://twitter.com/ysb33r/status/733071369450192898) For all you folks that worked on @ratpackweb - you rock.
*   [@Lspacewalker](https://twitter.com/Lspacewalker/status/733026471002972163) On my way to @jeeconf to talk about @ratpackweb #ratpackfw ?
*   [@groovypuzzlers](https://twitter.com/groovypuzzlers/status/733021577151840256) BOOM! [https://t.co/smHbIml2nI](https://t.co/smHbIml2nI)
*   [@craigburke1](https://twitter.com/craigburke1/status/732909718889504768) Very cool. I don't know what this means for #groovylang. Will Groovy still be officially supported in 3.0? @gradle [https://twitter.com/gradle/status/732757721343217664](https://twitter.com/gradle/status/732757721343217664)
*   [@marc0der](https://twitter.com/marc0der/status/732867539798216704) Finally getting to play with #sshoogr in the real world and SO impressed. Well done @codingandrey! [https://github.com/aestasit/sshoogr](https://github.com/aestasit/sshoogr)
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/732834583549489153) #Kotlin meets #gradle [http://bit.ly/25aWhUi](http://bit.ly/25aWhUi) And for those who worry, no, we're not dropping #groovylang support.
*   [@breskeby](https://twitter.com/breskeby/status/732289341226127360) @DailyGradle or “gradle help —task <taskname>”</taskname>

#### Conferences and meetups

*   [Pittsburgh Groovy Programming: Building Android Apps with Gradle and Groovy](http://www.meetup.com/Pittsburgh-Groovy-Programming/events/230952852/), Pittsburgh, PA, May 26th, 2016.
*   [GR8conf Europe & Gradle Event](http://gr8conf.eu/), Copenhagen - Denmark, June 1st -3rd, 2016.
*   [Gr8Ladies Gr8Workshop](https://www.eventbrite.com/e/gr8ladies-gr8workshop-registration-25219881344), Minneapolis, MN, June 18th, 2016.
*   [Gradle Summit](http://gradlesummit.com), Palo Alto - CA, June 23rd -24th, 2016.
*   [GR8conf US](http://gr8conf.us/), Minneapolis - USA, July 27th - 29th, 2016.
*   [G3 Summit](https://g3summit.com) , Fort Lauderdale - USA, November 27th - December 1st, 2016.- [CFP is open!](https://g3summit.com/home/speaker_request)

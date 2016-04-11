
# Grails Diary - Week 8 in 2016 <small>29-02-2016</small>

> original at (link)[http://grydeske.net/news/show/129]

Groovy on Android seems to be picking up adoption! Andrew Reitz har released version 0.3.9 of the gradle-groovy-android-plugin enabling users to program Andrid apps in Groovy. This release deals with the interoperatability of tha Java and Groovy compilation. It is available on [Bintray](https://bintray.com/groovy/gradle-plugins/gradle-groovy-android-plugin/0.3.9!) On Stack overflow, you should annotate your question with `groovy-android`.

If you are new to Groovy, Guillaume Laforge answer where you could start in this [quora.com](https://www.quora.com/I-am-a-complete-newbie-to-Groovy-Where-can-I-find-more-stuff-on-Groovy-like-some-tutorials-books-and-any-interactive-learning-aid-for-Groovy-beginners/answer/Guillaume-Laforge?share=0f0420fd) answer.

On the Groovy mailinglist, there has been a discussion on linking to blogs for documentation, especially for the blogs of MrHaki. As blogs does not originate from ASF, this could be seen as a problem, but MrHaki is solution oriented: "In the nearby future I certainly want to contribute to adding snippets to the existing Groovydoc sources." The full thread can be found [here.](http://www.groovy-lang.org/mailing-lists.html#nabble-td5731382i10|a5731443) This could be seen as a great opportunity for new contributions to Groovy: updating the documentation with samples from Groovy Goodness.

Graeme has added some [nice documentation](http://grails.github.io/grails-views/latest/) (not just because it is in AsciiDoctor format), to the JSON views available from Grails 3.1

Geb has been released with a bugfix [version 0.13.1](https://groups.google.com/forum/#!topic/geb-user/1JIquhlk8gs), handling a regression from 0.13.0, and a couple of concurrency issues, including one that speeds up tests run simultaneously.

In 2015, Iván López visited a large number of conferences, with excellent talks on Groovy, Spock and other topics. This year, the #IvánOnTour2016 caravan is rolling again! Iván has shared [slides](http://www.slideshare.net/ilopmar/confoo-2016-mum-i-want-to-be-a-groovy-fullstack-developer) and [code](https://github.com/ilopmar/contest) for "Fullstack Groovy Developer" and [slides](http://www.slideshare.net/ilopmar/confoo-2016-metaprogramming-with-groovy) and [code](https://github.com/ilopmar/confoo2016-metaprograming-with-groovy) for "Metaprogramming with Groovy" both talks given at the ConFoo conference in Montreal.

Baruch hinted strongly about a couple of [great surprises](https://twitter.com/groovypuzzlers/status/704351974284611584) on Greachconf and GR8Conf EU. That is all I will tell here ;) But I think it is going to be Groovy!

If you are more fluent in Italian or Japanese than in English, I'm sorry for not advertising more for the translations of the Grails Diary! You can find the Italian translation at [bmeweb.it/blog/](http://www.bmeweb.it/blog/) thanks to the great crew at Bmeweb. The Japanese translation is available at [grails.jp](http://grails.jp/news/index.html) thanks to [T.Yamamoto](https://twitter.com/tyama)

#### Blogs, Articles, etc.

*   [Ratpack as a Lightweight Static Content Server](https://danveloper.github.io/ratpack-as-a-lightweight-static-content-server.html) (Dan Woods)
*   [Continuous Build: is it time to start using this by default?](http://gradle.org/continuous-build-time-start-using-default/) (Sterling Greene)
*   [JSON Assert lib released](http://toomuchcoding.blogspot.com/2016/02/json-assert-lib-released.html) (Marcin Grzejszczak)
*   [Gradle Goodness: Lazy Task Properties](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-lazy-task-properties.html) (Hubert Klein Ikkink aka MrHaki)
*   [Gradle Goodness: Methods Generated For Setting Task Properties](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-methods-generated.html) (Hubert Klein Ikkink aka MrHaki)
*   [Gradle Goodness: Inter-Project Artifact Dependencies](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-inter-project-artifact.html) (Hubert Klein Ikkink aka MrHaki)
*   [JWT, the walking dead, of Spring Security REST for Grails plugin](http://sergiodelamo.es/jwt-the-walking-dead-of-spring-security-rest-for-grails-plugin/) (Sergio del Amo)
*   [How to use a Trait to encapsulate Spring Security Core functionality in a Grails 3 App?](http://sergiodelamo.es/how-to-use-a-trait-to-encapsulate-spring-security-core-functionality-in-a-grails-3-app/) (Sergio del Amo)
*   [Grails Tips: How to change the default port of a Grails 3 App](http://sergiodelamo.es/grails-tips-how-to-change-the-default-port-of-a-grails-3-app/) (Sergio del Amo)
*   [Gradle Goodness: Create Objects Using DSL With Domain Object Containers](https://dzone.com/articles/gradle-goodness-create-objects-using-dsl-with-doma) (Hubert Klein Ikkink aka MrHaki)
*   [How to use Spring Security Core to Secure you Grails 3 App?](http://sergiodelamo.es/how-to-use-spring-security-core-to-secure-you-grails-3-app/) (Sergio del Amo)
*   [How to log SQL statements in a Grails 3 app](http://sergiodelamo.es/log-sql-grails-3-app/) (Sergio del Amo)
*   [Groovy Calamari - Issue 27](http://groovycalamari.com/issues/27) (Sergio del Amo)
*   [Grails Tips: How to change the default port where your Grails App runs?](http://sergiodelamo.es/grails-tips-how-to-change-the-default-port-where-your-grails-app-runs/) (Sergio del Amo)
*   [Is Scala on the Way Out?](https://www.linkedin.com/pulse/scala-way-out-owen-rubel) (Owen Rubel)

#### New Grails 3 Plugins

*   [redis](https://bintray.com/ctoestreich/grails-plugins/redis/view) (2.0.4) Grails Redis plugin
*   [elasticsearch](https://bintray.com/puneetbehl/plugins/elasticsearch/view) (1.0.0) Elasticsearch is a search server based on Lucene. It provides a distributed, multitenant-capable full-text search engine with an HTTP web inter?
*   [novamail](https://bintray.com/novadge/plugins/novamail/view) (0.1.0) The Novamail plug-in provides e-mail sending and retrieving capabilities to a Grails application. It is also capable of sending emails asynchro?
*   [grails-twilio](https://bintray.com/novadge/plugins/grails-twilio/view) (0.1.0) Provides SMS sending capabilities to a Grails application.

#### Updated Grails 3 Plugins

*   [boselecta](https://bintray.com/vahid/maven/boselecta/view) (3.0.3) Websocket autocomplete/ multi dependency selection plugin for grails 3
*   [cookie-session](https://bintray.com/benlucchesi/maven/cookie-session/view) (3.0.1) Grails cookiesession plugin
*   [ajaxdependancyselection](https://bintray.com/vahid/maven/ajaxdependancyselection/view) (1.1) Grails ajaxdependancyselection plugin
*   [angular-template-asset-pipeline](https://bintray.com/craigburke/asset-pipeline/angular-template-asset-pipeline/view) (2.2.7) AngularJS Templates for Asset Pipeline 2.0
*   [quartz](https://bintray.com/grails/plugins/quartz/view) (2.0.8) Grails quartz plugin
*   [iCalendar](https://bintray.com/saw303/plugins/org.grails.plugins:iCalendar/view) (0.5.2) Grails iCalendar plugin
*   [redis-gorm](https://bintray.com/grails/plugins/redis-gorm/view) (5.0.2) GORM - Grails Data Access Framework
*   [views-gradle](https://bintray.com/grails/plugins/views-gradle/view) (1.0.3) Grails views-gradle plugin
*   [grails-views](https://bintray.com/grails/plugins/grails-views/view) (1.0.3) Grails Views
*   [neo4j](https://bintray.com/grails/plugins/neo4j/view) (5.0.2) GORM - Grails Data Access Framework
*   [mongodb](https://bintray.com/grails/plugins/mongodb/view) (5.0.2) GORM for MongoDB
*   [hibernate5](https://bintray.com/grails/plugins/hibernate5/view) (5.0.2) GORM - Grails Data Access Framework
*   [hibernate4](https://bintray.com/grails/plugins/hibernate4/view) (5.0.2) GORM - Grails Data Access Framework
*   [hibernate3](https://bintray.com/grails/plugins/hibernate3/view) (5.0.2) GORM - Grails Data Access Framework
*   [cassandra](https://bintray.com/grails/plugins/cassandra/view) (5.0.2) GORM - Grails Data Access Framework

#### New Grails 2 Plugins

*   [Favourite Plugin](https://grails.org/plugin/favourites) Adds support for favourites. Mark up any of your domain classes as having favourites.

#### Updated Grails 2 Plugins

*   [CodeNarc plugin](https://grails.org/plugin/codenarc) Runs CodeNarc static analysis rules for Groovy source.
*   [iCalendar Plug-in](https://grails.org/plugin/ic-alendar) This plugin contains a builder to easily convert your event into the iCalendar format. The plugin hooks replaces each render method that uses the contentType 'text/calendar'.
*   [AngularJS Template Asset-Pipeline Plugin](https://grails.org/plugin/angular-template-asset-pipeline) Provides AngularJS template support for the asset-pipeline static asset management plugin.
*   [Favourite Plugin](https://grails.org/plugin/favourites) Adds support for favourites. Mark up any of your domain classes as having favourites.
*   [JavaMelody Grails Plugin](https://grails.org/plugin/grails-melody) Integrate JavaMelody Monitoring into grails application.
*   [Redis Session Plugin](https://grails.org/plugin/redis-database-session) Stores HTTP sessions in a Redis data store.
*   [Grails Application Version Update Plugin](https://grails.org/plugin/version-update) Provides a more friendly way to update your application or plugin version.
*   [Ajax Dependancy Selection Plugin](https://grails.org/plugin/ajaxdependancyselection) Defines next auto completion/selection form field values ensuring it is bound on previous auto completed/selected form field. This can be used on two or more objects of hasMany and belongsTo. Provides: g:autocomplete, g:autoCompletePrimary, g:autoCompleteSecondary, g:autoCompleteSecondaryNR, g:selectPrimary, g:selectSecondary , g:selectSecondaryNR & g:selectController. g:selectAutoComplete and g:selectPrimaryNR. Now also supporting 1 object with multiple dependencies.

#### Interesting Tweets

*   [@sdelamo](https://twitter.com/sdelamo/status/704390626608091136) Kudos to @andrewreitz_ he is pushing the #groovylang #android project fantastically The 0.3.9 release is an example [https://github.com/groovy/groovy-android-gradle-plugin/releases/tag/RELEASE_0_3_9](https://github.com/groovy/groovy-android-gradle-plugin/releases/tag/RELEASE_0_3_9)
*   [@jdriven_nl](https://twitter.com/jdriven_nl/status/704178820333465604) Ratpacked: Running With LiveReload Using Gradle [http://dlvr.it/KdxpCD](http://dlvr.it/KdxpCD) #Gradle #Ratpack
*   [@pledbrook](https://twitter.com/pledbrook/status/704011116163239936) Here’s how I tested that #lazybones works with authenticated proxies: [https://github.com/pledbrook/lazybones/commit/359c1f8b6ad1a3d51d0621105a21bf101508102d#diff-5b686fa89ece151982561f56cea76de5R18](https://github.com/pledbrook/lazybones/commit/359c1f8b6ad1a3d51d0621105a21bf101508102d#diff-5b686fa89ece151982561f56cea76de5R18) (using LittleProxy)
*   [@gradle](https://twitter.com/gradle/status/703988603207225344) "Read this InfoQ article called ""When did Gradle Get So Hot?"" here:[http://buff.ly/1WqwWwY](http://buff.ly/1WqwWwY)"
*   [@aalmiray](https://twitter.com/aalmiray/status/703519179991883777) #asciidoctor, #jbake, #gradle, #jmh, #jsr377, #jsilhouette. These are some of the topics to hack on during #hackergarten at @javaland
*   [@evoljoh](https://twitter.com/evoljoh/status/703446087646863361) @smartthings uses @ApacheGroovy, feeling right at home. Thanks @yaimavaldivia
*   [@gradle](https://twitter.com/gradle/status/703310096575680512) Learn about: #Gradle Daemon Support for Faster Compilation here:[http://buff.ly/20CGUMQ](http://buff.ly/20CGUMQ)
*   [@marcinerdmann](https://twitter.com/marcinerdmann/status/703293753977643008) Let's see if I can pull off getting a PR accepted into @spockframework after having two beers: [https://github.com/spockframework/spock/pull/571](https://github.com/spockframework/spock/pull/571)
*   [@andrewreitz_](https://twitter.com/andrewreitz_/status/703270806021734400) To follow in @CedricChampeau's footsteps with #ThankAnOpenSourceContributorFriday I'd like to thank him for the groovy-android-plugin.
*   [@gradle](https://twitter.com/gradle/status/703264188160991233) Check out this Reddit post of #Gradle tasks that make your life easier:[http://buff.ly/20CGOVC](http://buff.ly/20CGOVC)
*   [@aalmiray](https://twitter.com/aalmiray/status/703249071998418948) procrastination is over, unit test chapter has been added to the #griffon guide [https://github.com/griffon/griffon/commit/fc525f8130d7c9c12afa92e06b8f080ed1ef0440](https://github.com/griffon/griffon/commit/fc525f8130d7c9c12afa92e06b8f080ed1ef0440)
*   [@CedricChampeau](https://twitter.com/CedricChampeau/status/703216851162161153) Thanks @the_antlr_guy for providing us with a rock solid parser library! #ThankAnOpenSourceContributorFriday
*   [@greachconf](https://twitter.com/greachconf/status/703212953001201666) Remember to get your tickets before it's too late! [http://greachconf.com/#tickets](http://greachconf.com/#tickets) #greach #groovylang #grailsfw #gradle
*   [@alvaro_sanchez](https://twitter.com/alvaro_sanchez/status/703160447361363968) Very nice post by @sdelamo on using @SpringSecurity REST plugin for @grailsframework: [http://sergiodelamo.es/how-to-secure-your-grails-3-api-with-spring-security-rest-for-grails/](http://sergiodelamo.es/how-to-secure-your-grails-3-api-with-spring-security-rest-for-grails/) #grailsfw #groovylang
*   [@gradle](https://twitter.com/gradle/status/702947761415651328) The #Gradle #Docker plugin now allows you to copy files to a container (with Docker 1.8+) - grab it at:[http://buff.ly/1oI5q3q](http://buff.ly/1oI5q3q)
*   [@pledbrook](https://twitter.com/pledbrook/status/702915873678426112) Thanks to @betamaxtest, I discovered a configurable proxy server for the JVM that uses Netty: LittleProxy - [https://github.com/adamfisk/LittleProxy](https://github.com/adamfisk/LittleProxy)
*   [@JennStrater](https://twitter.com/JennStrater/status/702630302804410368) Brought my #gr8conf beer to OPI beer club #opirules [https://t.co/PWnyXujiLW](https://t.co/PWnyXujiLW)
*   [@craigburke1](https://twitter.com/craigburke1/status/702588363275161600) Version 0.2.0 of gradle Client Dependencies #Gradle Plugin (npm/bower). It’s getting there. Feedback welcome. [https://github.com/craigburke/client-dependencies-gradle](https://github.com/craigburke/client-dependencies-gradle)
*   [@gradle](https://twitter.com/gradle/status/702569494313615360) Get the free eBook from O'Reilly: Building and Testing With #Gradle: [http://buff.ly/1oI5iRm](http://buff.ly/1oI5iRm)
*   [@musketyr](https://twitter.com/musketyr/status/702568632937795584) I think @ApacheGroovy static compilation should be triggered automatically based on some file ext chosen (i.e. .sgr)
*   [@ilopmar](https://twitter.com/ilopmar/status/701982581819056129) It seems that @sdelamo is becoming the new @mrhaki. A lot of great articles about @grailsframework 3 :-) [https://twitter.com/JacobAae/status/701888032895541248](https://twitter.com/JacobAae/status/701888032895541248)

#### Conferences and meetups

*   [London Groovy & Grails User Group: There's so much more to Ratpack than non-blocking](http://www.meetup.com/london-ggug/events/228577336/) , London - UK, March 1st, 2016
*   [GR8Day Warsaw 2016](http://www.meetup.com/Warsaw-Groovy-User-Group/events/227938015/), Warsaw - Poland, March 19th, 2016 - [CFP is open!](http://cfp.gr8conf.org/login/auth)
*   [Webcast: Seriously, Use Groovy NOW](http://www.oreilly.com/pub/e/3648?cmp=tw-prog-webcast-info-webcast_cmjrs), Online, March 29th, 2016
*   [Greach](http://greachconf.com/), Madrid - Spain, April 8th & 9th, 2016
*   [Spring I/O](http://www.springio.net/), Barcelona - Spain, May 19th - 20th, 2016
*   [GR8conf Europe & Gradle miniSummit](http://gr8conf.eu/), Copenhagen - Denmark, June 1st -3rd, 2016.
*   [Gradle Summit](http://gradlesummit.com), Palo Alto - CA, June 23rd -24th, 2016.
*   [GR8conf US](http://gr8conf.us/), Minneapolis - USA, July 27th - 29th, 2016.
*   [G3 Summit](https://g3summit.com) , Fort Lauderdale - USA, November 27th - December 1st, 2016.- [CFP is open!](https://g3summit.com/home/speaker_request)

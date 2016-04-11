
# Grails Diary - Week 4 in 2016 <small>01-02-2016</small>

> original at (link)[http://grydeske.net/news/show/126]

Grails 3 is really picking up steam! This week there are no new or updated Grails 2 plugins, but a lot of both for Grails 3.

Biggest news this week must be the release of [Grails 3.1](https://github.com/grails/grails-core/releases/tag/v3.1.0). The manual has a section on [What's new in Grails 3.1 Guide](http://grails.github.io/grails-doc/3.1.x/guide/introduction.html#whatsNew31), and the highlights are the improvements to profiles (publishing and repositories), the new REST API and AngularJS Profiles, the GORM 5 suite and plugins for publishing plugins. Graeme visited the [Groovy Podcast](https://www.youtube.com/watch?v=ZxExU0lbMUI&feature=youtu.be) discussing the history of Grails and the new 3.1 release

Burt Beckwith pointed to an article on [performance issues with Hibernate when the logging settings were changed](https://plumbr.eu/blog/io/how-we-accidentally-doubled-our-jdbc-traffic-with-hibernate). It is worth a read, as Grails/GORM for most of the drivers use Hibernate under the hood

The Groovy team is discussing the roadmap for the next major release on the Groovy mailing list, and the wording of features. There are much work to be done, but also a steady stream of contributions.

Power blogger Mr Haki (if you don't believe me, check the blog section) has updated four of his notebooks on leanpub: [Groovy Goodness](http://mrhaki.blogspot.dk/2016/02/groovy-goodness-notebook-is-updated.html) [Gradle Goodness](http://mrhaki.blogspot.dk/2016/02/gradle-goodness-notebook-updated.html) [Spocklight](http://mrhaki.blogspot.dk/2016/02/spocklight-notebook-is-updated.html) and [Grails Goodness](http://mrhaki.blogspot.dk/2016/02/grails-goodness-notebook-updated.html)

Craig Burke has shared the [slides](http://www.craigburke.com/gradle-intro/) and [code](https://github.com/craigburke/gradle-intro) to go with the video for his "All About Gradle" talk in the video section.

Phill Barber has tried to do a comparison of [Ratpack and Dropwizard](http://phillbarber.blogspot.com/2016/01/choosing-between-ratpack-and-dropwizard.html), and have measured performance and other metrics, and have Ratpack as his teams new framework.

Peter Ledbrook is the instructor on a couple of [new courses on Groovy and Grails](http://blog.cacoethes.co.uk/groovyandgrails/a-new-approach-to-training), where instead of intensive one or more day training, the timespan is longer with feedback gradually. I'm interested in how Peters experiences with this style is, as it sounds promissing for long term retention of the material.

After Spring One dropped the 2GX part, New No Fluff Just Stuff is instead having a dedicated Groovy, Grails and Gradle conference, the [G3 Summit](https://g3summit.com) this year in Fort Lauderdale late november/early december.

Greach, the Spanish Groovy conference, has published [the agenda](http://greachconf.com/agenda/), with lots of interesting talks and speakers. I'll present a talk on Geb, and is really looking forward to visiting Spain again. Last year was a great experience! And the conference has extended the [early bird ticket](http://greachconf.com/#tickets) discount, with a few tickets, now that the agenda is out, - but hurry, there a only a few left!

The call for paper is still [open](http://cfp.gr8conf.org/login/auth), for both GR8Conf EU, GR8Conf US and a new mini conference in Warsaw, the GR8Day Warsaw on March 19th.

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

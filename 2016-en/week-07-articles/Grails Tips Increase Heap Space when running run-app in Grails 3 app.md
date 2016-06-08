# Grails Tips: Increase Heap Space when running run-app in Grails 3 app

> original at (link)[http://sergiodelamo.es/grails-tips-increase-heap-space-when-running-grails-run-app/]     
I recently need too increase my heap space while executing   

		grails run-app

The solution was, as many times, in [stack overflow](http://stackoverflow.com/questions/29812691/grails-3-0-x-how-to-increase-heap-space-when-using-grails-run-app)

Add to your build.gradle

		bootRun {
    		jvmArgs = ['-Xmx2048m']
		}
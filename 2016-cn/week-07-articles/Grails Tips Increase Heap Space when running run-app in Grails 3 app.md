# Grails Tips: Increase Heap Space when running run-app in Grails 3 app

# Grails小窍门：在Grails 3中如何增加堆空间


> (原文档链接)[http://sergiodelamo.es/grails-tips-increase-heap-space-when-running-grails-run-app/]     


I recently need too increase my heap space while executing   

当运行`grails run-app`命令的时候我需要增加堆空间   

		grails run-app

The solution was, as many times, in stack overflow

解决方案跟以前一样在[stack overflow](http://stackoverflow.com/questions/29812691/grails-3-0-x-how-to-increase-heap-space-when-using-grails-run-app)，

Add to your build.gradle

把下面的语句添加到你的`build.gradle`文件中   

		bootRun {
    		jvmArgs = ['-Xmx2048m']
		}
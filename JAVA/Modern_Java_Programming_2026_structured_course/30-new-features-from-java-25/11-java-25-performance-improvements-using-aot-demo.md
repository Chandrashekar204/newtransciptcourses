# 30.11 — [JAVA 25] Performance improvements using AOT - Demo

> Section 30: New features from Java 25

[00:00] To see the demo of performance improvements.
[00:03] With Aot.
[00:04] We don't have to create a Spring boot application from scratch.
[00:07] Instead, we can leverage an official Spring Boot application that is provided by the Spring Boot Framework
[00:14] team inside Google.
[00:15] If you search for Spring Boot Pet Clinic, you're going to get a GitHub repo.
[00:19] Let me open the same.
[00:21] Spring Pet Clinic is an official web application provided by the Spring and Spring Boot Team, which
[00:27] is developed based upon Java Spring and Spring Boot.
[00:31] If you scroll down on this page, they have given instructions on how to run these application.
[00:36] So first you need to clone these application into your local system by running this git command.
[00:42] So please make sure you are running this command and navigate into these spring Pet Clinic.
[00:48] So once you navigate into these application folder, you can package this application as a jar by executing
[00:55] this Maven command.
[00:56] So this command is similar to what I have provided in the slide.
[01:01] You can either use Mvn clean package command if you install the Maven inside your local system.
[01:08] Otherwise, if you don't have Maven install, you can straight away execute this command provided by
[01:13] the Spring Boot.
[01:14] So this is going to generate a jar file inside the target folder.
[01:18] So let me show you the same.
[01:20] I already cloned this application inside my local system.
[01:23] I open my terminal and navigated into the folder Spring Pet Clinic.
[01:29] Before you try to package your Spring boot application, please make sure you install JDK 25 and set
[01:35] up the same under that Javahome environment variable.
[01:38] If you run the command Java hyphen version, you should get something like this, which is using Java
[01:46] 25 version.
[01:47] Since we are looking to test the Java 25 features, definitely we need to make sure that our operating
[01:52] system is using Java 25.
[01:55] At the starting of this course, I already explained you on how to install a specific version and set
[02:00] under the Javahome environment variable.
[02:03] Next I'm going to run the command dot forward slash M, V and w package.
[02:10] As soon as I press enter, the compilation and packaging of my Spring boot application is going to happen.
[02:17] Towards the end, you're going to get a confirmation that the build is successful.
[02:22] Once the build is successful, you can check inside that target folder.
[02:26] There will be a jar with the name spring hyphen, pet clinic hyphen, so on.
[02:32] So version hyphen Snapchat jar the same jar we are going to use to start this application.
[02:38] First, I'll show you how much time it is taking for this application to start without any Aot optimizations
[02:45] followed by.
[02:46] We can evaluate how things are improved with the Aot performance improvements.
[02:51] Before I try to start my application without Aot, I also want to install one more tool inside my system.
[02:59] This tool.
[02:59] It is going to help me to perform some load testing on my application.
[03:03] Inside Google you can search for or load testing and open the website with the name Terminal trio.com
[03:12] and open these website.
[03:14] Inside this page you're going to have instructions on how to set up these OHA tool inside a operating
[03:20] system.
[03:21] Since I'm using Mac, I selected these under the Mac.
[03:24] I have an option to install these using brew.
[03:27] So I just have to install this command, which I already did behind the scenes.
[03:31] If you are using windows, you can use either scoop option or winget option to install this OHA.
[03:37] So once the OHA is installed, we should be able to leverage this to perform the load testing.
[03:43] I'll share more details around this OHA when we are seeing the demo.
[03:46] First, let me start my application without using a OT.
[03:50] I'm going to clear the console and type Java Hyphen jar.
[03:55] Java hyphen jar is the command that we need to use whenever we want to start a Java application that
[04:01] is packaged as a jar.
[04:02] So where is my jar is present inside the Spring Pit clinic folder.
[04:08] There is another folder with the name target.
[04:10] Inside the target there is a jar with the name Spring Pit Clinic.
[04:14] So on.
[04:15] So version hyphen Snapchat dot chart.
[04:17] If I press enter, my spring boot application is going to start, and towards the end we should be able
[04:24] to see how much time it took to start this application.
[04:27] In total, this process took 3.173 seconds.
[04:32] We can assume around three seconds.
[04:34] We can test whether the application starts successfully or not by navigating to the application URL
[04:40] inside the GitHub page, they have provided the application URL details, which is http localhost 8080.
[04:46] Let me click on the same.
[04:48] This is the home page of the application.
[04:50] If you go to the find owners, you will be able to see the list of owners.
[04:54] And we also have veteran doctor details and there is an error page.
[04:59] We don't have to worry much about this application.
[05:02] I'm just showing a simple demo.
[05:04] So this gives a confirmation that my application started successfully As a next step, I'll open another
[05:09] tab of my terminal and try to perform the load testing of my application, which is started without
[05:15] any overt performance.
[05:16] So the command that I'm going to execute is OHA space hyphen z five seconds.
[05:23] Along with that, I'm providing some application URL which is http localhost 8080 slash wet start HTML.
[05:32] When we click on this option, we should be able to see all the paternity doctor details.
[05:36] The same URL I'm trying to give as an input to perform the load testing.
[05:41] So with this command I'm telling to the OHA tool, please keep on sending requests up to five seconds.
[05:48] By using this URL, the tool is going to send good amount of requests to test the load testing of my
[05:54] application.
[05:54] As soon as I press enter, you'll be able to see some good graphs.
[05:58] Once the command is executed, I'm going to copy this entire data and paste in a tool with the name
[06:04] beyond compare.
[06:05] On the left hand side, I'm pasting the performance report details in few seconds.
[06:10] I'm also going to paste another report on the right hand side, which we tested by using Aot cache.
[06:16] So that is going to give us some clarity how much improvement we have achieved.
[06:20] I'll talk more details about this report in few seconds.
[06:23] For now, let's try to stop the application that we started previously.
[06:28] So here inside the window where I started my application, I just have to press Ctrl C which is going
[06:34] to stop the running application.
[06:36] So this time I'm going to start my Java application by using the first command which is going to create
[06:44] a cache.
[06:45] So what is the command that we need to use.
[06:47] It is Java hyphen x x colon Aot cache output.
[06:54] And the cache name is app dot Aot.
[06:57] This cache name can be anything followed by hyphen, jar and the jar location.
[07:02] As soon as I press enter.
[07:04] This time the application is going to start, and during the startup the JVM will try to create the
[07:10] Aot cache apart from starting the application.
[07:13] You should also do the testing of your application because only few classes will be loaded during the
[07:19] startup.
[07:20] Any other classes which are being executed when you are testing your application, those details also
[07:25] will be cached so that your application performance will be improved when we are leveraging the Aot
[07:31] cache.
[07:31] That's why inside the browser I'll try to perform some actions.
[07:35] I'll go to this find owners and click on these Find Owner.
[07:38] I'll navigate to a owner.
[07:40] I'll click on this Edit Owner update.
[07:43] Next I'll go to this option here I'll navigate to the next page.
[07:48] Next I'll go to the edit page.
[07:49] So try to test as much scenarios as possible inside your application.
[07:54] And all these details will also be cached by the Aot process.
[07:58] Once we are done with all the Aot process, we can stop the application and behind the scenes a cache
[08:06] might have created by the Aot process.
[08:09] If you see there is a cache file created with the name app dot Aot, and the cache size is 125 MB.
[08:17] For real applications it can be even one GB as well.
[08:20] So the more number of data that you cache, the better your application is going to perform when you
[08:26] leverage this cache.
[08:27] So this time I'm going to start my application by using Aot cache.
[08:32] And I'm also going to leverage the OHA tool to perform the load testing.
[08:36] So how to start our application by using cache.
[08:38] It's very easy.
[08:39] The command is Java hyphen X colon Aot cache.
[08:45] And to this Aot cache we need to mention the cache name which is app dot aot followed by hyphen jar
[08:51] and the jar location.
[08:52] If I press enter this time the application should start quickly.
[08:57] So here you'll be able to see the application started within two seconds.
[09:01] So previously it was taking 3.1 second.
[09:04] Now it started within two seconds.
[09:06] Are you seeing we got a improvement of 30 to 40% without making any code changes.
[09:12] I can leverage the same cache so that the scale up process or the startup process is going to be more
[09:18] quick.
[09:19] Now let's try to perform the load testing.
[09:21] I'll go to the other tab and here I'll try to execute the same command which is oha hyphen z five seconds
[09:29] followed by URL.
[09:30] If I press enter for five seconds, the load testing will happen and I'm going to get the output.
[09:35] So this is the output.
[09:37] Let me copy this entire report and paste it on the right hand side so that we can compare what is happening.
[09:43] So if you see without aortic cache within five seconds, my application is able to handle around 6170
[09:51] requests.
[09:52] Whereas with the aortic cache it is able to handle 6431 requests.
[09:58] Apart from that, you'll be able to see there is an improvement in the request per second.
[10:03] Our application is able to process 243 requests, whereas with aortic cache it is able to process 50
[10:11] more requests like 1294 of course, the amount of effort or time that you're going to put while preparing
[10:18] a cache, it is going to decide how much performance improvement your application is going to get.
[10:23] I quickly showed the demo of cache creation in few minutes, but in reality, you should spend more
[10:29] time by testing all the possible scenarios inside your application, which is going to provide you a
[10:35] good cache.
[10:36] And if you provide the same good cache to the JVM while you are trying to deploy your application or
[10:41] start your application, it is going to bring major improvements in the startup of your application
[10:46] and the memory footprint of your application.
[10:48] I hope you are clear on how these Aot new features that got introduced as part of Java 24 and Java 25,
[10:55] they are going to help us in improving the startup time of your application and the memory footprint
[11:01] as well.
[11:02] So without making any code changes, we're able to bring some good performance improvements in our application.
[11:08] So please try to adopt the same in your real applications as well, so that your application is going
[11:13] to perform in a better manner.


########################################

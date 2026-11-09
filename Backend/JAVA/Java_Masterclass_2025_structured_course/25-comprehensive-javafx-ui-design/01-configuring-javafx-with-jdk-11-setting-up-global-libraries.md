# 25.1 — Configuring JavaFX with JDK 11+: Setting Up Global Libraries

> Section 25: Comprehensive JavaFX UI Design

Java applications can have graphical user interfaces that contain buttons, lists, check boxes, menus, toolbars and many other controls that allow users to interact with rich client applications. Javafx is a set of APIs that we use to build user interfaces in java. It's essentially a set of java packages, and it's the successor to swing, which was java's UI toolkit for many years. So you can use javafx to develop the UI for desktop applications, internet applications and mobile devices.

But in this course, we're going to focus on desktop applications. With the release of JDK 11, javafx is no longer part of the core JDK. So that means we need to download the javafx jar files and configure them separately to get them working. So in this video, I'm going to go through the steps to set up the javafx package to work with the JDK 11. Then the next video will actually start building a project. So if you're using JDK 8, then you don't need to watch the rest of this video just fast forward to the next video when we start actually building our first javafx application.

All right. So the process we need to follow to get javafx working with the JDK 11 involves firstly, doing a download. So we're going to download the file that we need. So I'm going to go to our browser. And the website we want to go to is gluonhq.com/products/javafx. And you can see here that it talks about the javafx runtime being available as a platform specific SDK. So we need the javafx SDK for your operating system to be downloaded and installed.

And just a note here that is important to download the correct version. For example, if you downloaded the windows version of the javafx windows SDK, you'd be able to install it and set it up on a mac, but you'll find that it won't work. So make sure you do download the right version. I'm on a windows machine, so I'm going to download the windows version of the SDK for javafx. Good news is it's quite a small download. You can see it's under 38 megabytes.

I'm going to save that and give my computer a moment to run the security scan then we'll continue with the installation. All right. So it's finished downloading. So what I'm going to do is just go to open the folder. If you have any difficulties like I have, just go to explorer and just go to the folder, in my case, the downloads folder. I'm going to go there now. And you can see this open JFX 11, that's the file that I'm going to take a copy of.

Now we need to put that somewhere in a good spot because we need to put it in that spot and then it'll need to be referred to anytime you use javafx in a project. So in other words, you don't want to put into a temporary location or put it on your desktop or somewhere that you accidentally delete. So in my case, what I'm going to do is I'm going to put it in the documents folder in a subfolder called lib. I'm going to paste it into there. I'm going to extract the zip file.

All right. So that's finished now. Then we're going to go into that unzipped folder. And I'm going to cut the subfolder, which is javafx SDK 11. Then I'm going to go back to my lib folder and paste it in there. So in other words, we've now got a subfolder javafx SDK-11 in my lib subfolder. I'm going to delete those other two files now because we no longer need them. All right. So that's that file there, and what we need to do then is swing back to intellij.

So I'll just minimize the browser for now. And we need to configure a global library so that we can automatically use javafx in any projects we create. So to define a global library, click on configure, click on project defaults and click on project structure. Next, we're going to come over here to global libraries. So when I click on plus, I want to select java. Now we need to navigate to the folder where we've just created that javafx folder from the unzipped folder that we downloaded.

So in my case, it's going to be in my users folder and I go to my documents folder. There's the lib folder. In my case, it's the javafx folder. I need to go into the subfolder of lib, then javafx SDK, then the subfolder lib. I need to select all the jar files that are in that folder, select them like so then click on okay. And the other thing i suggest you do is just change the name there to something more meaningful. I'm going to call that javafx 11, just so for me I know that that's the javafx library for the jdk 11.

So I'm going to save that. At this point, we've been able to find the global library for JDK 11. So I'm going to end the video here now. In the next one, we're going to start creating our first javafx application. So I'll see you in the next video.

----------------------------------------

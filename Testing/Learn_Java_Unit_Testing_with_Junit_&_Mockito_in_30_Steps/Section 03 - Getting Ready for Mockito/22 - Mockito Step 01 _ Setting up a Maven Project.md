# Mockito Step 01 : Setting up a Maven Project

*Section: Getting Ready for Mockito*

Instructor: As with all the in28minutes tutorials and courses, we would start this one in a hands-on way as well. So before we discuss a lot of theory about Mockito, we would start with our step one, and try and set up a project where we can start discussing things much more. So this is step one where we would learn how to set up an Eclipse Project with JUnit and Mockito frameworks. And we would end this step once we have a successful unit test.

If you have already followed the JUnit course and come up to here, most of this step should be very easy for you. So it should be a quick step where we get started with JUnit and Mockito. I'll launch up Eclipse. You can enter any workspace folder in here. I'm entering Mockito August, 2016. That's basically when I'm creating this particular course. Or you can click browse and browse to a specific folder.

The workspace is kind of the folder where Eclipse would store all these files. So I'll enter workspace and click okay. When you launch up a new workspace, Eclipse would bring this particular window up. I'm not really interested in this right now so I'll just close this, and I would want to start by creating a new Java Maven Project. So I would start with File, New, Maven Project. Maven is very useful in maintaining dependencies.

With JUnit and Mockito, I would want to be able to use these frameworks. I don't want to go to the repositories and download the jars and put them in the build path. Maven is a tool which helps us make it very easy to manage dependencies. If you have no previous experience with Maven, that's not a problem at all. In this course, you'd be able to follow and understand what are the basic things about Maven.

You can start off, I'm doing a cancel again. So it's File, New, Maven Project. Or you can actually say File, New Project, and type in Maven. Or the other way of getting this here is right-click here and say New Project and type in Maven. So any of the type ways you would want to start, that's okay. So type in Maven. We want to create a new project. So New Maven Project and click next. So I would choose the default workspace location.

The other thing is I would also want to create a very simple Maven Project. So these two check boxes you can check in and say next. And one of the things with Maven is you need to give a name to the project that you're creating. So this is a new project I'm creating, so I have to name it. And just like a Java class, we have a package similar to that for any project you need to have a group ID. So I'll just put in com.in28minutes.mockito as the group ID and the artifact ID as mockito-example.

So you can actually put anything that you would want in here. I'm just saying com.in28minutes.mockito and mockito-example as the thing. So, Mockito of course. And I'm going to click finish. When the project opens up on the top left folder, you should see all these folders inside the Mockito course. So you'd see source/main/java, source/main/resources, source/test/java, and source/test/resources. Typical Java project, you would have all your source code in source/main/java, and all your tests in source/test/java.

That's exactly what we followed during our JUnit course as well. So we write all the code in source/main/java and all the tests in source/test/java. In a typical Maven project, you also have a pom.xml. Pom.xml is the place where you declare all the dependencies that you would want. Let's open the pom.xml. Double-click on it and it would open this, where I can actually click the pom.xml to see what's in there.

Right now it's a very simple XML file. There's not a lot of details in there. There's a group ID, artifact ID, and version. In this project we would want to learn JUnit and Mockito. So we want to use Mockito. So we would want Maven now to download Mockito and JUnit for us. How do we do that? The way we do that is by adding something called a dependency. So just go and add in dependencies. And the dependency that we would want to add in are JUnit and Mockito.

I've made it easy for you by actually going in and actually making the dependencies available on the GitHub. So if you look at this step one, this contains the dependencies section right here. So you can actually take this dependencies section, and instead of typing in dependencies, dependencies, you can actually start out fresh and actually paste this in. So what you do see right now is these dependencies will be downloaded and added in here.

That's the magic of Maven. So now, you have these jars downloaded by Maven and made available as part of Maven dependencies for this project. And that's the beauty of Maven. And that's the reason why we are using Maven in this particular project. So instead of downloading the JUnit jar and making it available in the build path, what we are doing is we are using Maven's pom.xml to download these jars and make them available for us.

We have a dependency JUnit, and we are using 4.12 version of JUnit here, and 1.10.9 version of Mockito. So these are the two dependencies which we added in. And here are all the stuff that we would need to run this particular project. So let's get started and start creating a small test to check whether everything is working fine. So I would start with source/test/java because we want to create a new unit test.

I would create it in source/test/java. Right-click, New. I would want to create a test class. So I would say Test, JUnit Test Case, and click next, and say New JUnit Full Test. That's good. Since you are already familiar with JUnit, I would go ahead and quickly create this particular test. So I would call this First Mockito Test. I mean, there's nothing Mockito in there yet, and I would want to put this in the package com.in28minutes.Mockito.

And I would go ahead and click the finish button. So this would create a small test for us. And I'll remove this fail. I would add a simple assertTrue(true). This is a funny test because this is actually not testing anything, just to make sure that there is something being tested at, I just added it in to have some fun. And there you go. So there you see the green bar again. So the way I'm running the test is right-click Run As JUnit Test.

So that's basically what we are doing to run this test. So what we have done during this step is that we actually created a simple Maven project, added in two small dependencies, JUnit and Mockito. So Mockito is the thing that we are going to use in this particular course. So we added the Mockito dependency. And also we wrote a simple test. This test is not yet to using anything from Mockito yet. We'll start with using Mockito very soon.

Until the next step. Bye-bye.

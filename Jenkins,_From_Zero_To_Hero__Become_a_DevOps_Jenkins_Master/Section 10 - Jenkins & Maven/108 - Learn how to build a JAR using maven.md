# Learn how to build a JAR using maven

*Section: Jenkins & Maven*

Instructor: Hello, and welcome back. In this video you're going to learn how to build a JAR using Maven and this code that we have just cloned. So for this, we need to define a Maven installation. So let's go to Manage Jenkins, let's go to Global Tool Configuration. And here, we're going to look for Maven. Okay, we found it. Let's click on Add Maven. And here, we're just going to give it any name, like jenkins-maven.

And then we're going to look for the Maven version that we want. In this case, we're going to be using the latest version. So that's everything we need to do. Let's go ahead and save this. And we're ready to start configuring our job. So remember that we created a Maven job, which for now is only downloading or cloning the Git repository. So let's go to configure.job. And we're going to go down, down, look for the build section, and we're going to add this step, which is invoke top-level Maven targets.

So we're gonna click on this. And as you can see, it actually asks for the Maven version. And we're going to use the Jenkins Maven that we installed. If you have a preferred version or if you wanna install a specific version, then you can just remember on the Global Tool Configuration, define that version. And the goals are, what are we going to do here? Well, and the first thing that we need to do, and the, or the first thing that normally a continuous integration process does is nothing else but building a JAR.

You already have your code. Now, the second thing should be building a JAR using that code. But how do we build a JAR using Maven? Well, if you go to the repo and you go to the Jenkins folder, you're going to find out something called Jenkinsfile. And if you go here, don't worry. We're going to talk about Jenkins files later. That if you go here, you're going to find out how to build a JAR. And this is the line that we're going to be using.

So we're going to be using only this line because if you're invoking this Maven target, you're already using the Maven command. So we only need to pass the flags. So this is going to skip the test and then it's going to actually do a package, which means a JAR. So that's everything you need to do. Let's go and click Save. And after that, you're going to click on the Build Now button. So let's go to the Build History, to the execution, Console Output.

And as you can see, the first thing that this job is going to do is that it's going to pull the newest version from this GitHub repository. And after that, as this is the first time that we're going to run this job, the Maven version that we have specified is not installed. So Jenkins is going to start downloading that version. Don't worry, it's only going to happen once. But depending on your internet connection, it may take a while.

So let's wait until this finishes. I will pause the video and I will come back once it has finished. The job already finished downloading the Maven packages. And as I told you, it's only going to happen once. And finally, you can see this building_jar, which is success. So as you can see the resulting JAR, which is called in the DevOps world as an artifact. This artifact, it's actually located on the workspace.

So if you remember, the code is actually cloned in the workspace and this JAR is actually located at that workspace. So if we go to our console and we are here on the workspace, let's look for the full path. We need to go to maven-job-target. And there, we're going to find the JAR. So let's go to target. And you're going to find your JAR build there. So this is actually pretty cool. This looks pretty much like a continuous integration process because this is actually a continuous integration process, but the difference is that we're not using the Pipelines plugin, but this is exactly the same thing.

In the future, we're going to learn how to do this using Pipelines. But for now, we're just building a normal job for you to completely understand how everything works. If you click on Build Now, remember, what's going to happen is that the first thing that you're going to do or that Jenkins is going to do is going ahead and downloading or cloning the repository to your workspace. So that means that every execution, it's going to have a new code or the newest version of that code.

After that, you are running a Maven package, which is actually going to take the POM, that XML file that is on the root directory of your workspace. Let me show you. If you go to the root directory, this is the root directory. And you're actually, using this POM when you do the Maven package. So Maven is actually looking to the code that you'd previously downloaded. And based on that, Maven is actually building a new JAR.

So that's pretty cool. You already know how to build a JAR using Maven. I'll see you in the next lesson.

# Add post actions to Jenkinsfile

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello, and welcome back. In this video, we're going to add post actions to our Jenkins file, because remember that we're building a Maven application, and probably we want to record the JUnit report and we want to archive the success artifacts. So how do we do this? Well, let's open up our Jenkins file, and remember, we actually took a look at this in the previous section where we discussed about post actions in Jenkins files, so we're going to have one post action for build and one post for test.

Here, we're going to record the unit tests, and here, we're going to archive the successful artifacts. So for this, we're going to go to Google and we're gonna take a look at Jenkinsfile post actions archive artifacts. Look for it, let's look for the first result, and you have a lot of examples in here. So let's grab this example, I think. Yes, it could be... Okay, let's copy this, and we're going to paste that right here.

So let's paste this. Let's paste that inside of the build stage. Let's copy that again, and now you can see that we have this post action. We want to put it under the stages. So we're gonna say always, let's say 1, 2, 3, 4, always we want to archive the artifacts. Well, we don't want this to be always, we want this to be only when the job is success, so we will say success, we don't want to do this, and we want to close this, because remember, this is the close of the success and this is the close for the post.

Okay, that's super cool. So let's copy this again, and now we want to do exactly the same thing in the test stage. So we're going to hit enter in here. We're going to paste exactly the same thing, that we want to do this always. So here, we need to do a couple of changes. First thing is that, remember that our JAR is being saved in java-app/target, and then you say asterisk jar, everything that ends with jar.

And in the JUnit report, okay, this is my bad, we need to actually copy this JUnit, so we're gonna copy this right here. Let's hit enter, paste that, and we want to put this under always, like 1, 2, 3, 4. And we're going to modify the JUnit, because remember that the JUnit is in javaapp again, and we have the target, and under target, we have surefire-reports, and under that, we have that report. So this is it.

We're gonna save this, because we already have what we needed. We have a post action always that is going to record our JUnit result, and we have a success artifact that is going to save our artifact only if the execution succeeds. Okay, that's cool, so let's save this file, and we're going to add it. So let's say git add Jenkins, and we'll say git commit dash M, and we say adds post actions for, or to, Jenkinsfile.

And we say git push, and then we're going to have these changes in our Git repository. So you can go to your Git repository. Let's look at the commits for this repo, and you're gonna see the commit that we have just done that contains the changes to archive the artifacts. So that's super cool. This is it for this video. I'll see you in the next lesson.

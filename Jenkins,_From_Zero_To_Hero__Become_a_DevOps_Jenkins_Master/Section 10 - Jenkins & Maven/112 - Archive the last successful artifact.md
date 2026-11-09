# Archive the last successful artifact

*Section: Jenkins & Maven*

-: Hello and welcome back. In this video, we're going to learn how to archive or how to save the artifacts in Jenkins. So to do this, let's go to configure and we're going to add. Okay, before configuring let me show you where the jar is located. If we go to any execution and we look for the Maven package we're gonna see that we have the jar located in here. And if we go to the console, and you know that this is the root of your workspace, then you do an LS and you know that your jar is saved on target and then it's the file that actually ends on that jar.

So you can do like asterisk dot jar and then you're going to find your jar. So this is the folder that we're going to be using for the configuration. So let's go to the Jenkins, configure this and we're going to go to the final part and we're going to add a positive action which is going to V archive the artifacts. As I told you, in DevOps we call an artifact to the result of the build. So Jenkins is asking, okay, what do you want to archive?

And we want to archive this which is the folder target and the jar that's generated. So this is the path for the jar. We can go to advanced and we can say, okay I want to archive artifacts only if the build is successful because probably you don't want to archive a failed or a corrupted jar. So let's only save the successful jars. Okay, so let's click on this, and now we click on save. We're going to build this job and you're going to see that if everything goes good our jar is going to be appearing in here which is the last jar that was built successfully.

So let's wait until this project finishes and we're going to see what happens. Super nice. It actually finished. So let's go to the job. And as you can see now we have the last successful artifact in here, and this is actually the jar that was built and the last successful built jar. You can click on it and then you're going to find out that you can download that file. So you already know how to create a graph with your test result and you already know how to archive your jars.

So you can click on it and download it whenever you want. So this is it for this video. I'll see you in the next lesson.

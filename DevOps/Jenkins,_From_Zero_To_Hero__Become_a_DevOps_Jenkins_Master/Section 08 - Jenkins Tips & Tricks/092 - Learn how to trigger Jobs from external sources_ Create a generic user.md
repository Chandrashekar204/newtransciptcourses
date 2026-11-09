# Learn how to trigger Jobs from external sources: Create a generic user

*Section: Jenkins Tips & Tricks*

Instructor: Hello and welcome back. In this video, we're going to learn how to trigger a job externally. I mean, you know that you can, for example, go to any job that you want, click on that job, and then you're gonna click on the Build button, and the job is going to be executed. But what happens if you want to execute that through an external source? Like a script or something from a console from another part.

For example, let's say that you have another application in another server and you want that application to trigger a Jenkins job. How do you do that? Well, that's what we're going to be learning here. The first thing that we need to do is authentication. Because remember that currently our Jenkins is using authentication. So we need to create a user that's actually capable to trigger any job, or you can restrict that user as you have already learned.

But in this case, the user that we're going to create is going to have permission to trigger every single job that we have. So to do that, we're gonna go to Manage Jenkins, and we're going to scroll down a little bit, and we're gonna click on Manage Users. Once we click here, we're gonna create a new user. And let's call this user Jenkins, for example. Password 1234, 1234. Let's give a name in here and a email.

So Jenkins@jenkins.com, for example, and we're going to create that user. Okay, so we already created our Jenkins user. Now we need to associate this user to a role to allow permissions to the jobs. So we're going to go again to Manage Jenkins. And as you may know, we're going to go to Manage and Assign Roles, and we're going to go to Manage Role. And we're going to say, for example, we're going to create a new global rule which is going to allow this user to trigger all of the jobs or to build all of the jobs.

So let's call this Trigger Jobs or something like that. Let's click on that. And here, remember that you always need to add the overall read permission so the user can have the overall permission and therefore log into the Jenkins service. So once we click on the read overview, we're going to go to the job section, and we're going to click on Read and on Build. We already had our role pretty similar to this, which is the execution, but we're just gonna create this for this example.

So remember the overall read permission, and in the job section, remember that we're going to allow build permissions and read permissions. And this is actually going to allow to view every single job that we have. So let's go ahead and save this. And now we need to assign that rule to that specific user. So remember that the user that we created is Jenkins. So let's add that user in here, and we're going to bind or link this new user to the Trigger Jobs global role that we created.

So doing this, this user is going to be capable to read and build all of the jobs that we have. So this is it for this video. Don't forget to click on Save. I'll see you in the next lesson.

# Create a Git User to interact with your Repository

*Section: Jenkins & GIT*

Instructor: Hello and welcome back. In this video, we're going to learn how to create a user and how to grant that user permissions over this new repository that we created. So we need to create a user first. Let's go to the admin area here, and we're gonna click on Users, and we're going to add a new user. So let's click on New User. We're going to say Ricardo, for example, the username for this user, the email.

So let's give a fake email for now. So let's scroll down a little bit. This is going to be our regular user and we're gonna create that user. And now, that you created the user we now need to edit this user to set a password. So the password is going to be 12341234. And we're gonna click on Save changes. And now, okay, password is too short, minimum eight characters. Yes, what I told you before so let's go ahead and say 1234567812345678 okay and let's click on Save changes and that's pretty cool.

So I'm just gonna click on No here and this is it. Now that you've created this user, you need to assign these user permissions to see the Maven repository. So we're gonna go to Projects, and here we have our Maven project that was created under the Jenkins group. We're gonna click on that and we're going to look for Manage access, project members, Manage access. We're gonna click here and we're going to look for Ricardo which is the user that we created.

And for now, we're gonna give this user maintainer permissions because we are going to need to create a master branch. And if we don't give this rule then we're going to have errors. So let's click on Add to project, and this is it. Now, if you clicked on your Maven project and then you go to the left side hand and click on Settings, Members you're gonna see that the Ricardo user actually has access.

And we gave that access within one minute. So it was one minute ago. So now, our user is actually capable to do things on this Git repository. So this is it for this video, I'll see you in the next lesson.

# Create a role to execute jobs, and assign that role to your user

*Section: Jenkins & Security*

Instructor: Hello and welcome back. In this video, we're going to learn how to create a build role in order to allow users to build jobs. For now, let's say that we want the user Ricardo, or the user Tom, the one that you prefer to be able to build all of the jobs. This user is going to be allowed to read and to build but it's not going to be allowed to create or to delete or to modify any existing jobs.

So we're going to go to Manage Jenkins and we're going to look for manage and assign roles. Let's go to manage roles and in here, we're gonna add a new role. But remember that for now, these roles allow the user to build or to read all of the jobs. We're going to see later how to restrict the user to be alert to (indistinct) jobs. But for now, let's keep it like this. Let's create, for example, an execution role.

So let's click on add in here. You can name the roles as you prefer and remember that the overall read should always be marked in order to avoid the error that we had before. So if you want the user to be able to do something, you need to click the overall read. So okay, now we're gonna move to the jobs tab and we're going to click on build and we're gonna click on read. So the user is going to be allowed to read and to build.

So this is it. Let's go ahead and save this. And now we're going to go to assign roles and we're going to allow this user Tom the execution role. So we're gonna unmark this and we're going to leave only this marked. Cool, so in this case, the user Tom is going to be allowed to read and to execute jobs. So let's save this. And if we open up an incognito tab and we look for Jenkins in here, and we log as the Tom user with the password 1234, then if you go to any job and you click on build with parameters, as you can see, now you have the button in here.

So let's click on build and let's see what happens. So as you can see, this user is actually capable to build jobs. And remember that this user didn't have this capability before. We actually granted that by creating a new role and assigning that new role to this particular user. So this is how you create roles based on what you want the users to be able to do and then that's how you assign that role to a specific user.

So this is it for this video. I'll see you in the next lesson.

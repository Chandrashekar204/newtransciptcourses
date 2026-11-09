# Allow users to sign up

*Section: Jenkins & Security*

Instructor: Hello, and welcome back. In this video, we're going to learn how to allow users to register themselves. So imagine that whenever you get the login screen you have an option to register or to sign up. So that's what we're going to allow in this video. So we're gonna go to Manage Jenkins in here, we're going to go to the Configure Global Security, and under our Security Realm we're gonna click on Allow users to sign up.

So we're gonna click on that, let's click the Save button. And now if we open an incognito tab and we browse to jenkins.local, as you can see now we have a Please sign in below or create an account. So we're gonna create an account in here, and as you can see, we're just gonna give it a name. We're gonna give the full name, for example and we're gonna give some mail in here. So that's like this. And we're gonna give it a password which is one two three four for this case.

Show, one two three four. And let's create an account. So the thing that I wanna show you is that, as you can see we actually were able to create a new account and that account is going to be by default an admin account. So if I go to Manage Jenkins I have all of this available configuration, I can even go to the home and I can go to any job and I can delete any project, I can configure or change it, modify everything as a normal user.

And probably we don't want that, probably we don't even want the users to be able to register or to sign up. But for this video, I just wanted to show you if you wanted, how the users can sign up, which is not a good practice because if someone finds your Jenkins server, then that person is going to be able to create a fake account and is going to be able to log into your system. So I just want you to know that this possibility in Jenkins exists, but you should not enable this unless you know what you are doing.

So in this case, we're just going to go back to the Configure Global Security and we're going to uncheck this Allow users to sign up. So in the future, let's click on Save first, and in the future, we're going to learn how to restrict the users to what they can do. For example, we want to restrict users only to execute a job, but we don't want that user to be able to delete the job or modify the job.

Or we don't want the user, for example, A, we don't want that user to be able to see the backup jobs or we don't want the user to be able to see the remote task job, for example. We can restrict anything that we want using things that we're going to be learning. So this is it for this video. I'll see you in the next lesson.

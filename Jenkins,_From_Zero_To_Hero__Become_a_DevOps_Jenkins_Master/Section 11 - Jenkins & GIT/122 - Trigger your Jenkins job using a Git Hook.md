# Trigger your Jenkins job using a Git Hook

*Section: Jenkins & GIT*

Instructor: Hello and welcome back. In this video, we're going to test the Git hook that we created before. So let's go to the Maven folder that we created. Remember that this folder actually refers to our Git server. If you do a cat config, or I think it's like git/config, you're gonna see that this is our gitlab.example.com. So we want to modify the coding here to trigger the Git hook doing a commit and then a push.

So let's grep recursively for hello. And as you can see, we have two files. So we're going to modify the app.java which is the application, the code for the application. And we're going to say Hello World from Git and Jenkins. We're gonna save that, and we're gonna modify the test code for the tests. So let's modify this and we're going to look for this line that says try assertEquals and we're going to say Hello World from Git and Jenkins.

We're gonna save this and this is it. So if we do now a git status, you're gonna see two files modified, the app.java and the apptest.java. So if we go to our project, our Maven project, and if we reload this, you can see that the last execution was the number 18. So let's go ahead and do a commit git add source git commit dash M, and we're going to say like test git hook trigger. And then you do a git push origin master, and you hit Enter.

You are gonna see that you have in here the upload process and you have here the output of the kernel command. So if we go to our Jenkins job, you can see here that the Jenkins user was the one that started this. And now we're downloading the new code, which is the commit that we did. That's test Git hook trigger that's been downloaded in here. And after that, the new code is going to be packaged as a yard is going to be tested.

And remember that that code had a different message. So if we go down here, you're going to see the modifications that we did. Hello World from Git and Jenkins, which is pretty cool. So it means that whenever someone change any code or any file in your repository and that person pushes to your repository, this job is going to be triggered and therefore it's going to be testing the new code. It is going to be downloading the new code, building it, testing it, and finally deploying it if everything goes good.

So let's do a new test in here. Let's go to our repository and let's modify something different. So for example, let's modify the test. Let me grep recursively, R for hello. And let's modify the test. So we're going to make this fail because we're going to modify this code and we're going to say Hello World from Git. And as you see, if we go to the other file, we have a different message, and therefore this assertEqual is going to fail with this message.

So we're going to save this and we're going to do git status again, git at source, and we're going to say git commit dash M intentional failure. And we're going to do a push to origin master. It's going to say, okay, so we go to our job and we take a look to the execution. Let's go to the console output of this. And this job should fail doing the tests because we modified the code and we actually did an intentional failure, something like simulating a book in your code.

And that book is going to make your job fail. So as you can see here, we actually have the failure because here is the reason, but the main reason is because the two files have different content and the test is only looking if the content is the same. If it's not the same, then it's going to fail. And as you can see, it actually failed the message that we expected and we have an error here. So in this way is how you can catch errors in your code because whenever someone pushes a code that has a book or something, your Jenkins job is going to fail.

And then you're going to see why this failed and what is the root cause for this failure. So this is it for this video. Hope you've learned a lot from this. I'll see you in the next lesson.

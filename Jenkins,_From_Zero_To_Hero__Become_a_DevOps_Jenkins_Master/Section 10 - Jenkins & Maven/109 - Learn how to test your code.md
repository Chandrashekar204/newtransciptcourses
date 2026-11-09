# Learn how to test your code

*Section: Jenkins & Maven*

Instructor: Hello and welcome back. In this video, you're going to learn how to execute unit tests on your project. So let's go and configure this Maven project. And remember that now we have a nice continuous integration processing here, which is downloading the code from somewhere, then building a JAR using that code. And now we're going to add tests. So we're going to invoke top level Maven again, and we're going to use this version.

And the goal is going to be simply test. And these word tests is an argument of Maven. And you say like Maven test. And that's actually going to scan your project and look for the tests that someone must write because tests are not going to be written by themselves. Someone needs to write those tests. But in this case, we have tests in here. Let's go to the simple Java Maven. And here if we go to source, we have a test folder.

And as you can see, we have the tests that this job is going to execute. So once we do Maven test, let's hit save, and let's build this project and see what happens. The execution is going on, let's go to the execution, console output. As you can see, the code is being cloned, the JAR is going to be filled. And finally, Maven is going to start doing the test part. As you can see, it's the test that we define here.

It's going to start a scanning for projects, finding your tests, and then it's going to execute those tests. And probably you're going to find this error, probably not, depends on the version that you installed, but let's fix this error. Probably you might be wondering why these error happened. And don't worry, it's not my fault, it's not your fault. It is, as you can see in GitHub, this is a book on Debian, so don't worry, and the work around is setting an environment variable that has this content.

So I actually looked for a better answer, and this is what we need to do. So to fix this or to work around this little book, we need to define this variable, and we need to define this value. So you need to apply the knowledge that you already have created, and you need to go ahead and create a new environment variable using this. So if you can do that, please go ahead and try. Otherwise, I'm just gonna do it.

Okay, so we need to go to our job, our Jenkins configuration. Let's go to manage Jenkins, configure the system, and we're going to create a new global environment variable. So here we're going to click on add, and we're going to look for this answer. We're gonna copy the name of the variable, copy, paste that in here, and we're gonna paste the value which is, this is the value, let's copy and paste that in here.

And finally you just click on save. And after that, let's go back to our Maven job. Let's click on build now. And we're going to go inside of this execution, and we're going see what happens. Remember first thing, downloading the code from Git, the newest version. Second thing, building the JAR, and third thing doing tests on that JAR to validate the functionality or everything that we need to do.

And we have the same error. Why? Let me look. Oh, probably we actually made some typo or something on the variable. Let me go ahead and look. Manage Jenkins, configure the system. Probably that's a typo. So let's look for the variable. And yes, it's Java options, isn't it? Yes, I'm using an S in here, so let's put that S, let's click on save. These are normal things that may happen to you, but the idea is that you know how to fix the errors that appear on the way.

So we're gonna go again to the console, and we're going to wait. Oh, and as you can see, it actually picked up this variable. Wait in here. Well, let's wait until this finishes. This actually picked the variable in here. And this is to work around the issue. And as you can see now, the job is not failing anymore. It's downloading the code, building a JAR based on that code. And finally it's executing tests.

And as you can see it run two tests, and there were no failure test. It means that all of the tests are pretty good. So this is it. You've learned how to integrate unit testing to your job. Now you are downloading your Git Repo, creating a JAR, and testing that JAR using Jenkins. And that's pretty good because normally that's what continuous integration does. So this is it for this video. I'll see you in the next lesson.

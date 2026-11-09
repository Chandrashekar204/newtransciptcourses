# Start the CI/CD process by committing new code to Git!

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello, and welcome back to the last video of this course. Here, we're gonna modify the code and we're going to simulate code changes. So whenever we push those changes, our CI CD job is going to be triggered and it's going to do all of the fancy stuff that we have done so far. But before that, I will connect to our remote machine and I will take a look at the current container. So let's do docker logs maven-app.

And as you can see, the jar that has been executed says "Hello World!". So now we wanna change this text. It's going to say something like, "Hello Pipeline!". We're going to push the new change to Git. Git is going to trigger the entire CI CD process, and it's going to update our final application with the new changes. So let's exit and let's do the modifications. So let's go to our jenkins-data/pipeline.

And remember that this is a Git repository. So in java-app, we have all of the code for this application. So let's look recursively for "Hello World!" to find where this has been saved. Say Hello. And as you can see, we have a lot of things right here. So we're going to be using this App.java. Let's use this file, let's copy this. And we're going to modify this file. We're going to say Hello from Pipeline.

We're gonna say "Hello from Pipeline!". We're gonna save this, and we're going to do exactly the same thing in the Test.java file. So let's copy this, let's paste that in here. Okay, let me remove this. And we're going to look for the assertEquals. Yes, this is the one. So we're going to say "Hello from Pipeline!". I don't remember if I put the name, so let's look for it, grep -R. And it's "Hello from Pipeline!" and "Hello from Pipeline!".

Yes, so that's super cool. And this way, we're actually simulating a change in the code. So if you do a git status, then you have modified the source code. And this change should build a new jar with the string of "Hello from Pipeline!". So let's go ahead and do git add src/, git commit -M. We're going to upload this to Git because in this moment, we're Java developers, and we're going to say, okay, git commit, updates the application message.

And we're going to push it. Hit enter. And as you can see, it was actually pushed to our repository, but looks like our trigger wasn't executed. Let's go ahead and take a look at our pipeline. And nope, our Git hook was not executed. Why? Oh, I think I found it. I was looking at the files and I found that we actually created this as custom hook, and this should be custom hooks. So let's go ahead and modify this.

Let's log it inside of the git-server container. Let's go to the directory for this repository, and let's change this name from custom_hook to custom_hooks, which is the correct name, right? So okay, now we're going to do exactly the same thing. We already pushed the code, but the execution didn't start because we had a typo. But now we're going to do another push. So let's say git commit --allow-empty.

And then we say -m, and we say "Test trigger". And we say, git push, and hit enter and see what happens. And yes, as you can see, our execution was successfully triggered. So let's go here. And perfect. Our job is being built. So let's go to this execution. Let's go to console output. And we're gonna take a look at the logs. Remember, the first thing that we always do is that we download the new code.

In this case, we're downloading the last version of this code, which is our test trigger code that we actually pushed. After we download the new code, we start building the jar with that new code. Remember, the code had a different message. It says "Hello from Pipeline!". And this jar is going to be built using that code. After the build is successful, then we're going to start building the Docker image, copying the new jar to the image.

Finally, we start doing tests to the code. Everything went good, so we keep scrolling. And if everything goes good, then we just push this to our Docker Hub repository. And finally, we deploy this new image to our remote machine. And the final thing that we should see is that our container in here, where it says Recreating maven-app, it should now say "Hello from Pipeline!" because we actually created all of this process to easily update our remote application.

Do you remember that previously our containers said, "Hello World!"? Well, through all of this process, this container should be updated. And now it should say something like, "Hello from Pipeline!". So let's go here. Let's ssh to that machine. And let's verify it. Let's do a docker ps -la. And as you can see, now we have a new image in here, which is the execution number 4. Pretty cool. Now let's do docker logs to the maven-app container.

And as you can see, it says "Hello from Pipeline!". So we updated this service, this container, which was in another machine, just doing a push change in the code. And whenever we did the push, the process started all the CI CD workflow started building, testing, and doing more to finally deliver the new code that was tested to that remote machine, which can be your production environment, your desk environment, your QA environment.

It could be anything that you want. But I want you to see how powerful Jenkins can be. Because the only thing that you needed to do was to push new code to Git, then Git triggers the job, and the job starts doing all the magic. So I hope that you have really learned a lot from this course. And I hope to see you in the next courses.

# Create a Git Repository to store your scripts and the code for the app

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello, and welcome back. In this video, we're going to create a Git repository in our Git server to store the code that we have just created. So let's log in in here using the root, 12345678 password. Perfect. Now, in here, we're going to create a new project under the jenkins group. So, we're going to look for the jenkins group, and the project is going to be, for example, pipeline-maven, as you want.

And we're going to create the project. So we're going to go to our terminal. Let's go to our jenkins-data folder. Let's go to our pipeline folder that we have created. And we're going to start reading the instructions. And we already created the repository. So now, we want to add our existing folder to this repository. So for this, we change directory to that directory. We are already here. Then we do git init.

So we're going to copy that. We're going to paste that in here. Well, git init. Hit Enter. And as you can see, that repository was initialized. Then we're going to add this guide. So we're going to copy this, we're going to paste that. And in here, we're going to pass the credentials for our user. If you don't remember your user, then just Control+C and take a look at your dsl project. .git/ config, and you're going to find your user there.

So we're going to be using this guy. So I'm just going to copy this. Remember this instruction that we read from Git. Let me copy that again. Let me type this. Yes, we're going to copy this instruction again. And we're going to add here the credentials. So this user and the password, yes, at the server. Pretty nice. Then we do git add. But before doing git add, we're going to do git status. And you're going to see that you have your Dockerfile and your Jenkinsfile right there.

I don't know if we want to upload our Dockerfile. I think that we're not going to upload it. So we're only going to upload our Jenkinsfile. So we're going to add it. We're going to add the java-app and the jenkins folder. So we're going to add this. Okay. Then we can do a commit. So we can commit this. And finally, we're going to push it. As you can see, when we committed it, we actually had a lot of files in here.

This is all the stuff that we have been working in, all of our scripts and all that stuff. So we're going to push it. We're going to say git push origin master. And here, we have an error because we haven't granted permissions to this user. So let's go to our repository. Let's go to Settings, Members. This is a super important point. Let's look for our user. Let's give it maintainer permissions. Let's add it to the project.

And that's cool. So now, we should be able to push it without any problem. And even though when we already did that, this is not working, why? Oh, okay, this is because we haven't added the port in here. If we go to our server, remember that we are using this port, so we need to add it there. So let's go to vi .git/config. And in here, we're going to modify the port. So that's going to be :8090. Let's save this and let's try to push again.

And now, it's working. Cool. So let's go to our repository. Let's go to pipeline-maven. And we should see now all of the content that we uploaded. And that's cool. Here we have our Jenkins file, which is pretty nice. Here we have all the things that we did our jenkins folder. And here we have all of the scripts that we created. And here we have the Java application, which is the source code that we're going to be using.

So this is it for this video. I'll see you in the next lesson.

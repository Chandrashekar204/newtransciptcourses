# Deploy: Transfer the deployment script to the remote machine

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to create a script to automate everything that we did previously. Okay, remember that I'm still in that remote machine connected through SSH, so this is that remote machine that you created. I'm here, and this is the Docker composed file that we created in the previous lesson. So now we're going to create a sample batch of script to automate all the processes that we did.

But remember that the first thing that we did was defining the image, then defining the tag, and then defining the password, which is three P. Okay so this is what we did. So we need to do exactly the same thing in a batch script. So let's create a batch of script let's call it like publish or whatever you want. We can say slash slash bin, slash bash, and then we're going to execute this first line.

Then we're going to execute the second line, which is the tag. We're going to paste that in here and let's execute the third line, which is the password. So we're going to copy this and we're going to paste it. Cool, so in this way we already have the name of the variables that we're using in the Docker compose file. Now that we captured these names, we need to log into Docker. So that's going to be Docker login, the username, and the password that we already captured in here.

So password. And the final thing is just doing the docker compose up dash D. So for this, let's go to CD, maven, because remember this is the folder that we created. This is like doing this. Let me save this CD maven. This is the folder that we just created. So we're going to do that CD, and then we say and docker compose, up dash D. And this line actually creates the service. So we're going to copy this line to our publish file and this is going to be the final line of our process.

So we're going to paste that in here and cool. As you can see we're retrieving the variables from this file, then we're logging into the docker hop, and finally, we're starting and deploying the service using these variables to download the image that is coming in this tag. So this is super cool as you can see. Let's save this and let's give it executable permissions in here. Publish, and let's try to execute this script.

And as you can see, it's actually complaining because it says, if you want to do, let's take a look. Maybe we did some typo. Yes, we did a typo right there. So let's modify this because we put a colon at the end. So let's save this again. Let's run it once again. And as you can see, this is actually working good. The login is successful and the deploy of the application, it's going good. So let's take a look at this script and we're going to exit out of here.

And you have two options. The first thing is that you can leave your script right here in that machine, or you can transfer that script in every single execution. So for this example, we're just going to transfer this script from Jenkins to this machine. So the first thing is that we're going to copy the content of this. And as you can see, now, I exited out of the remote machine and now I'm logged in in our laboratory machine which is the machine that has a lot of the containers, our local machine.

In here, I'm just going to go to our pipeline folder, Jenkins deploy, and in here I'll be creating the same file which is going to be published and I'll be pasting exactly the same content. Cool, I'm just going to give it executable permissions, right. And now in the deploy stage, then probably we want to transfer in here that script to the remote machine. But remember, keep in mind that every single thing is going to be executed from this folder, from the Jenkins file level.

So the path to transfer the file would be Jenkins, deploy, and publish. So this is the path that we're going to use to transfer. So let's modify the Jenkins deploy, deploy file and we're going to transfer that again. So we're going to do SCP dash I, exactly the same thing, OPT, prod, we're going to pass this file, remember? So this is the relative path for this execution. And then we pass exactly the same thing.

We can pass it to slash temp publish if you want, or you can put it wherever you want. Or if you don't want, you can just leave the script in your remote machine and that's it. But in this example we're going to be transferring this script. Cool. So now let's save this. Let's save it. And as you can see, we now are transferring the script that we just created, which is the published file, to slash temp slash publish, to that remote machine.

So let's go ahead and execute this, deploy script, to see what's going on. So Jenkins, deploy, deploy dot SH, and remember that now this script is going to do two things, or three, actually. The first one is generate environment variables. Second one is transferring the first out file to our remote machine, and the second one is going to be transferring the publisher script to our remote machine as well.

So as you can see, it's actually working as suspected. And now we have the first part done. So this is it for this video. I'll see you in the next lesson.

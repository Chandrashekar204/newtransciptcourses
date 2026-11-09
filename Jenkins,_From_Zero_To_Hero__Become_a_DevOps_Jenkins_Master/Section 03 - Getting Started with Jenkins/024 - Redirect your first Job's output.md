# Redirect your first Job's output

*Section: Getting Started with Jenkins*

-: Hello and welcome back. In this video, we're going to learn how to redirect output in Jenkins. So, in bash, remember, that you are going to be working with bash, because in the job definition if we go to configure, we will find a Shell. So a Shell is exactly the same thing that your bash command. Please, again, remember that we are within the container. So, if you are not within the container go ahead and jump into the container with this command.

Cool. So, now, in bash we can use variables. A variable is nothing is like name, and for example, my name, Ricardo. Cool. So, if I now do an echo for name, I will have this value here. We want our Shell to say, "Hello Ricardo." The date and time is the output of the date command. How do we do this? Pretty simple. We do an echo and we say, for example, the variable with a dollar sign here which is the variable that we define up here.

Name. So, we say "Hello" to the name, and then we say "The current-" Let's say, "Current date and time is" the output of the date command. Pretty cool, isn't it? So we already knew how to do this, but this is something new using variables in bash. Okay, nice. If we copy and paste this for our Jenkins job, this is going to look exactly the same thing. Oh, but probably this is going to fail here because the variable doesn't exist.

So, we need to define the variable up here. Saying name equals to Ricardo. Cool. So, as you can see, this is exactly the same content that we wrote on our terminal. So, if you want to test a Jenkins job before running the job itself You can copy and paste the commands to your terminal, normally. Okay, so let's save this. And let's execute this job. So, we click on "Build now" and we are going to see what happened.

So, if we head to the build history, to the last execution, console output, We're going to see the output that we were expecting. So, it says "Hello Ricardo," current date and time is the output of the date command. Pretty cool. But now, what happens if we want to redirect that data into a file? So how do we do this? That's pretty simple. We put this sign, which is a redirection sign in bash, and then we give it a pad.

Like for example, "Temp". And we say " Info", for example. Hit enter. And, as you can see, nothing comes in the terminal as a response, but if we take a look on this file cat slash temp slash info, we're gonna see the content within the file itself. So, this is pretty cool. And we're gonna do this from Jenkins. So let's remove the file that we just created. And if we do a cat to this file, the file is no longer available because we already deleted it.

So, now let's copy this command for the Shell in here. So, let's click on configure. Let's delete our current configuration and let's paste the new one. And as you can see, we're redirecting this into a file. So, okay. Let's click on save and let's click on build now. If you see the build, let's go to the number, console output. And as you can see, the job actually finished as success. So now let's go to our container and let's look for a dot file.

And as you can see, it is perfect. The file is actually being created from our Jenkins job. So for example, if I remove the file again, I do a cut, the file doesn't exist anymore. But, if I build now, the job once again, it's going to be marked as succeeded. And if we open the console output, it says success. And if we take a look on the file, the file already exists because the job created it. And this is the important part that I wanted to tell you.

As we're using Docker to host the service, all of the files that we created are going to be saved within the container. So, if we go out of the container, and we look on cat temp info, we don't have that file because it's a completely different file system. But, if we go within the container, then we have the file. That's cool. And, remember, that your Jenkins container is a completely isolated process, with its own operating system and Linux distribution.

So that's why you can't see the file on your host. But, don't worry to solve that, if you want to share files with your host, you can use volumes. We're going to see that later. But, don't worry for now, just keep in mind that the files that you are creating are being created within the container. And, if you go outside of the container, you are not going to find those files. So, this is it for this video.

See you in the next lesson.

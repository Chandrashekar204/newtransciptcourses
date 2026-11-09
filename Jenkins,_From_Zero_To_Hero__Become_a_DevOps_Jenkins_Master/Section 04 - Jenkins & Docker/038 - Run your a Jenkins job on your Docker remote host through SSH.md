# Run your a Jenkins job on your Docker remote host through SSH

*Section: Jenkins & Docker*

Instructor: Hello, and welcome back. In this video, we're going to learn how to run a task, or a job, over SSH in our remote host. So, we already have configured these remote hosts. So the only one thing that we need to do is to create a job and test it. So let's click on New Item and let's give it a name. Let's say that it's going to be called remote-task, for example. You can call it whatever you want.

So let's click on Freestyle Project. Let's click OK. And, I'm pretty sure that you are now a little bit familiar with this screen. And now, in the build section, let's look for Execute shell script on remote host using SSH as you can see here. So we're going to choose this. And as you can see, this has a dropdown with all the credentials, with all the hosts that we have configured. So far, we have only configured one SSH side on the Configure Jenkins section.

That's why it's only coming up one. But if you want, you can create more. So, we already specified that we want to run this command on this host. So let's do the same thing that we did previously like name, Ricardo, and let's run something like Echo, Hello, name, current date and time is the output of the date command. Cool. So now we're going to redirect this in a file, let's say temp slash remote file.

So now I have a question for you, and that question is what do you think that's gonna happen when I save this job, and when I view this job? What do you think that's gonna happen? Where is the file going to be created? Is it going to be created in the Jenkins container, or is it going to be created outside of the container, or is it going to be created in the remote host container? What do you think that's going to happen?

So let's click on Build Now, and let's find it out. Remember that we name the file like slash temp slash something, like remote something, I don't remember. So let's click on Console Output. And as you can see, the name is slash temp slash remote file. Cool. So this output tells us that this SSH script already started, here is the execution, and it completed successfully. So, okay, let's go to our terminal.

Let's go ahead inside of the Jenkins container. And if we look for this file, let's see if we have this file. And the answer is no, we don't have this file. Hmm. So let's look outside of the container in here. Let's have a look and find out if this file exists in here. Nope, this doesn't exist here. So this only marks one possibility, and this one means that the file should be in the remote host. So let's go ahead into the remote host bash.

Let's look for that file. And, as you can see, the file is created in the remote host as we were expecting. So what did just happen here, and that's pretty simple. Remember, we created a connection. We configure that connection over SSH from Jenkins to that remote host. So, from Jenkins, we're connecting to this host through the SSH plugin, and we're running the task which is a simple task that creates a file on that remote host.

So, this is it for this video. I'll see you in the next lesson.

# Deploy: Execute the deploy script in the remote machine

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello, and welcome back. In this video, we're going to learn how to execute the script that we just created in the remote machine. Remember that so far we have this script that is transferring the auth file, and it's transferring the publish file that we just created. And if you take a look at this file, you are going to see that this is the file that the remote machine needs to start the container, or to create the container.

So, how do we execute this from Jenkins? Well, this is going to be simple. We're going to execute it using SSH. Probably, as I told you, in your real life, your process of deployment could be a little bit different because instead of SSH, you could be using AWS, which already has a CLI client. And you can do like AWS CLI deploy something. You should know how to do your deployments manually at least.

But for this case, we're using Docker Compose and SSH to deploy everything. So what we're gonna do now is that we're going to go to our Jenkins deploy, deploy SH. And in SSH, you can execute commands in remote machines using this line. Let me show you SSH-I, you pass the path of your key, then you pass the user at the machine where you want to connect to. And then in here you can execute one command in that remote machine.

So in this case, we want to execute this script that we're just transferring. So as you see, we're transferring those files. And finally, to deploy the application, we're just connecting to SSH, and we're executing that script that we just transferred in here. So let's save this, and let's execute this script so you can see the output. So let's click on this, hit Enter. And now this deploy file is going to start transferring the auth file, then the publish script.

And finally, it's going to execute this script that we just transferred using SSH. And as you see, this is the lock of that remote machine because with this line from here, we are telling that remote machine to execute this script that is going to deploy the application. Cool, so in this way, the only one thing that we need to do to deploy our application is simply execute this command or this script to deploy our application in that remote machine.

So, this is it for this video. Please make sure that you understand everything that we have done so far because this is going to give you a clear understanding of what we're doing, and it's going to help you to create your own workflows for your real applications. So, I'll see you in the next lesson.

# Trigger your Jobs from Bash Scripts (No parameters)

*Section: Jenkins Tips & Tricks*

Instructor: Hello and welcome back. In this video, we're going to learn how to trigger a Jenkins job from a script. So the first thing that we're going to look is how to trigger a job that doesn't ask for parameters. So for example, if we go inside of the environment job that we created, we can just click on this, and this is not going to ask for any input and this is just going to do the execution.

But the thing is a little bit different when you have to pass parameters. So we're gonna leave that for the next video. In this video, we're going to be covering how to trigger a job that doesn't have parameters. So let's take this environment job as an example. And if we go here, to the Build Now button and we click on copy link address. We do a right click, copy address, and we paste that in here.

You're going to see that this is how actually the job is being executed. So we can use this URL to trigger the job but we also need to pass something like a token. So let me show you. I'm gonna go to the Jenkins Home, Manage Jenkins, and Configure Global Security. In here, if we scroll down a little bit, you're going to see something which is, or is it, here! CSRF protection, which is something like prevent cross side requests, you know those attacks.

And this actually uses crumbs. So we need to retrieve a crumb. We need to create a crumb, which is something like a token. And you're gonna use that token when calling the job, in order for your script to work. So how do we generate this crumb? Well, I'll leave you this file, don't worry, I will attach you to the resources, and this is how you create the crumb. Let me copy this in here. I'm just gonna copy this.

I will go to my PuTTY or WIN2 terminal and I'm just gonna paste this in here. As you can see, we're actually using the curl command, which is a Linux command that allows you to do requests, http or https request. In here, we're passing the user that we created in the previous lesson, which is Jenkins user, column, and the password. And then this is actually silent, which means that it's not going to print any output.

And then we're going to pass the Jenkins, URL. And then if you can see this endpoint, don't worry about this endpoint, it's going to be constant. But this is the endpoint that you need to hit in order to retrieve the crumb. So here is going to happen something. And remember that if I hit the Jenkins, that local, from my machine itself, probably is going to have an error because we don't know what our Jenkins.local means for the machine.

We actually created the record on our Windows machine. So in this case, we need to create a record and the virtual machine outside of the containers to be able to reach Jenkins.local. So for that, we're gonna copy this and we're gonna do a sudo vi /etc/hosts, enter, give the password 1234, and then you're going to pass 127.0.0.1 and then you're gonna paste the name in here. So whenever you do that, and if you do a curl again, you're gonna find out something in here.

And if you do a :8080, now you are able to resolve this. So cool, if you hit again this crumb, let me just show you, I'm just gonna remove the parenthesis from here and this all. If you do this and you hit enter, let me remove this. You are going to see that Jenkins actually returns a crumb. So let me execute this back. And you see an answer in here. So this is the crumb or the token that we're going to be using in the requests.

But what happens if we want to save this, I would put in a variable. Well, we actually do something like crumb, for example, equals, and you know, we execute that command inside of the variable. So the output is gonna be saved on the variable. So if we do an echo to crumb, you are gonna find out the value there, which is pretty cool. So, okay, now that you have the crumb captured with this command, you can access that crumb using this.

Cool. So now let's go to our Jenkins job, which is the environment job. And we're going to look for the last execution, which was the number five. Let me reload. And yes, the number five was the last one. So we're gonna trigger a new one from here. So let's take a look to the file that I'm leaving you in here. And we're going to be using the first one, which is this. So we're going to create a sample script.

Let me just go ahead and create a scripting here, like, for example, crumb.sh, and you know, bin/bash. And in here, we're gonna copy the first line, which actually retrieves the crumb and saves that into this variable. And then we're going to use this. So let me copy and I will show you. So the second line is actually doing something similar. Another curl that this curl is actually passing as a authentication, the Jenkins user with the password, 1234.

And then we pass as the header, the crumb that we captured previously. And then we do a post. So we can just go to the job and do a right click copy link address. And if we paste that in here, this is the URL that I'm using here. So as you can see, this is how you trigger a job from a script. You only need to retrieve the crumb and then pass that crumb doing a post to the full URL that you already captured which is the job/env.

So let's save this. So you can see this in action. We're gonna save this. We're going to give this executable permissions. And let me show you that in here, we only have five executions. And if we now execute our crumb script and you hit enter, you are going to see that a new execution appears in here. And that is because your script is actually doing what you are telling it to do. It's retrieving a crumb, and then it's passing that crumb in the header and triggering the environment job that you are providing in here.

And if we go to the console output of this, you're going to see that the Jenkins user was the user that actually triggered this because we're passing the Jenkins user as the one that is going to do the job. You can execute that as many times as you want and every time that you execute it, your job is going to be executed as well, as you can see. So this is how you execute Jenkins jobs from a script without parameters.

I'll see you in the next lesson.

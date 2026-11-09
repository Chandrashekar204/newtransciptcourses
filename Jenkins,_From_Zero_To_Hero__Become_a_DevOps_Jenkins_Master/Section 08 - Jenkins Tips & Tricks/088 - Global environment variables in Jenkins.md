# Global environment variables in Jenkins

*Section: Jenkins Tips & Tricks*

Instructor: Hello and welcome back. In this video, we're going to learn about the global environment variables that are by default, available on Jenkins. So if you go to Google, and then you look for Jenkins Environment Variables, let's look for Jenkins Global Environment Variables. But let's look for the Wiki. Okay, so let me remove this global in here. Okay, cool, this is what I'm looking for, Building a Software Project.

And once you are here, you are going to see that there is a table where you can find a list of environment variables. So these environment variables are available in all the jobs that you run. For example, let me create a new job in here, and we're going to call it this as ENV. And we're going to say that this is a freestyle project. So let's hit in OK. And in here, we're only going to add a basic execute shell step.

In here we're going to do a BASH echo, and then we're gonna start passing these variables. So for example, the build numbers relates to the build number of the execution. So for example, let's say, build number for this is, and then we pass the variable is build number. Let's use some quotes in here. And we're going to do exactly the same thing with another variable, which is, for example, the build ID, and we're going to say build ID is this.

And then we're going to say the build URL is this. Build URL is this, so on and so forth, using all the variables that you want because all of these variables are available. So let's look for, what is it? Job name, job name is job name, okay. I think this is pretty cool only to test. So we're gonna click on the Save button. And as you can see, these variables that we define in the job, we are not defining them anywhere.

I mean, Jenkins is actually providing you the value of those variables. So if you hit the Build Now button, and you go to the execution in here, we're gonna go to the console output. You are going to see the value for this. So build number for this is number one. That's correct, as you can see here, number one. And as you can see, this is the build URL, it means your current IP, the port/job, the name of the job, and the number of the execution.

And then you have the job name is ENV. So what is this useful for? Okay, let's imagine that you are going to send an email or something. You're going to notify someone that the job with this number and with this name and with this URL is failing. Then you're going to be using these environment variables to notify. So don't worry about mail for now because we're going to have a section explaining how to send notifications from Jenkins.

But for now, just keep in mind that you can use any of these variables in any of your jobs to do anything that you want. So if you wanna print a message at the end of your execution, so for example, the execution number, and then you look for the execution ID or the build ID or the build number is number one. Or for example, the execution for the job. And then you pass the name of the job as a variable job name.

The execution for the job, job name was success. Or you can use it for whatever you want. I just want you to know that these variables are by default available globally, so you can use them at any time. This is it for this video. I'll see you in the next lesson.

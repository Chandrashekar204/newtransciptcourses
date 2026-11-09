# Timeouts

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video we're going to learn about timeouts. In the previous video, we learned about retry. Now we're gonna learn about how to time out a task that has taken more than expected. So let's take a look at the timeout file that I will leave you in the resources and we have this, everything that we know. The name of the stage can be anything that you want. And in these steps we have here one retry, which is just for testing, because you already know how to use retries.

And then we have a new one, which is time out. Then we say, okay, we want our task to time out in three seconds. So we define the time here, three, and the unit, it's going to be seconds. So we say here, we want this task to time out in three seconds. And as you can see, we're actually doing a sleep five. If you don't know, sleep is Linux command that allows you to sleep for some seconds. So if you say sleep two, this is going to be a stack for two seconds.

And that's it. So let's go ahead and take a look at how this works. Let's copy this code. Let's go to our pipeline configuration. Let's scroll down. Let's delete the old one and paste the new one in here. And we're going to save it. Let's build it and see how it looks like. Well, and as you can see, it actually changed its appearance, that probably it's going to fail. It was averted, as you can see here.

So let's go inside of the console output for this and you are going to see that the echo hello is actually working good with our retry because echo hello is a valid command in Linux. So our retry wasn't executed. Now, in the second step, we had something like the timeout. Remember? The sleep command, we set the timeout for this task to three seconds. And as the sleep took more than three seconds, then Jenkins actually terminated this automatically, marking the job as averted, because the timeout has been exhibited.

So this is how you use timeout in your jobs, because probably in the future you may find something that gets stuck or that takes more than expected and you wanna control that. If something takes more than expected, then just avert it. So this is it for this video. You already know how to use a timeout instruction in a Jenkins file. I'll see you in the next lesson.

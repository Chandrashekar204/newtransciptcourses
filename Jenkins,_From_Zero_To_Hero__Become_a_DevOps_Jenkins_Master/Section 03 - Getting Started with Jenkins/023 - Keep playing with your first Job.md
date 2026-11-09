# Keep playing with your first Job

*Section: Getting Started with Jenkins*

Instructor: Hello, and welcome back. So in this video, we're going to be playing with our job, the job that we created in the previous lesson. And I just wanted to tell you that you can go to the Jenkins home whenever you want clicking on the Jenkins button here. So we're going to click in the name of our job, and we're going to go into the Configure section. And as you can see, we're again presented with this screen that has all of the configuration.

And this is our current configuration. So we're going to make this job more dynamic. In Linux, we have a cool command, which is the date command. So, let's head to our virtual machine. Let's go inside of the container. Remember that we are outside of the container because if we type docker ps, we can see the container. So we're going to go to the container, docker exec -ti jenkins bash. And in here, we are within the container.

As you can see, the screen looks different. So if we type the date command here, as you can see, we have an output. And that output is nothing else but the current date and time. So, this actually returns the command. But what happens if I want to execute this command and I want to have text with this command? For example, I want to say, "The date is," and then I want the result of this date. So how do I do this in Linux?

That's pretty simple, you use the echo command. And then you type your string. Like, for example, "Current date is," and then you want to execute the command. So how do you execute the command? You put a $ here, and then you put parenthesis. And within the parenthesis, you type the command that you want to execute. For example, date. And as you can see, it says, "Current date is," and it returns the value of the date command, which is pretty useful for doing whatever you want.

So I could say an order or command like whoami, for example. And I could change, you know, the command, and I want to say, whoami, for example. And as you can see, it's actually giving the same text but returning different values based on the command that I'm executing here. So let's keep it like this, with the date. "Current date is," this. Let's say, "Current date and time." Cool. So this command is actually awesome.

So we're going to copy this command. And as you saw here on the job definition, we have a shell. So this shell is actually the same shell as this one. So you can freely copy and paste the command that we typed in the previous terminal in this terminal, and this is going to work the same way. So let's click on Save. And once you have that configured, you click on Build Now. And then you go to the job.

Console Output. And then you see the output of this, which says, "Current date and time is," the output of the command. Cool, isn't it? So for example, here, you are saying a 37, which is the second. So let's hit Build once again. And let's see if there is any difference. We're going to go here into the Build History. Job number four. Click on Console Output. And here, you are going to see that the day actually changed, the second change.

So this means that Jenkins is actually been executing the command whenever we ask for it. So this is pretty cool. You already know how to use Linux command within your Jenkins job and print it with text, which is pretty useful sometimes. So I'll see you in the next lesson.

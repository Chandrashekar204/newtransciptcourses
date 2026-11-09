# Missing the colors? Colorize your playbooks' output

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. As you may have noticed, whenever we build a job, there is no color in the output. And you may be wondering why. If we build that job, the exact same job from the Jenkins container, we have an output, but why don't we have any type of output in our Jenkins job? That's a good question. So if we build this in here, for example, playbook, we hit Enter, you are going to see colors in here.

Here, Ansible is complaining because we didn't pass the message variable, so don't worry. But the thing is that we have colors in here and the Jenkins, we don't have any colors. And that's because to be able to color the Jenkins standard output, we need to install a plugin. So let's go to the Manage Jenkins and let's go to the Manage Plugins. And now we're going to look for the Available tab. And in here, let's search for AnsiColor.

And as you can see, this actually allows us to print color to the output of the Jenkins jobs. So let's click on Install without restart. You know, all the process. Let's click this button, so Jenkins restarts whenever the installation finishes. So this is going to take some seconds. I will see you once it has finished. Great, the installation already finished. If you want, you can go ahead and verify it.

Click in on Manage Jenkins and then look for your installed plugins. But for now, we're just going to go to the ansible-test configuration. And remember that we still don't have colors in here, but if we want colors, we need to go and configure this, yeah, because we already installed the color plugin, the AnsiColor plugin. So once we are here, we're going to look for the Build Environment again. And we're going to click this, which says ANSI color map.

And we're gonna leave it like this. Please make sure you click on this. And then we're going to look for the Advanced Section and we're going to click on Colorized Standard Output. This is everything you need to have colors on your executions. That's pretty simple and it's worth it. So let's click on Save. And now we're going to build our playbook again. So let's build with parameters, and we're gonna say, for example, Hello! I now have colors.

And let's click on the Build button. Let's click on the number of the execution, Console Output, and let's wait for the colors to come up. Great, so now we have colors, we have green colors, and we're going to have all of the Jenkins colors, like red for errors, yellow for warnings and stuff like that. But as you can see, this is working like a charm, and this actually looks pretty cool. Using this little plugin to colorize the standard output it looks even better.

So this is it for this video. You already know how to color your output whenever you execute your playbooks. I'll see you in the next lesson.

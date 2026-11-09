# Learn how to install Jenkins Plugins (SSH Plugin)

*Section: Jenkins & Docker*

Instructor: Hello and welcome back. In this video we're going to learn how to install plugins in Jenkins. So the first thing that we're going to do is that we need to make sure that our machine, our virtual machine, has internet connection. So if we do a ping, google.com, it should work outside of the container or inside of the container. You should have an answer like this. So please make sure that you can reach internet before trying this.

Okay, so next what we're going to do is that we're going to click on Manage Jenkins. And here, let's click on the Manage Plugins section. And then we have here a couple of options. So the updates means the plugins that we have installed but you know, that are updates for these plugins. The available plugins means all the plugins that are available that we haven't installed yet. The install plugins means the plugins that we have already installed.

Okay, so let's go to available here, and let's look for SSH. So if we look for SSH and then we hit enter. You are going to see this plugin. This is the plugin that we want to install, SSH. Cool. So we're gonna mark this and then we're going to click on install without restart. Cool. So once we do this, what's going to happen here is that Jenkins, it's going to download the plugin and it's going to install it as you can see.

It already installed it, success. So now we need to restart Jenkins in order to test our plugin. So let's click here. Well, it says Restart Jenkins. And as you can see here, Jenkins, it's going to restart automatically. So the only one thing that we need to wait is until Jenkins finishes restarting. So let's hit here the Jenkins homepage and you're going to see that Jenkins is restarting. So as you can read, your browser will reload automatically when Jenkins is ready.

So let's wait until this happens. Great. The restart process already finished. So if we go again to Manage Jenkins and then we click on Manage Plugins again, and we click on the Installed Plugins, we should see our SSH plugin. So let's look for SSH here. And if you scroll down, you're going to see the SSH plugin correctly installed, which is pretty cool. So in this quick video, you learned how to look for an available plugin and how to install that plugin in Jenkins and then how to verify that the plugin was correctly installed.

So in the next video we're going to learn how to configure this plugin in order to set our authentication over SSH. So see you in the next lesson.

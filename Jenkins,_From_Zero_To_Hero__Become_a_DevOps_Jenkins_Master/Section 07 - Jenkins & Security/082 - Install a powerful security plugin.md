# Install a powerful security plugin

*Section: Jenkins & Security*

Instructor: Hello and welcome back. In this video, we're going to learn how to install a security plugin. So Jenkins is actually powerful in security terms, but by default it's actually a little bit weak. So we're going to tweak it using a custom plugin that actually has a lot of functionalities and works like a charm. So for that, let's go to Manage Jenkins and we're gonna go to the Manage plugins.

And you already know how to install plugins. So let's go to available plugins and we're going to look for a role-based strategy plugin. So let's filler using role. And as you can see, we have Role-based Authorization Strategy, which is pretty cool. So we're gonna click on download without restart, you know and now we're just gonna click on restart Jenkins when installation is complete. Let's click on that.

And as you can see, it's actually downloading things. So this may take a while or some seconds. I will just pause the video and I will come back once it has finished. Great. The installation already finished, so you know how to check that out. So we're gonna go to Manage Jenkins once again. We're gonna go to Manage Plugins. And let's see in the installed tab if our plugin was successfully installed.

So let's look for roll. And as you can see, our plugin is correctly installed. So we're gonna go to the Jenkins section. We're going to look for Manage Jenkins and we're going to go to the Configure Global Security. And we're going to make a small change in here to tell Jenkins that we want to delegate the authorization stuff to the new plugin. So if we go here to the Configure Global Security under Authorization, you're going to see a new option which is Role-based Strategy.

So we're gonna click on this and we're gonna hit on save. And after you do this, if you scroll down a little bit, you're gonna find out this new section which is Managed and Assign Roles. And this new section is because of the plugin that we installed. And in future videos, we're going to be learning how to manage and design roles. So this is it for this video. You already installed a security plugin and now you're going to learn how to use it.

I'll see you in the next lesson.

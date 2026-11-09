# Create a remote machine to deploy your containerized app

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. At this point we're going to be creating a new virtual machine because that's going to be the target machine. We're going to deploy the container in our application in that machine. So that's gonna be like our production machine. That's just for you to understand how to deploy code to a remote machine. So you have two options. You can just go ahead and create a new virtual machine in VirtualBox, as we have already done.

Make sure that you can SSH that machine using Putty or whatever you are using so far. So I already have one machine created. So let me open up this. I actually created a machine using AWS that you can simply create another virtual machine the same way that you created a virtual machine for the laboratory. It could be a Santos, it doesn't matter. So please make sure that your machine has Docker Install and Docker Compose as well because we're going to be using it.

You already know how to install Docker, how to install Docker Compose. If you don't remember, you can just simply go back to those lessons, to the initial lessons and take a look at how to install the virtual machine, how to create it, how to install Docker, and how to install Docker Compose. One important thing is that you should be able to log into your machine using a key file. So once you create your virtual machine, please make sure that you install Docker, that you install Docker Compose because that's gonna be our production machine, and we're going to deploy the application there.

And after you have everything up and running, you will need to set up a user to connect using a key file. So the first thing that you probably want to do is to do something like user at Jenkins or any user that you want because that's gonna be the remote user, let's say prod user or something as you want. And once you create that user, then you need to create a key file. So please go inside of your Jenkins machine and generate the key there.

So how do we generate keys? It's using SSH Key Gen, and then we say dash F. We give it a name like Prod or something, and we hit enter and then enter enter. And then you're going to have one prod file and one prod pub file. So we're gonna take a look at the content of the prod.pub file, and this is the key that the user that you created in your new virtual machine is going to have. So let's head to that virtual machine again.

Remember, this is gonna be our deployment machine our target machine. So in here, once you have created the user, remember that you already copied this content that you just generated in your Jenkins machine. In this machine, we're going to become this user so sudo su prod user, and here we're going to CD two /home/prod-user or the name that you've provided in here. So hit enter, and right here we're gonna create a new Directory called SSH.

We're gonna change permission to 700 to that directory. And instead of this directory, we're going to create a new file, which is gonna be called authorized keys. And inside of this file we're going to paste the content that we generated in here. So let's copy this content, and we're gonna paste that right here. Okay Let me remove this. We're not gonna be using this, remove it and okay save it. Once you've saved this, you need to change permissions to 400 to this specific file.

And that's it. So now let's go out of this remote machine. Remember that this is the virtual machine that we created, probably using VirtualBox or something. Let's go out of this machine out again, out again. And now as you can see, I'm on my local computer. So now we're gonna try to log into this machine using the key that we just generated. So remember that you created two files, the prod file and the prod.pub.

you're gonna log into that machine using the prod file. So let's take a look at that file, and we're going to copy this content and you're going to paste that content in a plain file text don't worry. So let's say like vi prod, let me open it with a different aider because this actually complains using bin. So let's say nano prod. And we're gonna paste that in here. We're gonna save that file. And as you can see here, well here we have our prod file just created.

So if you cut that file, then you have exactly the same content. So we're gonna be using this file to log into our machine. So we're going to do next SSH-i Well, let me look for the entire line. We're gonna specify here the prod file that we created which is the key, the user, it's gonna be prod user. This is the user that we created remotely at the IP of your virtual machine. So please graph the IP of your virtual machine and use it to connect to it.

So hit enter. And as you can see, we have here a warning, and that's because we need to change permissions to this key. So let's do like change mode 400 and we're gonna pass the name of the key file, and then we're gonna try again. And as you can see, we just connected to this new created virtual machine without a password using a key file in a user that we just created. So this is super cool. Remember that you can test all of this in your Jenkins machine.

So you can always do that inside of here. You can generate all and you can test everything from your Jenkins machine. So this is it for this video. Please make sure that you create your virtual machine using VirtualBox or whatever you want, but please make sure that your machine contains CentOS or the distribution that you want. But it should contain Docker. It should have Docker Compose installed, and it should be able to log in without password exactly like this.

So this is it for this video. I'll see you in the next lesson.

# Start building your Lab - Install CentOs

*Section: Introduction & Installation*

Instructor: Hello, and welcome back. Okay, here, we already downloaded our image. Please be sure that the image that you download it's going to be a CentOS 7, as you can see here, and that it is a 64 version, as you can see here. So, okay, once we have this image, what we're gonna do is that we're gonna create a virtual machine using this image and VirtualBox. So let's go ahead and open up VirtualBox.

We're gonna click on New, then we're gonna give it a name like Jenkins, or you can name it as you want. We're gonna say that the machine is Linux. I think we don't have CentOS here. No, we don't have, so we're gonna use Red Hat. As I told you, it should be 64-bit, so we're gonna choose this one. We're gonna click Next. We're gonna give it, for now, I think two gigabytes for RAM, so we're gonna click Next.

We're gonna create a hard disk now, because we don't have any hard disk. We're gonna click on Create. We're gonna click on Next, here. Next, and we're gonna give it, I don't know, let's give it like, 20 gigabytes. Okay, so let's click on Create, and, okay, we have already our machine created. So let's go ahead to Settings, and let's go to Network. Once we are here, we need to define which adapter we are going to use.

So we can use, as you can see here, a lot of adapters. For this course, we're gonna be using the bridged adapter. So we have a, in this dropdown, as you can see here, a lot of adapters. These and these are virtual adapters, so we don't want these ones. We could want this or this. The first one, which is ethernet, or the last one, which is wireless, depends on you. So for example, in this course, I'll be using the ethernet connections, which means that my computer is always gonna be connected to the network using a cord or a wire.

It means that the connection is going to be always this ethernet connection. Or if you know that your computer is always using Wi-Fi, then you should bind your virtual machine to the wireless. It depends on you. Please make sure that the connection that you specify here is always active whenever you turn on your virtual machine. So for now, as you can see here, I will be choosing ethernet connection, then clicking Okay, and then we're gonna click on Start.

So after we click on it, our machine is going to boot up, it's going to start, and we will need to select a startup disk. So as you may guess, we're gonna use the ISO that we downloaded previously. So we're gonna go into Downloads, and we're gonna look for CentOS. This is the one that we downloaded. We click on Start, then, okay, it's powering up. As I told you before, if you are not using Windows, then you can just skip these videos and use your Linux desktop, but if you have Windows, then you should keep with these videos.

Okay, so what we're gonna do here is that we're gonna use the arrows of the keyboard to select Install CentOS. Once we're here, Enter, and we wait. So let's wait until something appears on the screen. Cool, as you can see here, you have the welcome page, and you have, in this left side hand, you have the language. So we're gonna use English for this course, and here, let's just click on Continue. So this is cool, once you click on Continue, then we're going to have this screen here where we need to configure a couple of things.

As you can see here on the software selection, this is specified as a minimal installation, cool. Then we go into the installation, we're gonna click on here, and we're gonna use the automatically partitioning, because it's okay just for testing, so we're gonna click on Done, and then we're gonna go into the network, and we're gonna see the ethernet adapter that we created before, and we're gonna just turn this on.

As you can see, it actually retrieves an IP, and we're gonna use this IP address in the future. So for now, we're done with this. Let's click Done. And finally, after we've configured everything that is needed, we're gonna hit the Begin Installation button. So we hit this, and then we're gonna create our root password. So for now, I'm just gonna say 1234, 1234, okay, and we're gonna click on Done twice.

Okay, now, I don't know if we need to create a user. Let's create a user. Let's say that I wanna create a user, which is gonna be called Jenkins. Okay, let me, Jenkins, and we're gonna make this user an administrator, because we want this user to be able of using Sudo. So we mark this, and then we're gonna give it a password. We're gonna say 1234 again, 1234, and then we're gonna click on Done. So now, the only one thing that we need to do is just to wait until this installation gets completed, and after that, we will have our machine ready, so we can start playing around with Jenkins, Docker, Amazon, and more.

So let's wait until this installation finishes. I will pause the video, and I will come back once it has finished. Cool, so these already finished. So the only one thing that is left is that now, we need to click this Reboot button, and then our machine is going to reboot. So let's hit it, let's click on Reboot, and then we need to wait until the machine boots up, and then we're gonna be ready to start playing around with Jenkins.

See you in the next lesson.

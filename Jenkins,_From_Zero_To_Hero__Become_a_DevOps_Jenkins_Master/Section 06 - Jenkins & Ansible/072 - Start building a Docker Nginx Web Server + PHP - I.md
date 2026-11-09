# Start building a Docker Nginx Web Server + PHP - I

*Section: Jenkins & Ansible*

Instructor: Hello, and welcome back. In this video, we're going to learn how to create our web server that's going to hold the site where the HTML table is going to be displayed. So, cool. As you may guess, we're going to create that server using Docker as we have been doing so far. I already created a folder, a web folder, inside of the Jenkins Ansible directory, so I'm just gonna change directory to that directory.

I already created the configuration for the Docker file and the stuff that we need, and I'm going to explain it to you, because if I start typing, then it's going to take us a lot of time, and I don't want you to see me typing, right? So I'm gonna explain to you how I view the Docker file. So let's take a look to the Docker file that I have in here. I think that you're already used, or at least a little bit, to the Docker file syntax.

So as you can see, we're starting from that remote host. So we're doing exactly the same thing that we did in the Ansible installation from Jenkins. Now we're doing from remote host, and remember that that remote host image is the image that we created to start the SSH service. So as a base, the resulting image from this process is going to have a remote user created, the key file created, it's going to have SSH installed, because remember that if we go two levels back to the CentOS 7 and Docker file, this is the Docker file for that remote host image.

So this new image is going to have all of this installed, and we can do that only by putting this as a from. So we say from remote host, and automatically, we're going to have all of this configuration, because remember that if we do a Docker images, we already have this remote host created, so Docker is only going to take this as a phase, and that's it. So let's keep taking a look to this Docker file.

The second thing that I'm doing here is that I'm copying this nginx.repo, which is in a folder, to the etc/yum.repos.d/nginx.repo. So if I take a look to this file, cat nginx.repo, you're gonna see that this is nothing else but a sample yum repository. But if you don't know how to do that, you can just do something like nginx centos repo file, and then it should be right here. Actually, I took everything from internet, so as you can see, this is exactly the same file that I have in here, so this is it.

You can just Google, and then you're going to find everything. This way, we're enabling the nginx repository so we can download the package from there. So, cool. Second thing that we're going to do is that we're going to install nginx in here using the nginx repository. You can just Google a little bit about how to install nginx in CentOS, and then you're going to find exactly these lines. So then, we have nginx installed.

We install PHP packages from a repository, which is centos7.iuscommunity. So if you go to Google, for example, and then you look for CentOS ius repo phpfpm7 and you hit enter, then you are going to see, let's see what we have in here. We have CentOS 7 packages. There are actually a lot of packages that you can choose, so if you wanna choose them all, then go ahead, but I actually chose the ones that we're going to be using in here, which are these ones.

So finally, we're doing a yum clean all, which is going to clean the temp files and data stuff. Cool. Here, we're exposing the ports that we're going to be using, then we're creating volumes for the HTML and for the log folders, so if the container dies, then we can have this information secure. This line, actually, I'm just going to remove it because it didn't work as I thought. I'm just gonna remove it because it's doing nothing here.

And then we have another copy here, which is an nginx configuration. So if we take a look to that, conf/nginx.conf, you're going to find this. Don't worry if this looks difficult, because I took it from internet. So if you go to google.com and you type nginx vhost php example, because remember that we need to configure nginx to use PHP. So if we browse the first result, let's see what happens. Let's look for an example in here.

As you can see, I actually took this, and I modified a little bit of things like the root, the index server name and all of that. In this case, let's go ahead and modify the nginx.configuration, because the server name's not going to be localhost, it's going to be jenkins.local, which is our Jenkins server, because remember that we have a local VNS pointing to the IP of this Jenkins server, so whenever we hit this name, we're actually hitting the virtual machine IP address.

So this is going to be cool for now, and in this section, we're defining where nginx is going to find the PHP service, and you can see that in the example on the internet. So here is the example. That's pretty cool. So let's take a look to our Docker file and see what's left. Finally, I'm copying a start script, which is going to be the CMD, and that script is nothing else but a sample script to start the services.

So here, we start the sshd service, because remember that we're starting from the remote host, and that service is already installed there. Then we start the PHP process in the background, and finally, we start the nginx daemon. So this container is going to have SSH, it's going to have PHP, and it's going to have nginx. So that's pretty cool. You already know what this Docker file does. In here, we are just giving executable permissions, and finally, we're defining the script as the CMD.

As you could see, it was a little bit long. That's why I didn't type that in here because it could take a while and could be a little bit boring. So this is it for this video. I'll see you in the next lesson.

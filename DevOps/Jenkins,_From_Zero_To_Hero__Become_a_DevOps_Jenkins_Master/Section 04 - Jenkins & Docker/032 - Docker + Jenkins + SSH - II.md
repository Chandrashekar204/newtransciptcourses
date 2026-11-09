# Docker + Jenkins + SSH - II

*Section: Jenkins & Docker*

Instructor: Hello and welcome back. In this video we're going to keep configuring our Docker image in order to spin up an SSH service. Remember that if you want, you could create a virtual machine in VirtualBox maybe used in CentOS or whatever you want. But the thing is that we want to connect from Jenkins to that remote machine and then we want to run commands over SSH. For simplicity and for you to learn a little bit of Docker, we're creating a Docker image and then we're going to create a container based on that image.

So this is what we are doing here. Okay, let's keep it like this. For now, let me save this file, and now we need to create a private key, an SSH key. Maybe you have heard about SSH keys, and SSH keys are a mechanism of SSH to make connections in a more secure way. So to create an SSH key, it's pretty simple, you just need to type ssh-keygen, and then you give a name for the resulting file. So in this case, let's give it like remote-key, for example.

Then you hit Enter, you hit Enter, Enter, two Enters. Leave the password empty for now. And then you're going to have this output. So if you see here, this process actually created two files, a remote-key which is a certificate key. This is a private key. And this is going to be another key, which is a public key as you can see. So please for real environments keep this remote-key secure. And this public key is as the name suggests, public.

So okay, to make a connection through SSH using these keys, we're going to copy this name, the pub name, and we're going to open up again our Docker file and let's keep modifying this. So let's create a COPY instruction, and what this does is to copy a file from our file system to this image. So in this case, we're going to copy the file that we created which is the remote-key. We're going to say COPY remote-key.pub, which is the public one.

And we're going to copy this to this folder, that's why we created this folder. So we're going to copy this and then the final file, it's going to be authorized_keys. So, okay, in this line we're copying the key that we generated before in this location within the image. Cool. So now we need to make sure that this user that we created, remote_user is the owner of everything that is under this folder.

So for that, let's run a Linux command which is called change owner, and we're going to say that the remote_user that we created and the group remote_user that is created by default in Linux when you create a user it's going to be the owner recursively of this folder. So we're saying, hey, everything under this folder, it's going to be owned by this user. Cool. Now we need to give more permissions like this and we're going to say we're going to change the permissions for this file that we created here.

So we're gonna give these permissions to the file that we copied to this path and then we're going to say, okay, this file is going to have 600 permission. And remember that the folder is going to have 700 permissions. Pretty nice. So I think we already configure everything for this user. Now what we need to do here is to RUN as we're going to create this server from scratch. SSH needs to create some global keys, and that is created by using the command usr/sbin/sshd-keygen.

And that's it, as simple as this. Normally if you read a guide to install a open SSH server maybe you can find it, maybe you won't find it. But anyways, for a Docker container, this is needed. Cool. And now the last part or the last thing that we need to do for our service to be alive is certify as CMD. This all is Docker configuration remember. FROM instructs which operating system we're going to take as a base.

RUN, run commands. COPY copies files from our host to the image. And CMD is a new command, and this actually instructs which command the container should run. It means which command needs to be executed in order to start the SSH service. So for Linux, that command is /usr/sbin/sshd and -D. As simple as this. So in this order of ideas, we already have our base, we installed the server, we configure a user with a password with a home folder, an SSH folder, and we give permissions, and we copy the public key that we generated.

We are generating some keys for SSH and then here we're just instructing Docker how the service should be started. And that's pretty cool. So this is it for this video. I'll see you in the next lesson. A file.

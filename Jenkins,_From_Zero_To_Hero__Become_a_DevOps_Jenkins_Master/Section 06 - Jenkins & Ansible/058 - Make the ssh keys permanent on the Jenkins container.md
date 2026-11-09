# Make the ssh keys permanent on the Jenkins container

*Section: Jenkins & Ansible*

-: Hello and welcome back. In this video, we're going to be using SSH private key files again to use in our connections through SSH. So remember that if you go to your Jenkins data folder we're outside of the container in this case, and you look for your centos7 folder, let's go to that folder. You are going to see that remote key file and that remote-key.pub file that we created. So we're going to be using these files again because we already created them and we already configured them, so let's use them again.

Now, there's an important point in here and it's that these keys should be accessible from the Jenkins container because now Jenkins needs to read these files. So how are we going to do it? Well, it's time to start learning how to share files between a container and between your host. Cool. So let's go to the main directory where we have our docker compose file and let's take a look to our docker compose file.

So let's look at the Jenkins section here. And as you can see we're telling Docker to save all the content of /var/jenkins home inside of the container to our local folder, which is jenkins home. So let me show you, if we do an ls here you are going to see your jenkins home folder in here. So if you type an ls you're going to see a bunch of files in here. So let's go inside of the container exec -ti jenkins bash and if you type cd, for example, home and then you type pwd you are going to see that this is the directory inside of the container where all the information for Jenkins lives.

If you type ls, you are going to see exactly the same files that are in the folder on your local machine. So let's test it and let me create, remember that we are inside of the container in this path and let me create a file which is going to be called ricardo, for example. ricardo1234, enter. And if we look for this file, this is it. Cool. Now, if we go outside of the container now we are in our local machine.

If we go to the jenkins home folder jenkins underscore home and we look for the file that we created, which is ricardo1234. You are going to find the file there. Pretty nice, but why? Remember that again, if you take a look to your Docker compose file, which is one folder back cat docker compose file, you will see that your local jenkins home directory which is this one it's actually been mapped to this folder inside of the container and inside of the container this folder contains all the information for Jenkins.

That's why if we create a filing here then it's going to appear in here. It's because this folder and this folder are exactly the same folders. But here, this is the location for our local machine and this is the location for the container. So keeping this in mind, we're going to create a folder on our jenkins home directory. So let's type jenkins, for example, home and then we're going to type ansible.

So we're going to create a subdirectory which is going to be called ansible under the jenkins home folder. So remember as this is a volume for the container it means that everything which is under jenkins home it's going to be in the Jenkins container. We can log into the container, go to cd home and then if you look for ansible you are going to find the folder that we created. Pretty cool. So please make sure that you understand this important part about volumes.

And if you have any dot, please watch the video again. Okay, so let's jump to save the key that we created to the container. Remember that we're doing this because we want to store this remote key in the container and in the host at the same time. Remember that in this case, we're in the same level of our docker compose file, which is this path. So let's copy from the centos7 directory, that remote key.

We're only going to need this file. So let's copy this to our jenkins home ansible folder that we created before, hit enter. And now if you take a look to your jenkins home ansible folder you are going to see the file in there. Cool. So let's go inside of the container. Let's do exactly the same thing. You know, go to the home directory and then if you type ls for the ansible folder, you are going to see the file there.

And this is exactly this file, so this is pretty cool. Now, if we remove the container or if the container dies or something, the key's always going to be here. The key's not going to be deleted unless you delete that key manually. But if the container dies or if the container gets destroyed then your key is going to be saved. Because remember that we're mounting our local volume to the container which is going to persist all the information that is living in here.

So this is it for this video. I hope you've learned a lot from this and I'll see you in the next lesson.

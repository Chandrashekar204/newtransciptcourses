# Install Ansible: Docker + Jenkins

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. In this video, we're going to learn how to install Ansible and we're going to run it in a Docker container, which is going to be pretty cool. So, okay, if you have never heard about Ansible before, don't worry. We're going to be covering every single step in here. So let's look for install Ansible pip , Linux, for example. And remember, or if you didn't know it, Ansible is like the AWS client that we installed before.

This is a Python library, so we can install this using pip. So let's click on the first result in here and we're going to look for latest releases with pip. So as you can see, this is pretty simple. The only one thing that we need to do is like pip install Ansible, which is quite simple. So, okay, knowing this, we're going to go to our Jenkins data directory. Remember that at this moment, we're out of the container.

So if you take a look on your current directories and then you see your CentOS7 Dockerfile, remember that we did something similar in here. We're installing pip, well, downloading a file, then installing pip with this command and finally using this new command, which is pip and installing the package that we want. So we can actually use this instruction to install Ansible. Okay, cool. So we're going to be working with Ansible in Jenkins.

So our Jenkins container, it's going to need Ansible installed. So if we go inside of the Jenkins container in here and if we type Ansible, we don't have Ansible installed. So we need to install it. So for this, let's create another directory, which is going to be Jenkins Ansible. Let's head to that directory in here. And as you may guess, what do we normally use to create a new image? I know you know it.

And this is a Dockerfile. So let's create a Dockerfile in this folder to create our new service. So, okay, here we're going to do something cool. Remember that always in a Dockerfile, we need to start with a from instruction, which tells Docker which image to pick as the base. So in this case, we're going to be using the Jenkins image. Remember that we used this image to create our initial container running Jenkins.

So once we are doing this, we're telling Docker, "Hey Docker, please take this image as a base." So at this point, in this Dockerfile, we already have all the full Jenkins image in here with all of the configuration and all the stuff needed for Jenkins to run. Now in here, there is a cool point and if you go, let me show you. If you go inside of the Jenkins container, you are going to see that the user in this case is the Jenkins user, which has 1000 as an ID.

Cool. But if you go to the remote host container, you are going to see that the user in this case is the root user. And as you may know, the root user has all the superpowers to install things on the system, but the Jenkins user probably will not have those superpowers and it's going to complain about permissions. So let's get out of this container, out of all of the containers, actually. We're outside.

And now keeping in mind what I told you, we're going to modify our Dockerfile. Remember that currently we're in the Jenkins Ansible folder that we created. So let's go and modify the Dockerfile that we created and let's run the user instruction. And this is something new for us. And in a Dockerfile, a user instruction means which user is going to be executing the commands. So in this case, we want the user route to be executing all of the commands that we're gonna pass in here.

So what are we going to do? We're going to look for the Dockerfile in the CentOS7 directory, the Dockerfile that we created to install Amazon CLI . So let's copy this line. Let's open our Dockerfile and let's paste that in here. Pretty cool. As you can see, we have all what we need. We have the Jenkins imaging here, the user route and now we're downloading this script, then running this script. And now we need to change this Ansible.

Pretty cool. So remember that we modified the user as the user route. So now we need to leave things as they were before. So let's type user again and let's put the Jenkins user back. So cool. This Dockerfile is actually instructing Docker to start from the Jenkins image, change the user to the root user around these commands to avoid permissions problems and then switching back to the Jenkins user.

Pretty cool. So let's go ahead and save this Dockerfile. Right? And now what we need to do is that we need to modify our Docker Compose file. Remember that our Docker Compose is the file that holds all the definitions for our services. So in this case, we're going to do three things. The first one is that we're going to create a new image, which is going to be called Jenkins Ansible, for example. You can name it as you want.

And we're going to do something similar to this. So we're going to tell Docker, "Hey Docker, please build this new image using a context." And what is that context? As in this case, the context means the folder where the Dockerfile that we created lives. So let's look for that folder, which is Jenkins Ansible and then you're going to see the Dockerfile there. Cool. So let's copy the name of the folder.

Right? Copy. And then we're going to go to the context section. Let's paste this in here. And that's it. So we're telling Docker, "Hey Docker, please for the Jenkins service, you are no longer going to be using the Jenkins/Jenkins image. Now you are going to use a new image, which is going to be built by me, and you are going to build that image using this folder as a context. It means that the Dockerfile should be under this folder.

So pretty cool. Let's save this. And remember, we need to do a Docker Compose build which tells Docker, "Docker, please read my Docker Compose file and build all the features and all the configuration that I instructed you." So in this case, as you can see, our Dockerfile is being run. We can see the from instruction here that we defined, the user root here. It's downloading the pip stuff and installing Ansible as well.

So this is pretty cool. We only need to wait until this finishes. And this is awesome. As you can see here, the installation, everything completed successfully, which means that our Dockerfile was correct and now everything is working. Cool. But remember that we still need to recreate the Jenkins container in order to use our new configuration. So to do this, we need to do docker-compose up -d, which is going to recreate the Jenkins container using the new image that we created.

Please remember to run this command inside of the folder that holds the Docker compose file. You should be at the same level of this file to avoid errors. So this is it. Let's go ahead inside of the Jenkins container and let's look for the Ansible command. Ansible enter. It now doesn't show any errors. Instead it's showing you how to use Ansible and which flags or options you have available. So this is pretty cool.

We already installed Ansible in Docker and in the Jenkins container> So we can now run playbooks in here. Cool. This is it for this video. I'll see you in the next lesson.

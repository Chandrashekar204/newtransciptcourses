# Create a Docker Compose file for Jenkins

*Section: Introduction & Installation*

Instructor: Hello and welcome back. The first thing that we're going to do is that we're going to create a directory which is going to be called Jenkins. You can create it wherever you want. In this case, the path is slash home Jenkins and Jenkins. As you can see here, I just created a directory here. If I do an ls here is the directory, and the full path for that directory is the current directory plus this path.

So let me just rename this directory because you may be confused. So let's rename it and we're going to call it Jenkins data, for example. So the full path for Jenkins data, it's going to be ls home Jenkins and Jenkins data. Perfect. This directory is empty as you can see because we haven't created anything but we're going to create things. Okay, we created the directory. Now we're going to move into that directory.

We don't have anything here, but we're going to create a sample Docker Compose file. So we type vi docker, compose dot E M O. This is important. This name is pretty important, so please keep it like this. And vi is a text editor for Linux. So we're gonna hit enter, and then we're going to start typing the Docker Compose file. Before doing this, a Docker Compose file is like a script. It's a definition.

So here we're going to define which services we want to spin. So in this case, for now, we want to spin a Jenkins server. So we're gonna start with this file. So we say version three. That's the current version of Docker Compose, don't worry. And now we say services. So in services, we're going to define our Jenkins server. And this Jenkins server will have some properties. So we can define the container name.

Container name, and we're going to call it Jenkins. Simple. Now we're going to define the image. So we say image. And then the name that is going to go here is the name that we downloaded in the previous video. So we type docker image, and here we have the name. So we're gonna copy this name. We're gonna open up again, our Docker Compose file and we're gonna paste this in here. Cool. Oh, a pretty quick tip.

If you don't know how to exit off this screen this is pretty simple. You hit escape, then you hit shift, and the colon key. Then you press W and Q, which means write and quit. So we hit enter and you already quit. Cool. So, okay. We already defined the container name and the image. What else do we need? I'm gonna leave you this template here and this template you can actually just copy and paste it if you want, reuse it, or you can manually type it.

There is not a problem. So we're gonna define the ports. What are the ports? So we're going to say ports and we define an array of ports. So we're going to say that we want to expose the port of Jenkins using the port 8080 on our machine and we're going to map that port internally to the container on port 8080. Don't worry, we will take a look on this later. What else do we need? We need a volume.

What is a volume? Okay, you must know that in Docker, when you create a container, when you spin up your service, all the data which is within the container is going to be destroyed if you don't save that data into a volume. So we'll say volumes here in this case, and we're gonna say okay, we want to create a folder, which is going to be called Jenkins folder. So let's use the current path for now.

We're going to say P W D, which means P W D, the current path, and we're going to create a folder, which is going to be called Jenkins home, for example. And we are going to map this folder. Okay, first we need to create this folder in our machine. So we're gonna copy this and we're gonna go out of bim and we're gonna create a directory here. So we click mkdir home, make sure you don't put dir slash, mkdir Jenkins home.

Hit enter. And if you do an ls, you should see your Jenkins home folder at the same level of the Docker Compose file. So, the full path for this is the PWD which can be represented with this variable. You do an echo. Oops. So this is the current path plus your folder, the folder that you have just created. And this is the full path as you can see. Okay, so we're gonna go back to our Docker Compose file.

And we already defined this. This is the host volume. Now we're gonna map it to the container. So how do we do this? Within the container the Docker image uses this folder to store the file. So we're gonna copy this location we're gonna put a colon here and then we paste this location. So we're saying, okay, Docker, please whatever you write here, which is going to be all of the files for Jenkins, please save those files in this directory that I have just created.

Cool. And now we need to define a network. So we say we want this to be in the network net but we haven't created the network net. So let's go here in the same text file at the same level of services, we're going to create a section which is going to be called networks. Networks, we put a colon and underneath of this we're going to create a net network. So, okay, we're saying, please, Docker create a network using this instruction which is going to be called net.

And then we're going to use this net here and we're gonna include the Jenkins server or the Jenkins service within this network. So that's pretty cool. I think this is everything we need. We're gonna save this file and we are done. So let's recap what we just did. And if we do a cat in the Docker Compose YAML file, we're gonna see that we're using the version three of Docker Compose, we have defined a service.

Its name is Jenkins. The container name is going to be Jenkins. The image that it's going to use is the Jenkins slash Jenkins image. It's going to export the port 8080. It's gonna save all the information in this folder that we created. And this is going to bind the service into a network which is called net. And this network is being created here.

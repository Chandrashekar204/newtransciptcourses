# Hands On! Create your first Jenkins Job

*Section: Getting Started with Jenkins*

Instructor: Hello and welcome back. Okay, in this video we're going to create our first job. It's not going to be a huge job. It's going to be pretty simple because it's our first job. In the future, we're going to do more interesting things. So to create a job, we can either click here or create a new item. So let's click on the create new item. And now we need to give you the name. So let's say that we want this job to be called my-first-job.

So we say my-first-job, we're gonna click on Freestyle project, which is a simple project, and we click OK. After this, you are going to see this screen with all of this configuration, don't worry. I know it could be like overwhelming or something, but it's pretty simple. So the first thing that we're going to do or the first thing that I want you to keep in mind is that a task is in Jenkins called a job.

So you are probably going to see everywhere, people using the concept of job. And a job is nothing else but a task, something that is going to be done, that's a job. So we're configuring here a job or a task, but the concept in Jenkins is a job. So here in the Build section, we're going to Add a build step, and we're going to look for Execute shell command. So I wanna show you one thing and this is that this shell refers to our virtual machine but not entirely to our virtual machine.

Remember that we created a container in here and this container actually has the Jenkins service app and running, but if we look in our machine, I mean outside of the container, there is no Jenkins server. We don't even have Java installed as you can see. But if we go inside of the container doing docker exec -ti jenkins and asking for a Bash terminal, we hit Enter, and if we type Java, you are going to see that we have Java installed here.

We can even do a java -version, and we have Java installed within the container. So let's make this clear. We have our virtual machine, which is nothing else but like the house of the container and the container which can be listed using docker ps is the service itself. So as you can see, when we do a docker exec, the terminal actually changes its appearance. For example, let me create a file, touch, hello, /temp/hello, you are going to see that this file is going to be created only within the container hello.

But if we go out of the container and we look for the same file, this file doesn't exist. So please keep in mind that everything that's going to happen on the Jenkins job will occur within the container, I mean within the docker exec -ti. It's not going to happen outside, not here, but everything that we run, every command, anything, it's going to be running within the container. It's time to start running our job.

So let's say Echo Hello World, which is, you know, the most popular quote for beginners in technology. So let's click on Save here and after we save, let's click on Build Now. The Build button means building a project. So for now, if we go here, Console Output, we are going to see that our job executed successfully, printing a Hello World. So remember what we just did is to create and configure a job.

We added a step here, a shell step, and then we said the command, Hello World. We Save this, and then we clicked on the Build Now button. So here we have a Build History. We can just go into the number of the execution that we want to know. We click on the Console Output and then we have this output, which means that the job executed correctly. So you already created your first job. Cool, remember, this job is being executed within the container, not outside.

So having said this, see you in the next lesson.

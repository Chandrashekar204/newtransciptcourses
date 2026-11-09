# What is a Seed Job in DSL?

*Section: Jenkins & DSL*

Instructor: Hello and welcome back. In this video, we're going to learn about the seed job and well, you must know that the seed job is nothing else but a job. And that job actually creates new jobs. That's why it has this name. So this is a seed. You configure all of the jobs that you want to create inside of that job and then that job is going to create all of those jobs. So we can say that the seed job is like the parent job of all the jobs that are going to be created.

So let me show you. If we create a new item, let's call it like job-dsl or whatever you want. Freestyle project, let's click on okay. And then if we scroll down a little bit to the build section and we add the build step, let's look for process job-dsl. In here, as you can see, we have two main options. Use the provided DSL script or look on the file system. So this look on the file system is going to load a file on the Jenkins container file system.

And this is going to allow us to type in here the configuration manually. So for now, we're going to be working here and then we're going to use this look on the file system. So the thing is that you define all of the configuration in here or in the file that you define. And then whenever you execute this seed job or this current job, all of the content in here is going to be executed and therefore everything that is defined here is going to be created.

So this is this simple. We're going to be learning more about this in the next videos.

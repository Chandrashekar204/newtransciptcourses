# Version your DSL code using Git

*Section: Jenkins & DSL*

Instructor: Hello and welcome back. In this video, we're going to save the code that we created in Git. So let's go ahead and create a new project. And this new project is going to be under the Jenkins group that we already created. And we're going to call this DSL Jobs or as you prefer. And let's click on create this project. Now that we have this project created, it's time to grant permissions to the user, Ricardo.

So let's go to Members and let's add that Ricardo user in here with maintainer permissions. Let's click on Add to Project, and that was good. So if you go to your Jenkins group, you're going to find that now you have two projects, the Maven project that we created in the past, and this new project where we're going to save the DSL jobs that we're going to be creating. So let's click on this DSL Jobs.

And now we're going to scroll down and we're going to copy this clone command. And we're going to go here to our terminal. Let's go to the same level of the Docker compose file. Paste that in here. So the first thing that we need to do is to add the port 8090. And remember that we can pass the credentials in here to avoid passing interactive input. So this is it. Let's hit Enter. And as you can see now we have this DSL Jobs, and if we change directory to that directory, we are going to see that this is empty.

So let's create a new file. Let's go to our Jenkins seed job, which is the job DSL. Let's configure this. And now we're going to copy all of this that we created. Let's copy that. Let's create a new file inside of this repository. Let's call it like jobs. Let's paste that in here. Let's make sure that everything is good, that we're not missing anything. Okay, looks good. Let's save this. And if you do git status, then you have your new filing here.

So let's do git add jobs, git commit dash M, and you are going to say add DSL jobs for example. And let's do a git push origin master, hit Enter. This is pushing. And as you can see, it was good. So let's go to our Git server. Let's refresh this. And as you can see now we have this file that holds all of the jobs that we have created so far. So in the next video, we're going to learn how to trigger the seed job using Git Hooks, because probably you don't want to keep going here, configuring, adding jobs, deleting this from here, probably you don't wanna do that.

So we're going to automate that process using Git Hooks. So whenever you modify it or you add a new job in this file, then the seed job is going to be triggered and it's going to download the new content and it's going to create the new jobs automatically. So that's what we're going to learn in the next lesson. So see you there.

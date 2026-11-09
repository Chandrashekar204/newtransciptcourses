# Create the Jenkins Pipeline. Finally!

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

-: Hello and welcome back. In this video we're going to create the pipeline for this project. So let's go ahead and create a new item. We're gonna call it like pipeline-docker-maven or as you want. This is going to be a pipeline project. So hit okay. And in here we're going to say in the pipeline configuration that we want to download it from our SCM. So remember, the SCM is going to be Git and the repository URL is going to be this URL right here.

Let's go to the pipeline-maven and this is the URL that we're going to be using. So let's copy that. Let's paste that in here. And remember that this is going to be internal communication. So, we're going to be using Git on port 80 and we're going to add the Git here. Cool. So now it says that we are not authenticated. So let's pick up the credentials of the user, Ricardo which is allowed for that repository, the master branch.

And that's cool. And the script path, it's going to be Jenkins file. Because if you take a look at the root of your repository you're gonna see that this is the root and this is the Jenkins file. So this is the file that we're going to read. We're gonna save this configuration in here and we are done. Now, I just want to tell you something and it's about the workspaces. Remember that if we go to our machine to our local machine and we browse to Jenkins data here we have a folder, which is called jenkins home.

So let's go to this folder. And in here you have all of the content that the Docker container is using. So let's go to workspaces. And as you can see, we don't have a workspace for this job because we haven't built this job yet. So if we build now this project then the workspace is going to be created right here. You have the workspace that was created for your job. Probably this job is going to fail because we still need to do some things.

But I wanted to tell you that in every single execution this folder is created. I mean, this folder is created for the first time and the code is being downloaded in here. So pipeline, oops. I mean, this is the project that we created. And if you go there then you see the code that was downloaded in here. So let's go to the field history console output and you're going to see that the cloning of that repository was successful.

But anyways, we, it actually failed because of some things, that in here. Remember that the code has been downloaded and the code has been downloaded in this workspace which is on Jenkins, which is at jenkins home workspace in the name of the job that you created. So please keep in mind that in this workspace is going to occur, every single thing we're going to download the code there the scripts are going to be executed from there and all the stuff is going to be done from there.

So this is it for this video. I'll see you in the next lesson.

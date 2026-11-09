# Upload the code for the Java App in your Repo

*Section: Jenkins & GIT*

Instructor: Hello and welcome back. In this video, we're going to add code to our new repository. So for that, let's go to Google and let's look for Maven sample app, the same product that we created before. We're gonna look for this, and we're going to clone this in our machine. So let's click on Clone or download. We're gonna copy this name, and then we're gonna go to our terminal. Let's go to the jenkins-data folder.

Remember that we're outside of the containers in this case. And now if you type git and you hit Enter and you have this error, it's time to install this git command for Linux, this package actually. So let's type sudo yum -y install git, and hit Enter. And then this is going to install the git client for your Linux distribution. So you only need to wait until this finishes, and then you're going to be able to use the git commands on your terminal.

Okay, pretty nice. Now we're gonna clone the code from GitHub. So let's go to GitHub. Let's copy this URL. And we're going to clone it, but before cloning it, remember that now I am at the same level of the Docker file. So we're gonna clone this using git clone and the URL that we copied it. So let's hit Enter. And as you can see, this is actually going to create a folder with this name. So let's look for it.

And you're gonna find out this folder in here. So this folder actually has the content of the GitHub repository. If you look inside of that folder, you're going to find the same files that we saw before. These files are the files that are in here in the Git repo on GitHub. So now that we have the code from GitHub in our machine, we need to upload this code to our GitLab server. So if we go here to our GitLab and we click on the Maven product that we created, and if you scroll down a little bit, you're going to find out how to clone this repository.

So let's copy this command, which is a git clone. We're going to go to our terminal. And here at the same level of the docker-compose file, we're going to paste that in here. And as you can see, we have an error that says gitlab.example.com couldn't resolve the name. That's because this DNS GitLab doesn't exist in this virtual tool machine. We created this record in the Windows machine, but we haven't created this on the virtual machine.

So we need to go and do something like vi /etc/hosts, and we need to create a new record so we can reach that DNS. And we're going to do exactly the same thing. We're gonna point this record to our local host. So we're gonna save that. And now we're gonna try to clone this again. And as you can see, now we have a networking here, and that's because we need to specify the port 8090 in here. Remember, that's the port that we have been using.

So we need to define that there, and we hit Enter, and then it's going to ask for input. But if we want to do this automatically, we can hit Control + C, and then we're gonna pass the credentials in here. So we're gonna say, like, the user that we created, 12345678, which is the password at the Git server. And if you hit Enter, you're going to see that the repository is automatically cloned. So if we do an ls, you're gonna see that repository in here, which is the maven repo.

But if you go inside of that folder, you're gonna find out that it's empty. So we need to populate information in here. So for that, we're gonna do a cp from the simple-java-maven-application, and we're going to copy everything from here into this directory, and we want this to be recursively because we have folders. So if we do this, what you're going to see is that now we have the README, the jenkins, and the pom, and the source, and all the files that are here in this GitHub repository.

So now if you do a git status, then you are going to see that these files are new files. So we need to add these files to our Git repository. So let's do git add, and we put a dot in here, and that means that we're adding everything. As you can see, this is a new file. So we're going to do something like git commit -m, and we're going to say Adds maven files or something like that. And then you do git push origin master, and hit Enter.

And as you can see, we're actually uploading that code to our Git server, to our Git repository. So if we now go to the browser to our Git server, and we reload this, you are going to say that these are the files that we actually uploaded 29 seconds ago and this is the commit, the message that we included, and these are all of the files. So that's pretty cool. Right now you have all of the project, the Java project in your Git server.

So that's pretty cool. Now we're going to integrate this repository to our Maven job so we can retrieve the code from here instead of retrieving the code from GitHub. So this is it for this video. I'll see you in the next lesson.

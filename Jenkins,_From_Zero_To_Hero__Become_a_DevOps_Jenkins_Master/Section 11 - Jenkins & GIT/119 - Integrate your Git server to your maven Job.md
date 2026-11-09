# Integrate your Git server to your maven Job

*Section: Jenkins & GIT*

Instructor: Hello and welcome back. In this video, we're going to modify this maven-job in order to retrieve this code from our Git Server. So we're going to configure this maven-job to fetch all the code or to clone all the code from our Git Server and to build, and to do all the entire process that we're doing, but now, with our code. So as you can see, if you go and configure your maven-job, you're gonna find out that you are using the GitHub code.

So now, we wanna change that because we want to use this repository instead of using the GitHub one. So for that, the first thing that we need to do is that we need to create a user, because remember that this repository has authentication. So let's go to Credentials. Let's click on Jenkins, global credentials, and we're going to add a new credential. And this new credential is going to be a username with a password.

So the username is going to be the Git user that we created, which is Ricardo. The password is going to be the password for that user, which is 1, 2, 3, 4, 5, 6, 7, 8. And the ID is like whatever you want. So I will call this like git_user, and then we click in Okay. So after that, we can go again to the maven-job, we can configure that again. And now, if you go to the Source Code Management, and you click on Credentials, you're going to find your credentials that you created there.

So that's cool. Let's pick that one. And now, we need to change this URL. So let's go ahead and delete this. And we're going to use the maven URL. So you know that the maven URL is this one, but it must end with dot git. So it's like this URL.git. But now, we need to do a couple of changes in here, because remember that this clone is going to happen inside of the Jenkins container. Because if you go to your docker-compose file, let me go out of here, and if you take a look to your services, you can see that you define your Git service as git.

So that means that your Jenkins container or your DB, or your remote host, they all can reach each other using these names. So if we go inside of the Jenkins container, and we try to do a curl, for example, to gitlab.example.com, you're gonna find this error, "Couldn't resolve host." But if you do a curl to git, you're going to find an answer. So same thing if you ping, ping gitlab .example.com, you're going to find errors.

But if you ping the Git Server, you're going to find an answer. So this is the cool part of using networks, because whenever you use a network, you're actually creating an internal communication between the containers and they can reach each other using our internal DNS. So that's nice. So let's go and modify this. Okay, this is Git, but this port is not correct, because if we take a look to our docker-compose file again, you're gonna see that this is the external port, and this stands for the internal port.

So if we do exactly the same thing and we log in inside of the Jenkins container and we try to do a curl to git on port 8090, you're going to find out errors. But if you do a curl using the 80 port, you're going to find an answer, which is pretty cool. And that's because of this configuration, external port, internal port. And remember that when we are configuring this Jenkins Server, we're using internal communication.

So we should use the port number 80. So let's go and click on Save, and now, we are ready to build our project. So let's go ahead and build this. Go to the Console Output. And as you see, the first thing that this is actually doing is retrieving the code from the Git and the repository that is created there. And as you can see, it's downloading the last commit, which is, "Adds maven files." And that's correct because that was the commit that we did like 10 minutes ago when we uploaded that code.

And if we scroll down a little bit, everything else is going good because the structure of the repository is exactly the same structure. We're only downloading the code from a different source, but the code is exactly the same. So the package for the URL is actually working, the test is working and the deployment is actually working as well. So as you can see, this is how you integrate your Git Server with your maven-job in order to do an internal communication between containers and using authentication, of course.

So this is it for this video. I'll see you in the next lesson.

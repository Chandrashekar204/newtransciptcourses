# Intro - Learn how to Enable/Disable Login in Jenkins

*Section: Jenkins & Security*

Instructor: Hello, and welcome back. In this section, we're going to be talking about the security in Jenkins. So as you may know, security is an important concern for enterprises and for applications. So how do you make your Jenkins secure? How do you control who can access your jobs? How do you control authentication? How do you control security aspects? That's what we're gonna be covering here.

So the first thing that you need to know is that for now, by default, we have enabled the login security. So for example, if we open up an incognito for our browser, we're gonna go to the same location which is jenkins.local and it's going to ask for the username and a password. So for now, if someone wants to log in, then that person should have the password. So let's close this. And for example, if we want, we can change that, go into Manage Jenkins, and here we're gonna go to the Configure Global Security, and once we are in here we're gonna click on Enable security.

So if we click on this, we're actually disabling the security. So if we hit on Save and then we open up a new incognito window, then we're gonna go to the jenkins.local, and as you can see, it's actually going inside of the Jenkins service because it's not asking for login, which is not a good idea. So in this way, anyone who can access your IP is going to be allowed to do anything, deleting jobs, accessing to data, removing tasks.

Anything is allowed in here because by default, any user can do anything. So we don't want this, and as you can see, we even have a warning here. So let's get back to the Global Security and let's enable the login again. So let's click on this. We're gonna say that we're going to be using the Jenkins database, we're gonna uncheck this, and we're gonna say logged in users can do anything, in this case, authorization.

This is the default configuration so let's click on this, and let's uncheck this and let's save this. Okay, so for now, we actually reverted the changes that we made and we're now allowing users to log in normally. So if we open up a new incognito tab and we go to our Jenkins server, you're gonna see again the login authentication, which is pretty cool. So in these videos we're going to be learning about good practices, about how to create users, how to manage users, how to create rules, how to grant permissions to certain users, to certain jobs.

So that's what basically we're going to be doing here. So I'll see you in the next lesson.

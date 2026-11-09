# Create the Registry Password in Jenkins

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to create the password for the registry. Do you remember if we take a look at our push scripts, you will find out that we're actually using this pass environment variable, but this pass is not defined anywhere. So we need to define it in Jenkins as a credential. So let's go to our Jenkins, let's get out of here. Let's go to credentials.

Let's create a new credential and you can click as you want. So let's click on Credential. And we can say like this is going to be a secret text. So the secret is going to be 1, 2, 3, 4, 5, 6, 7, 8 which is my password for Docker Hub. The ID is going to be Registry Pass, for example. So in this way, we already created this registry pass, which contains the password for the login to Docker hub. And now we need to modify our Jenkins file.

So let's go to our Jenkins file, and we need to add that to our Jenkins file. So let's go here and say Environment. Do you remember how to add credentials? So that's environment. You need to open and close this, curly braces. And then you say, okay, I want this credential to be passed. Because remember that we're using this name in our push scripts. So Jenkins, push push. We're using this name. So we need to define this environment with that name.

So let's go ahead and say Pass. It's going to be credentials, and we're going to pull the credential that we just created, which is Registry Pass. And that's super cool. So now Git Status, and you can see that this Jenkins files modified. So let's add it Git Add Jenkins file. Oops. Git add Jenkins. And we're going to say Git commit dash M adds credentials to Jenkins file. And then we do Git push. Remember that always when we push, we can always go to our repository refresh.

And then you're going to see all of your commits in here. So if you take a look at this, you're gonna see the content of the file that you actually changed. This is it for this video. I'll see you in the next lesson.

# Credentials

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video, we're going to learn about credentials in pipelines. Let's think for a second that you need to handle sensitive information in your pipeline. Probably you don't want to put this in plain text. So how do you manage it? Well, let's take a look at the creds files that is in this folder and you're going to see that this is super simple. Well, we define an environment instruction in here and we define the name of the variable, and as the value we define this credentials function, and we pass the name of the credential that we want to get.

So we define a super-simple environment variable calling this credential function, passing the name, and then we simply call the secret variable. So let's go to Jenkins. Let's create a new Credentials in here, and let's click on global, let's click on Jenkins down here, let's click on global, and we're going to create a new credential. It's going to be super simple, so I will just create a secret text and that's going to be 1, 2, 3, 4.

And the ID for this is going to be, let's say, SECRET_TEXT. It's super important that you define an ID because you are going to be calling this ID when you call this function. So you say credentials and in this case, SECRET_TEXT. So let's go ahead and save this. Now we're going to go to Jenkins and we're going to modify our pipeline job. Let's configure this. Let's go to this box, delete the old code, let's paste the new one.

And remember that now we need to change the name of this which is the credential that we want to call. In this case, this is SECRET-TEXT. So now let's save this, and let's build this, and let's see what happens. And as you can see, we have an error. So let's go here. Console Output. And, as you can see, it says CredentialNotFound because probably I just, I don't remember the name. So I'm super-bad remembering things.

So this is SECRET_TEXT underscore, that's why. So let's go back. Let's go to Manage. Sorry, et's go to our pipeline project. Let's go to Configure, and then we're going to change this and we're going to be using the name that we created. So let's paste that. Let's remove this quote and save this. And we're going to build it now. And this time it was cool, it didn't fail. So let's go to the Console Output.

And as you can see, Jenkins is not displaying the content of your secret because that's actually a secret, and probably you don't want to display that to the entire world. So now you know how to handle sensitive data using credentials in Jenkins and how to use that using your Jenkins pipeline file. So this is it for this video. I'll see you in the next lesson.

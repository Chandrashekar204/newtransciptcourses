# Learn how to execute a bash script from Jenkins

*Section: Getting Started with Jenkins*

Instructor: Hello and welcome back. In this video we're going to learn how to execute a script from Jenkins. So to achieve this, the first thing that we need to do is of course, to create a script. So let's go ahead into our virtual machine. Remember that in this case we are adds out of the container because we're going to create a sample file. So if we go inside of the container as we have learnt this way, and then we type vi, which is a text editor, we're going to have an error.

And this is because containers normally only have what they need. So for example, in this case Jenkins only have packages regarding to Jenkins. It shouldn't have any other package like network tools or editors because a container is meant to do only what it's meant to do. That's why we're going to look out of the container and we're going to create the file here outside of the container. So let's create a simple script which can be called like script, that is H.

And remember that to type in Putty you need to press the letter I. Cool. So normally in Linux or when we are creating a script, the first line informs which interpreter are we going to use. In this case we're going to use bash. So that's why we're marking as being bash. Cool. So let's start with a sample script that is going to accept parameters and it's gonna print out the name and the last name for one person.

So this would be like echo, hello. And then it's going to receive the name of one person and then the last name of that person. So if we execute this script like this, what do you think that's gonna happen? If I just go ahead and do... And I try to execute this script, I will have an error. The first error in here. Okay, to fix this, we need to give executable permissions to this file. And to do so, we need to execute a command, change mode plus x, which is going to give executable permissions to the file.

Cool, then try again. And you are going to see that the only one thing that comes is the hello. So what we want to do is like, for example, we are going to call this a script like this, and then I want to pass my name and my last name in the script. So this, in this case, this should print this variables saying hello, name and last names respectively. So let's modify our script and let's add parameters.

So in bash, normally parameters are represented with dollar design, number one for the first parameter, dollar design number two for the second parameter, so on and so forth. So in this case, we're going to say that the variable name that we're mentioning here, it's going to be referenced as the first parameter. Cool. So we're going to say that the last name that we're referencing here, it's going to be the value of the second parameter that we are going to receive.

So let's do like this and okay Let's save this and let's execute this script again. And as you can see cool. It's actually returning the values that we are passing to the script itself. So cool. Now if we want to execute this from Jenkins, what do you think that we need to do? As I told you, we are outside of the container, which is a completely isolated and different file system. So our container can't see this file unless we copy that file to the container.

In the future, we're going to learn how to use volumes and docker to share data between the host and the container. But for now, let's just go ahead and copy the file that we just created to the container. So for example, let's say that we wanna copy this file, which is called script.sh. So we do docker cp, the name of the file that we wanna copy. Then the name of the container where we wanna copy and then we put a column and the full path.

So let's say that we want this to be called /tmp/script.sh. The full path. So if we hit enter and then we go inside of the container like this, and we take color temp, script, which is the location that we defined before, we're going to find these in here. Pretty cool. So we have our script here. So how do we execute this? Cool, we just take this full path and execute it inside of the container. And we are going to have an empty answer as you can see because we're not passing any parameters.

If we pass this, then we're going to have both of the parameters in here. So cool. Let's copy the path for this script. Let's go to our job. Let's click on configure and let's execute that script from the Jenkins shell. Do you know how to do it? So if you want, do it before I do it. Otherwise I'm just gonna do it right away. So it's gonna be pretty simple, as simple as this. We're just gonna copy and paste this, the path, and then we're going to pass the parameters as simple as that.

So we can just click here on save. And then if we build now, what's going to happen is the Jenkins is going to go to the file, read the script and it's going to pass the parameters that we are passing in the shell, and in the output, as you can see we have the expected output. Cool. So again, what happened here? Jenkins from its shell actually took the parameters that we passed and read them and at the same time pass those parameters to this script.

We can do it passing variables as well. So we could say like, name equals to my name and we could say last name equals to my last name. And then what we're going to pass here are the variables. So we say like, name and last name as you can see here. And the output should be exactly the same. So let's go ahead and save it. Let's go and click on the build button. And as you can see, we have an error here, which is pretty cool.

We made a typo. And what is that typo? Can you spot it? So that typo, it's pretty simple. We define as you see here, we define variables. But in this case, we have a space here, which is a problem. So if we go ahead and fix that and then we click on save, and then we build this now, we're going to see that this is going to be blue again. So what happens in Jenkins is that whenever and an execution fails, the color of the real history, it's going to be red and it's going to be marked as failed.

But if it doesn't fail, then it's going to be marked as success and the color is going to be blue. If we go into the console output here and we take a look on the response, we can see that we're defining the variable name, the variable last name and then we're passing those variables as parameters to our main script, and then the output is exactly as we were expecting, which is pretty cool. So okay, this is it for this video.

See you in the next lesson.

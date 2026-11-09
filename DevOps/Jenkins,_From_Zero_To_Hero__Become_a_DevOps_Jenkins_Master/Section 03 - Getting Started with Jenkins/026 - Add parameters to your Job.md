# Add parameters to your Job

*Section: Getting Started with Jenkins*

Ricardo: Hello and welcome back. In this video we're going to learn how to use parameters in Jenkins. So if you remember in the previous video we were creating parameters in dash. So we were passing those parameters, hard coded. So if we go to the configuration of our job and we take a look here, if we wanted to modify a parameter we would need to change the parameter to for example something like Tom and then last name which could be, I don't know, Smith, for example.

And then if I click on save and then I built now the job, the output that we could expect is something like hello Tom Smith. And that's perfect, that's what we were expecting. But what happens if we don't want to configure the job to change the parameter. We want to be able to dynamically set the name that we want to greet. So let's go ahead and configure our project. And in this part is where the concept of parameter in Jenkins comes into the rescue.

So if we go here in the first section, in the general section of the configuration for this job, we're going to see a lot of options here. But for now, we are just going to choose the option that says this project is parameterized. And then we're going to add a parameter which is pretty simple. We have a lot of parameters here. Don't worry, we will see them later. But for now, let's use a normal string parameter because for now we only want to pass the name and the last name for the person that we want to greet.

So let's say that we want the name to be name. So this means the name of the parameter. In this case, we want to call it as name. So let's call it different so you can see it. First name for example. And then we can give a default value if we want. If we don't want, then we just leave it empty. Let's go ahead and give it a default value with my name. And now we're going to add a second parameter, a string parameter again, and we're going to now use a second name of that person.

So it's a- oops. Second name. And then we can give it a default value. So in my case, let's give you my second name as you can see here. Cool. So there is something that I want you to check here. And this is the name. The name means the name of the variable, the name of the parameter. So we're going to be referencing this name in our scripts. So for example, we're going to say hello first name and then it's going to take this value.

And then we can say hello second name, and then it's going to take this value. Cool. So let's go down and let's modify our current configuration. Let's delete these old. And let's run a simple hello to the name that we are passing as a parameter. So we can say echo hello and then we're passing the first name parameter that we created. And then we can pass the second name parameter that we created.

So if you see these are the names that we're using, first name and second name. So cool. We are saying hello first name and second name. So let's go ahead and save this. And now if you see the build button already changed. It now says build with parameters. And what's going to happen, is before executing the job, Jenkins, it's going to ask for these parameters. So here is the first name parameter that we created and here is the second name parameter that we created.

So we can just leave the default values as you can see here and let's click on the build button. So if you see the console output of this you are going to see that- this is not the job. This is the 13th, my bad. So if you go here and then you go to the console output, you are going to see the hello Ricardo Andre which is my first name and second name. Cool. But what happens if now we wanna greet another person.

That's gonna be simple. We're going to say, for example, hello Tom and then the second name, I dunno, let's say Adam or something like that. And then click on build. And now, so you can see this is pending and cool. We already have this execution done so let's go to the console output. And as you can see, the name already changed only by modifying the parameter before executing the job. So building jobs with parameter is actually quite powerful because we can define the names or the variables or files or parameters that our script should execute without modifying the configuration of of the job.

So this, for example, we could define an environment like production here or dev or QA or staging or whatever. We can just create all the parameters that we want. But for now, let's keep in mind that a parameter is nothing else but an interactive variable. So before you build your job, Jenkins is going to ask you for these values in order to populate the information that is contained on this script that Jenkins is going to execute.

So this is it for this video. See you in the next lesson.

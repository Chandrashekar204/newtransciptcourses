# Environment variables

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video, we're going to learn about environment variables in our Jenkins file. So let's take a look at the end file that I will leave you here and you are going to see that it's super simple. The stages are the same. You define stages, your stage, and you have your steps in here. But here we have a new instruction, which is an environment. An environment, you can define these curly braces.

And instead of these curly braces, you can start defining all the environment variables that you want to use in your pipeline. So for this case, I actually created super simple environment variable which is my name and my last name. So you define the variable name equals to the value, and then you can reference those variables using just the dollar sign and the name of the variable. Super simple. So let's go ahead and copy this.

Let's copy, and let's go to our job configuration. Let's delete the old code and let's paste the new one. So let's paste that in here. Remember, in environment, one and two variables and then we call those variables doing a sample echo. So let's save that and let's view our pipeline right here. And as you can see, our execution was successful because we had nothing that could fail there. So let's go to the console output for this job.

And you are going to see Echo Ricardo Gonzalez, even though when you set name and last name. But remember that these values are being taken from these environment variables. So in here, name becomes Ricardo and last name becomes Gonzalez, which is my last name. So this is super cool. You already know how to create environment variables inside of your Jenkins file to do any kind of things that you need to do.

This is it for this video. I'll see you in the next lesson.

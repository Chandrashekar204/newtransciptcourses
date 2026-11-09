# Understand the DSL Structure

*Section: Jenkins & DSL*

Instructor: Hello, and welcome back. In this video, we're going to create our first DSL job. I mean, we already created the parent job, which is the seed job, but now we're gonna create something like a child. So if we go to our terminal, let's go to the jenkins-data folder. And I will leave you a folder in here, which is dsl, in the resources for this section. So if you go to that folder, you're going to find a lot of files in here.

I actually created all of these files for you to completely understand every single part of DSL. So let's go ahead and look to the easiest one, which is the job file. And as you can see, it's pretty simple. You call a function, which is the job function, and then you pass a parameter or an argument, which is on a string. And this string is going to have the name of the job to be created. So let's go ahead and modify this file.

And we're going to say job_dsl_created. Or name it as you want. And we're gonna save this. And if we go ahead and copy this content, which means we're going to create a job that is going to be called like this, and it's going to have an empty configuration. So let's copy this. And if we go to our seed job and we paste that in here, then let's go ahead and save this. And once we do this, let's build this project and see what happens.

And as you can see, the execution succeeded. And if we go inside of the execution, you're going to see that it generated job_dsl_created was successfully created. So if we go to our main window to the dashboard, you can see the new job that was created. And if you click in that job, then you're gonna see that the parent job, or the seed job, for this child is actually this job_dsl. This means that this job actually created this child.

So if you want to know where did I take these values from? Okay, let's go to Google. And we're going to look for jenkins dsl. Hit enter. And let's look for this jenkinsci.github.io. Let's hit enter in here. And you have all of the documentation in here for you to use. So if we click on job, you can see the examples in here. Well, it actually looks a little bit complicated because we haven't touched anything of this.

But if you see here, this is the most basic example, which means you call the job function, you pass a string, and an empty body, and then you're going to have an empty job. And if we go to the job that was created and we click on configure, what do you think that this job is going to have? Well, let's take a look. And as you can see, this job is actually empty. And that's because if we go to our file, we didn't define anything inside of these curly braces, which means that this job is empty.

So this is pretty cool. You already created your first DSL job. I'll see you in the next lesson.

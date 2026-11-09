# Description

*Section: Jenkins & DSL*

Narrator: Hello and welcome back. In this video, we're going to learn how to create a description for a job. I don't know if I told you that you can add a description to a job. For example, if you configure this job, you're going to find out here a field that allows you to add a description for this job. So for example, if you say something like, this is a test job, and you save that, that is going to appear under the main name.

And this only gives you an idea of what this job is about. So, okay, let's learn how to create a description using DSL. By the way, it's not a good idea to modify a job created by DSL because as you can see here, it says, this item has been changed manually. They should be modified using the job DSL, the seed job instead. So let's go to our seed job. Let's go here, and let's configure this job. And I will show you in the terminal a new file, which is a description file.

And here we have a new function, and okay, we're defining our job in here, and we're going to be working with this new job because I think that all the files have this name. So I just changed the name from the previous video for you to see that you can name it as you want, but we're going to be using this name, okay? So inside of the curly, braces you can add a description. And then you can pass a simple string telling what this job is about.

If you don't know where to find it, remember that you can go to the documentation and look for description, and you scroll down and look for freestyle job, you're going to see the same example or a pretty similar example. So let's copy this. We're gonna copy this. Let's go to our DSL, and let's paste that in here. And now we're gonna create a new job that is going to be a job DSL example, and it's going to have this description.

So let's save this seed job. Let's go ahead and build this. And as you can see, it was successful. So let's go to the dashboard. And as you can see now, we have this job DSL example in here. And if we click on it, you're going to find the Description field populated. If you go ahead and configure this job, you are also going to see the description in here as a configuration. So that's great. You already know how to add a description to a job using DSL.

I'll see you in the next lesson.

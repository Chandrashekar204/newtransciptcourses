# Steps

*Section: Jenkins & DSL*

Instructor: Hello and welcome back. In this video, we're going to learn how to add a shell execution in our job using DSL. So let's look at the steps file in here. And as you can see, we're keeping everything exactly the same. And now we're adding a new section which is the steps section. And this is nothing else but the option that you choose when you want to add a new step. So let me show you. If we go to this Ansible test and we click on Configure, then we scroll down a little bit.

And if we go to the part where it says build and we add a build step, and if you click on Execute Shell and then you have this prompt, this is what we're going to configure. So let's go to the dashboard in here, let's leave this. And in here, we're going to add a shell step that is going to say Hello World. So you say steps and inside of the curly braces you say, I want this to be a shell and I want to execute this Hello Word.

If you want to know more, remember you can always go to the documentation and you look for steps. Look for freestyle job, and you're going to find a lot of examples there. Always click this three dots and look for whatever you need. So for now, let's keep it simple. We're going to copy this all. We're going to configure our job DSL which is the seed job. Let's click on Configure. Let's scroll down and we're going to paste the new code in here.

Let's save this. And we're going to build this project. And as you can see, if we now go to our job DSL example and we configure this job, let's see what this has. Let's scroll down a little bit. And we have everything, the source code management, the triggers, everything is in place. And now we have a new step, which is executing a shell command that says Echo Hello World. So this is pretty cool.

But now what happens if you want to add more than one line? So let's go ahead and modify our steps file. And if we want to add more than one line, then we simply add three quotes in here. We hit Enter, and we finish this with three quotes. And inside of these three quotes, we can add all the content that we want. So let's put this in here and we can say, for example, Echo Hello World. And we could say running script.

And then we could run on a script like /temp/script.sh and that is going to be done. So let's copy this new code in here. Let's save this and we're going to go to the seed job. Let's go ahead and configure this and we're going to add the new code in here. So let's delete this. Let's paste the new one and let's build this and see what happens. So the execution succeeded. Let's go back and let's take a look at our job DSL example.

Let's go to Configure. Let's scroll down. And as you can see, we have all of the instructions that we define in our file, and they all are in the same shell execution. So you already know how to run a shell command, how to configure that in your job using DSL. So this is it for this video. I'll see you in the next lesson.

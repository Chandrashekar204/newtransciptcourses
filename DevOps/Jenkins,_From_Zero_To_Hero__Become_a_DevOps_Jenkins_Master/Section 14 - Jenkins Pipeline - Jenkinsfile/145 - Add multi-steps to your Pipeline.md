# Add multi-steps to your Pipeline

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video, we're going to learn how to execute real steps in our pipeline. So, let's go to our terminal and let's take a look at multiple steps in here. And as you can see, this is exactly the same thing that I showed you before, but now we only have one stage in here. So, in this case, we're only gonna be creating one. And that is going to do an echo "My first pipeline".

And then we're going to do more stuff here below. So, let's take a look at this. We can instruct Jenkins to use sh commands passing this instruction here, sh, and then inside of quotes we can say what we want to do. In this case, let's print a simple echo. Let's have another sh in here. And we can actually split this in multiple lines using three quotes. And this way you can actually have a lot of lines inside of these quotes.

So you can, for example, do another echo in here and you can use Linux commands like ls or, you know, all of the commands available in Linux. So, let's go ahead and copy this and see how it looks like. Let's go to our pipeline project. Let's go to configure it. And we're going to go to the ruby box. We're gonna delete this. We're gonna paste the new one. And let's save this. And let's build this now and see how it looks like.

As you can see, we didn't have this stages in our pipeline, so they are not marked as green because they didn't exist on the definition of our pipeline. But you only had one step, the build step. So, let's go to the console output, click on console output. And as you can see, we actually have every single thing that we defined in here. So, this is the first step of our build stage, echo "My first pipeline".

This is the instruction and this is the output. Cool. And here you have the second instruction inside of the same stage on the build stage telling you more things. Hey, "I can do more stuff in here" and doing a simple Linux command. And you have here the output of that command. So, this is super cool. You already know how to create more than one instruction in any stage of your Jenkins file. And you already know how to split it, how to use more than one line, how to use Linux command, and how to print things using the sh instruction inside of these steps.

So, this is it for this video. I'll see you in the next lesson.

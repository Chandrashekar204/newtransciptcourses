# Define the steps for your Pipeline

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to define the steps that our pipeline will execute. So you already know how to create a pipeline. So this is the file or the skeleton that we will be using. So here we have our pipeline. We have some stages in here. We only have four stages. The build stage, and for now we're just doing an echo build. We have the test staging here, we have the push stage and the deploy stage.

And as you can see, for now we're doing nothing but doing echo push, echo deploy, echo blah, blah. So our idea is to be using bash scripts or shell scripts to do all of the magic. So for example, if we're going to build something, we're going to write a bash script and then we're going to call that script from here so we can execute it. And then all of the content in that script is going to be executed.

Same thing in here. The idea is to create a script to keep this Jenkins file as simple as possible. And this script is going to do all of the magic. So we're going to be learning how to do this through this section. So don't worry. Now that we know all of the stages that our pipeline is going to have, let's copy this content and let's go to our terminal. Let's head to our pipeline directory. And in here, let's create a Jenkins file.

So let's create a Jenkins file at the same level of the docker file, Jenkins file. And we're gonna paste the content in here. So let's save it. And now as you can see, we have two files, our docker file and our Jenkins file. We're going to be using this in the future, don't worry. I'll see you in the next lesson.

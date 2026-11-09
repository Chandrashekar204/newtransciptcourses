# Introduction to Pipeline

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video, we're going to learn what is a pipeline? Well, probably, you already know what a pipeline is and a pipeline is nothing else but the entire workflow that normally it's executed when you are going through the CI/CD process. So as you can see, this is actually a pipeline. It starts with a pipe and it finishes with a pipe. So normally, the starting of the pipeline is when you are developing your application.

So you develop, you push, you do a lot of things to finally reach production, to finally deploy your application in production. So in the pipeline, you do a lot of things. You can do whatever you want to cover the things that you need to cover. I mean, to cover your field, your test, your deployment. You can create as many steps as you want. So let's take a look at this diagramming here that is actually in the Jenkins page.

You can go the jenkins.io/doc/book/pipeline, and you're gonna find this diagram there. Okay, so let's get started. Normally when someone pushes or commits something, the Git hook is triggered and the workflow starts. So whenever the workflow starts, you can have a lot of stages and a stage is nothing else than a step of your workflow. So your first step would be something like checking out your code, which means downloading the new code.

Remember that we have already done this in previous sections in the Java section, in the Maven section, even in the DSL section, we did a super simple workflow like this. And here we've got our checkout for our code, which means that we're going to download all the new code. Then probably we wanna build our application in here doing a Maven JAR, sorry, a Maven package or any kind of building that you're going to do.

And here you probably wanna build a Docker image. Don't worry, we're going to learn how to do this. Then you probably wanna test to do a lot of testing here. And finally, probably you wanna deploy your tested and successful application to production. And as you can see, you can actually save or publish your test unit results, as you already know, using the JUnit plugin. So this is it. Probably you are super familiar with all of these steps because we have done a lot of this.

When we worked on the Java application in the Maven section, we actually did all of this. So probably you are already familiar with this kind of workflow. So we're gonna learn how to create this entire pipeline here. We're going to learn how to create these stages, how to check, how to code, how to fill a Docker image, test it, deploy it and do more things using the core Jenkins pipeline. So let's go ahead and move on to the next lesson.

# Create your first Pipeline

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video we're going to be creating our first Jenkins pipeline. So let's go to our Jenkins data folder, and here I will leave you this pipeline folder that you can see here. So let's head to that folder. And in here you're going to find a lot of files that are created for you to simply learn. And let's take a look at the first one, which is first-pipeline. So let's take a look at cat first-pipeline.

And probably you already saw this before, and that is because this is the example from the Jenkins page. So this is how a pipeline looks like. You always need to start saying, pipeline, because this way you instruct Jenkins that this is a pipeline. And instead of the correlations, is all of the configuration. So here we have a line which is always mandatory, agent, and you will have this, agent any, always in here or probably most of times.

And an agent is nothing else but how this pipeline is going to be executed. For example, you could say here, docker or another source, just keep it simple. agent any, which means that any available agent is going to build this pipeline. So don't worry about this. Let's move to the important part, which is, stages. So in the stages you define (indiscernible) section as you can see here. And instead of this, you have your stages.

So you can have as much stages as you want. So let's take a look at this one, stage('Build'). Okay, so in here probably we want to build something. So here you have a steps section and you can start building things in here. Normally this accept Bash, so you can do like, Bash commands in here. For now, we're only going to be printing the word, Building. Same thing here, stage('Test') Here you have your steps and we're only going to be doing something like echo Test because this is a super simple example.

And same thing in here, stage('Deploy'). And we're just going to do an echo Deploying. But the thing that I want you to know is that in this step section is where you are going to do all of the magic. You are going to be executing script, executing shell commands, executing deployment commands, everything that you need to do, you are going to do that from this. So let's go ahead and copy this. Let's go and copy this and we're going to go to Jenkins and let's go ahead and create a new item.

So let's enter an item name, and we're going to say, pipeline, for example. And this is going to be a Pipeline project. So let's click on OK. And in here, if you scroll down, you are going to see something similar to the DSL configuration. So we have two option in here to put a pipeline script in here, or to download a script from SCM. So for now, let's go ahead and paste our coding here, in this shell.

Don't worry, we're going to be using a script from our GIT server later. But for now, just for learning, let's paste this in here and let's see how it looks like. Remember pipeline agent and you have your stages in here and this is it, super simple. So let's save this for now, and we're gonna build this project and see how it looks like. And as you can see the process is already starting, and well, it was super fast because it didn't have too much to do.

So here you have your Build stage, which is defined in this file, and you say stage, stage('Build') and this is your Build stage, and you have that it was success. And you can even take a look at the locks. And as you can see this is only printing what we printed in the script. Same thing for testing and deploying, stage('Test'), this is the test, state Deploy, This is at Deploy. And you can always go to the Console Output.

Let's go here. Let's click on Console Output. You can see all of the things that happened when you were executing your pipeline. So in our real stage we only had something like an echo here. Same thing for testing, and same thing for deploying. But as you can see, we have all of the logs in here so we can have a track of what actually happened. So this is super simple. You already created your first pipeline using Jenkins file user Jenkins as code, and you already have here, your VAXs looking super nice.

So this is it for this video. I'll see you in the next lesson.

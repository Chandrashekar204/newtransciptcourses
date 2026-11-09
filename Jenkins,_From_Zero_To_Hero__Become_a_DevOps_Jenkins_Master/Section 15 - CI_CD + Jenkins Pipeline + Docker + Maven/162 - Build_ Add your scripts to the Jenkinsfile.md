# Build: Add your scripts to the Jenkinsfile

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to use our two scripts to generate a full new Docker image using our code. So remember, how do we create a jar using Docker? Well, we already created a script for that and that is like Maven.sh. Something like that. Let me look for -D. Yes. Remember this line? Doing this, we actually create a jar file. So if we execute this, our jar is going to be built and it's going to be put at the level of target.

And then in order to create a Docker image using this jar, we do Jenkins build and build.sh. And doing this, we are building a docker image using the jar that we previously generated. Because remember that if we take a look at our Docker file, we are actually copying the jar that was generated previously to that specific image. So that's super cool. Now, how do we include this in Jenkins? Well, remember that first we always need to generate a jar.

Whenever your developer push to your repository, the first thing that you want to do that you want to build the jar to make sure that everything is working good. So let's go to our Jenkins file. And the first instruction in our build stage is going to be yes, building the jars. So for this, we're just going to execute our simplest script. That is going to build our jar using docker. Cool. And the second instruction is going to be building a docker image using this jar.

So, okay, let's save it. And remember that to build the image we just need to run this script that we created and this is going to build the image. So let's go to our Jenkins file and let's paste that in here. So this is cool. Now we have in our Jenkins file, our process completed. In here we are creating a jar and here we're building a docker image using this jar only in two lines. So this is it for this video.

I'll see you in the next lesson.

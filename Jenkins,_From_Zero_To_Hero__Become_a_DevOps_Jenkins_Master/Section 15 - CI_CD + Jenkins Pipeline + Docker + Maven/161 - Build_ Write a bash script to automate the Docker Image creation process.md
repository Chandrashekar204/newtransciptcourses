# Build: Write a bash script to automate the Docker Image creation process

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello, and welcome back. In this video, we're going to learn how to automate everything that we have done so far. Remember that we have done a lot of manual things and probably that's going to be a little bit complicated, and we don't like complicated, so we're going to make it easy, and we're going to create a script that is going to do everything for us. So, remember, what do we need to do?

So let's go back to the pipeline folder. You know, jenkins data/pipeline. And in here you have your Jenkins folder, your Docker file, and Jenkins file. Let's go to this level and remember that this Jenkins file is going to be executed, so you must keep in mind that everything that you do should be from this relative path. So the first thing that we need to do is always to copy the jar that is being generated from here.

You know, you can say something like this to jenkins/build. Remember that this should always be done because you need to copy your new jar to this specific location. Because remember that in the Docker file that is exactly in this folder we are saying that we want to copy the jar file. So doing a copy of your new jar is super important so you can actually build your image with the jar that was previously generated.

So this is a super important line always copying the new jar to your build folder. And once you do that, probably you want to do something like in one line you can do cd jenkins/build because remember that this is the folder where we have our Docker compose file in our Docker file. And once you are in here, you can do that automatically doing something like ampersand docker compose and then you can say dash f, And remember that your docker compose file- let me show you the content of that folder so you can see it.

So you can say cd to this folder and then you can do docker compose dash f, this guy, and then you can do build. And if you don't want to use cache, so you can go like dash no cache and docker is not going to be using cache. So you can make sure that your image is not cached. Okay. so doing this, we're actually doing automatically the same thing that we were doing before. So if you hit enter, then your image is going to be created using this docker compose file.

And as you can see, we actually changed directory automatically because of this instruction. So that's super cool. Now, let's create a script to automate this entire process, right? So let's go to our build section and let's create a new script. So let's call our script like build.sh. And we're going to say, okay, bin/bash. And what is the first thing that you need to do? Do you remember? Well, the first thing that we need to do is, of course, copy the jar, the new jar to the build location.

And remember that this script is going to be executed from this folder from the level of the Jenkins file. So to copy that would be cp dash f to force it, java app/target* everything that ends in jar, and we're going to copy that to jenkins/build, and that way, we are copying the jar to this folder. Take a look at this. If we ls the jenkins/build directory, you're going to find your jar there. It will remove that jar from these jenkins/build/* .jar.

And then you do an ls, the jar is no longer there. But if you do the copy instruction and you do an ls, you are going to find your new jar in that specific folder. So we need to copy this line and this line needs to be executed by our script. So from here, let's open our file in jenkins/build/build.sh, and we're going to execute our first line for this script. So this is like this. The second line would be building the docker images.

So let's do something like this. I really like doing these kind of things like echo building, docker images, you could say, just to know what is happening, Building Docker Image. And then you can do like this and then you can do things like this. Okay, let's close this. Let's put more asterisks out here, and let's close it. Okay, cool. So now we need to build the image, and remember that we already know how to do that using our docker compose file.

First, we need to do an ls to our build folder. And in here we're going to do the cd line. Remember, cd jenkins/build. We need to execute this. We're going to cd to this specific folder. And from here, we do the docker compose dash f calling the docker compose file build that we created. And then we say build. So let's copy this line. Remember that if we execute this, a new image is going to be created, so that's super cool.

Let's go back to the level of our Jenkins file and let's modify the build script. And as you can see, we're going to paste that in here. So in this way, we're doing everything that we need to build our application. So in this case, we're copying the new jar and we're building a new image using this specific jar. So let's go ahead and test it. We're going to give it executable permissions, change mode plus x.

And now the only one thing that we need to do to execute all of these things that we have manually done is just calling the script. We just need to call it. And as you can see, this is going to be automatically done, which is super cool. So now you have reduced all of your effort to a simpler script, and now you can just simply run this script, and then your entire process of building your docker image is going to be executed.

So this is it for this video. I'll see you in the next lesson.

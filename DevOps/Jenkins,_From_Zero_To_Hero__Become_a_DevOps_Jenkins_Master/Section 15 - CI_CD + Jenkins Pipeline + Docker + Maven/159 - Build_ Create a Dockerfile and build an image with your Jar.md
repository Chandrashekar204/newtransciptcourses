# Build: Create a Dockerfile and build an image with your Jar

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to learn how to create a docker image using the jar that we are generating using Maven. So the first thing that we want to do is that we want to use a docker image that has Java installed. So let's look for docker openjdk, and let's look for it because probably we want to start from this Java. This image actually contains Java. We're going to run a Java application, right?

So we need Java. For this exercise we're going to be using the 8-jre-apline We're going to be using this image. So, okay, now that we know which image from all of these we're going to use. let's go to our terminal, let's go to our Jenkins directory. Let's go to build, because remember that here we're saving everything that is related to the build stage. And here we're gonna create a new docker file.

Let's call it like Dockerfile-Java. And in here we're going to start from openjdk and we're going to use the tag. We're gonna use this tag, okay, it looks like I can't copy so I'm just gonna manually type it. 8-jre-alpine. So we're going to start from this image because it contains Java and it's Alpine. It's super, it's a super tiny image. Cool. So now we want to run a command. We want to make a directory in a slash app because here we're going to place our jar.

Once we create a directory, we want to copy the jar file that is being created from our host. So we're going to copy everything that is .jar to /app/app-jar. So in this way we can control the name inside of the container. Cool. And finally we need to specify what this container is going to run. In this case, we want to run this jar that we're copying. So we want to say Java-jar and we want to run this jar that we have just copied.

In here we have a super important part and that is that we're going to try to copy a file that is in this current directory, which ends in .jar. But if we save this docker file and we do an ls we're not going to find any file with this name. So what do we need to do? Well, what we need to do is simply go back and copy the jar that was created in the Java app folder, target directory, my jar and we're gonna copy to that directory.

And as you can see, now we have a jar file. So if we do an ls, then that's gonna be cool. So let's do an ls in here. Let's take a look at our docker file. And you see, okay, we create a directory then we copy this jar to this location and finally we just execute that jar using Java. Super simple. Now how do we test it? Well, let's build this image, and let's see if this jar gets copied to this location.

To build a docker image, it's super simple. You do docker build, and then you say, okay, I want to use this docker file and I want to tag my image as test, for example. And we're going to put this dot which means that it's going to use all of the content that is in this directory. So let's hit enter. And if you don't have this image locally, then docker is going to start downloading it for you. So this may take a while depending on your internet connection.

So let's wait until this finishes. Okay, the process already finished. As you can see, the image was downloaded and the other steps were executed successfully. So, cool. Now if we do docker images and we look for the test image that we created we're gonna find that image in here. Cool. So now let's see if this jar that is in this folder is inside of this image. So let's go and run a container, a temporary container.

We want an interactive shell, so we pass ti, then we pass the name of the image that we created, which is test, and then we pass sh which is the terminal that Alpine has built in. So let's hit enter. And now we're inside of this container which is based on this image. So if we go to /app/, you're gonna find the file there. So this is super cool. As you can see, our process is working because our jar is actually inside of these folders.

So we, if we exit out of here, this jar is actually this jar, but with a different name because remember that in the docker file, we're copying the jar that we have in this location, right here. We're copying this two /app/app.jar which is exactly this content. So this is super cool. You already know how to create a docker image, how to copy the jar that you are generating to that image and how to get a final image.

And at the end, you're gonna end up with a super simple image like this, which is going to have your Java application in here. Remember that this CMD means what a container is gonna do. So if we now create a container doing a docker run -d and then we say test, because remember, that test is the name of the image that we created. This line is going to be executed, so this should say hello word. So let's hit enter.

And now we're going to do a docker logs for this id. And as you can see, we have hello word. And hello word is nothing else but the code or the functionality of this, your file. So this is super cool. You already have your application dockerized. This is it for this video. I'll see you in the next lesson.

# Push: Write a bash script to automate the push process

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're gonna automate the process of pushing images to our registry. So let's go to our jenkins-data folder pipeline and in here we're gonna create a new directory under jenkins that is gonna be called push. Okay, now we need to do a super small change. We're gonna go to that jenkins directory, the build section, and remember that in the docker-compose-build, we are generating our image using app.

But if you remember, our repository is named as maven-project, so we need to give the image this name. So we're gonna modify this and we're gonna say that the resulting image is going to be maven-project just to make it simple, right. So, cool. Now that we have done this, we need to go to the folder that we have just created, which is push. Well, I think I made a mistake so let's move this to push.

And that's okay. So let's go to that directory, and in there we're gonna create a simple bash script. So let's say vi push.sh, for example. And remember that normally bash scripts start with bin and bash, and we're gonna do the thing that we always do which is *, and then we say echo, we say pushing image, okay, and finally, another echo. And once that we've done this, now it's time to create a simple variable.

So let's create a new variable. Let's call it image. And we're gonna say that this image is going to be the maven-project, right? So we're just gonna copy that, paste that in here. Cool. So the first thing that we need to do, remember that in order to push to our registry, is the login. So we're gonna login. We're gonna say echo logging in or something like that, and we're gonna give more asterisks just to inform what we are doing.

And in this specific moment, we're going to do docker login and we can pass some parameters to avoid interactive input. So if we pass docker login -U and we pass our user, which is this one. Okay and then we want to pass the password. So for that we pass -p, and we're going to specify an environment variable that is going to be called PASS, and we're going to populate this later because this is sensitive information so probably we don't want to store the pass right here.

But keep in mind that this will contain the password to get authenticated. The next thing that we need to do is that we need to tag the image as we saw before. So we're gonna do tagging image. Tagging image, and right here, we're gonna do docker tag. Remember that the resulting image will have this name. So we can say IMAGE, and remember that we're going to be using a BUILD tag, and that resulting image would have the name and column build tag.

Remember, that information is already set in the build section. In the docker compose build, you find the maven-project which is the name of the image and the build tag for that image. Remember that this variable comes from jenkins. So we're gonna tag the resulting image that is gonna be the image which is this one in the build tag, and we're gonna tag it to the format that Docker Hub is expecting.

So in this way, it should be like this. So we're gonna copy this and we're gonna paste that in here. Cool. We're gonna change this because remember that we can say this is the IMAGE and the tag name is gonna be the BUILD tag. So that's cool. As you can see, the only one thing that we're doing is that we're putting this before the image so Docker knows where to push it, right. But we are still missing one step, which is the final one, and that is pushing the image to the Docker Hub.

So we say echo, then we say pushing image, and we're gonna just push the image that we created. So docker push, and this newly tagged image right here. Now it's time to test it. So let's save this file and let's test that it works. So we're gonna give it executable permissions. Cool and now we can execute this script from here because we're not copying anything so it doesn't matter. Now, we're just gonna try to execute it and probably we're going to have errors.

So let's execute it. Yes and as you can see, this is complaining because of two things. The first one is because the argument, the passed variable that we're defining here, is not defined. I'm just gonna define this right here for you to see how it works. But remember that we're going to define this later. So we're gonna say export PASS equals to the password that I created for the registry, and then we're going to export this BUILD_TAG.

We're gonna give it a new tag. So export BUILD_TAG. It's gonna be like this random number, right. So once we do this, then we have all of the variables that we need. So we have the path and we have the build tag, and this should work. So let's execute this script once again. And as you can see, this is logging in correctly. Then you see the login success and then you see an error in here that there is no image maven-project, and that's right because we don't have any image like this.

So let's just create a new image there to test it. So we're gonna say docker tag app:2 which is the image that we have and we're going to put this name to this one. Okay, enter and let's try again. And as you can see, that's actually working now. We were successfully logged in tagging the image with success this time and now we're pushing the image to the repository. Now, if we go to the repository and we refresh, you are going to see our new image that we pushed from the script.

So this means that our script is actually working good and now we can use it to push images to our Docker Hub. So you already know how to automate the process to push images to your Docker Hub repository. So this is it for this video. I'll see you in the next lesson.

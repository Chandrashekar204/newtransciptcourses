# Build: Create a Docker Compose file to automate the Image build process

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to learn how to create a Docker Compose file to automatically view our image. Remember, that in the previous video we were using the Docker build command to build this image, but now we're gonna take it to the next level and we're going to create a Docker Compose file to build this image in a easier way. So let's go ahead and create a Docker Compose build dot YAML file at the same level of your Docker file Java and your MVN dot SH.

Remember that right now, we are inside of the pipeline Jenkins and build directory. So let's create this new filing here which is going to be Docker Compose build. And if you are a little bit familiar with Docker Compose, you will know that we're going to start with version, this is going to be version three, and in here we're going to have the services. And this section is going to contain an app service.

Remember that you can name it as you want. We're just gonna keep it simple for now. And this service is going to have an image and the image is the image that we're going to be creating. So we're gonna call this image "app". And remember that this process, I mean the building process, is going to be executed via Jenkins. So probably you will want to have something like a version of your images. So for that, we can do like build tag because remember that this build tag is an environment variable that is available in Jenkins.

And this means the number of the build. So if we do this, whenever we generate a new image we're going to tag that image with a different number. So for example, app version one, app version two, app version three. And in that way, you are going to have your image version which is going to be cool in the future if you want to roll back or something. So okay. For now, we don't have this environment variable.

We're gonna set it later for testing purposes. But remember that this is a global environment variable in Jenkins. So in Jenkins, this is going to be auto populated. Okay, cool. Now we need to tell Docker where is the Docker file that we're going to use to build this op image. So to do that, we're going to use the build property. And under it, we're gonna say that the Docker file that is going to be used is the Docker file Java that we created.

And remember that Docker file is right here. You can even do something like the context. Context means the folder where the Docker file is located. In this case, it's located in this folder. So we're telling Docker, okay Docker, please build this image going to this context, which is the current directory, and looking for a file which is called Docker file dot Java. So let's save this and let's try to build this new image using Docker Compose.

So for that, we do Docker Compose. We say dash F because the name is different. So we pass the name and we say build as you may already know. And as you can see, it says the build tag variable is not set. So this actually fails. So let's set this to any value like export this to one for example. And now if we build this, then it gets automatically built. And as you can see, we now have an image which is called app colon one.

So let's do Docker images and let's grep for app. Grep dash W for app. And as you can see now, we have the version one in here, but what happens if we change the build tag to two, for example? And now if we build it again, remember that our Docker Compose file is taking this value, and if we do a Docker images, you're going to find that now you have another image which is the version two. And remember that always when you build your image your jar is being copied to that specific location.

For now we're copying the same jar. That's why the image is the same. But in the future, this jar is going to be dynamic. In the next lesson, we're going to see how to do this but for now, you know how to create a Docker Compose file, how to define your build process, and how to automatically do it just doing a Docker Compose build. If you hit enter, then you're going to be building new images always.

So this is it for this video. I'll see you in the next lesson.

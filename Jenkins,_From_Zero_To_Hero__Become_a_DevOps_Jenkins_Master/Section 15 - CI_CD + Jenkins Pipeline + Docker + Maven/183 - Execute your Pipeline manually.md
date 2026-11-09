# Execute your Pipeline manually

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to execute our pipeline manually and we're going to see if we have any errors are still pending. So, let's click on build now finally, because we've done a lot of things for this pipeline. Let's click on build. And I think that is going to fail. So, let's take a look at the console output. And here we have a permission denied. Do you remember this error?

Yes. So, to fix it, we need to go to our terminal and do outside of the containers, we need to do "sudo chown 1000 -R", or well "/var/run/docker.sock". And this should fix the issue. So, let's put the password and let's try to execute this again. Okay, let's take a look at the logs. Let's go inside of this execution, console output. And cool. As you can see now, our project is being executed. We're building the jar.

It looks good. Now we're doing, we're building the Docker image. The output looks super cool. As you can see, this is the tag that it's automatically being taken. Remember the build tag variable which is the number of this execution. And here, we are testing the code. Everything looks good. Nothing bad happened. That's super cool. And here, we are pushing the image to the repository as you can see, yes, it's says login succeeded, tagging the image, pushing the image to the Docker hub that we created.

That was successfully pushed. And now finally we're doing the deployment. So, it looks like everything is going as expected. Let's wait until this finishes and see if that works. Great. As you can see, the deployment process was successful. You can see that this is the log for the execution in the remote machine. Looks like the image was not present in the remote machine so Docker downloaded the image in here, as you can see.

So, that looks pretty cool. As you can see, it was successful. So, let's click on this. We have the last successful artifact archiving here and our pipeline entirely worked. So, let's log in into our remote machine and let's see if everything went good. Let's do a "docker ps -la". And that's super nice. As you can see, the container was recreated one minute ago. The image that we're using is exactly the image that was pushed with the execution number three of our pipeline, as you can see number three.

This is the build tag environment variable that Jenkins automatically assigns to our scripts. And as you can see, it was about one minute ago, you know, that this container exits because it only says "Hello World!" and then it actually dies. So, it's gonna be "docker logs maven" and we have our "Hello World!" But as you can see, the entire process worked as expected. Let's take a quick recapping here.

Let's go to the logs. And remember, we're cloning the repository with the new changes. We're building a jar with that new code. Then we're building a Docker image using that specific jar. And then we're testing the code using a Docker container. And then we are actually pushing the image to the Docker registry that we created. And finally, we're deploying that new image that passed all of the tests and that is ready to be deployed using this script.

And whenever we deploy, we're transferring the file with environment variables. We're reading that file in that remote machine, downloading the image, the correct image, getting authenticated using Docker login, and finally deploying the application as you can see, or recreating the Maven app. So, this is super great. It's actually working good. So, this is it for this video. I'll see you in the next lesson.

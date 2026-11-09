# Add the private ssh key to the Jenkins container

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to put the key file that is needed to deploy the application in the Jenkins container. Remember that here in our Jenkins Deploy, deploy.sh, we're actually using a key, which is OPT prod, to transfer files and to deploy the application in our remote machine. And also remember that this script is going to be executed from the Jenkins container.

So if we go to our Jenkins container and you try to look for this path, then you're not going to find it. So you're going to have errors. So what we can do is that we can simply do a Docker CP of the key that we just created to the container where we want it. So Jenkins OPT prod. So that's it. Now you exec inside of your container, go to OPT and you're going to find your file there. So please make sure that you copy your key file to your location, because otherwise you're going to have errors.

Now that we have the key, let's try to do the connection. So let's say ssh-i prod prod user at Linuxfacilito.online, and we hit enter. This step is super important, because you need to verify the authenticity for these hosts. So say yes, because if you don't say yes, then probably you're going to have errors in your pipeline. So this is it for this video. As you can see, the connection was successful.

We have done everything we needed. So I'll see you in the next lesson.

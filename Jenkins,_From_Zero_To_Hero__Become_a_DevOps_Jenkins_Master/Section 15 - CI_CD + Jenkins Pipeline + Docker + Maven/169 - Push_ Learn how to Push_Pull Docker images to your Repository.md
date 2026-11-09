# Push: Learn how to Push/Pull Docker images to your Repository

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to learn how to push images to this Docker repository that we have just created. So let's go to our terminal, and in here we're gonna type Docker login and we're going to hit enter. And here we're gonna pass the username that we created. In this case, this is my username, so let's go ahead and copy that. Let's paste it. And now let's provide a password that you created.

And as you can see, it says login succeeded. So now we can start pushing or pulling images from our repository. So the first thing that we're going to do is that we're going to push a new image to our repository. So we're gonna copy this command because we are already locked in. We're gonna copy that and our image needs to have this name to be pushed. So let's take a look at Docker images, and let's look for an image right here.

Let's push this app image. So we're gonna do Docker tag and we're gonna change the name of app tag 2, we're gonna tag it to these versions. So we're gonna say Maven Project, and we're gonna pass the tag as two. And now if you do Docker images you can see your image in here. If you see it's exactly the same image, but with a different name. So now that we have tagged our image, it's time to push it.

So let's go ahead and do Docker push the name of the image and the tag that we just set, so number two. And if we hit enter, as you can see, it's preparing the push and it actually starts pushing your image to this repository. So once you have pushed completely this image to your repository you're gonna be able to see that image right here. So let's wait until this finishes. And as you can see, it actually finishes too fast.

So now let's head to our repository, let's refresh and as you can see, now we have the image that contains the tag number two. So you have already pushed your image with this Maven Project name and the tag that you've specified. So now let's take a look on how to pull image from this repository. It's gonna be exactly the same thing. We're going to copy the name of the repository that's gonna be like this, and we can do Docker pull from here.

We want to pull the tag number two, which is this tag that we have just pushed. So whenever we do this and we hit enter, as you can see, the image has been downloaded from here, from that repository that we created. So you already know how to push images and how to pull images from the Docker Hub. So this is it for this video, I'll see you in the next lesson.

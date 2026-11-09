# Download the Jenkins Docker Image

*Section: Introduction & Installation*

Instructor: Hello and welcome back. In this lesson, we're gonna learn how to install Jenkins and we're going to install Jenkins using Docker. That's why we installed Docker before. Okay, so as you may know, or if you don't know, don't worry, but Docker uses something called an image. An image is like an snapshot of a configuration. So in this case, we're going to look for a Jenkins image, which has already all the configuration and we just need to run that image, and then we will have our Jenkins server up and running in some minutes.

So let's head to google.com and let's look for Docker Jenkins image. We hit Enter and then we're going to go to their first result. And as you can see here, we have this Jenkins image, which is the official image for Docker. So we're going to copy this command and this command is going to download the image. So we go here and what we're going to do is that we're going to paste this command and we hit Enter.

Okay, as you can see, the image is already downloading. We only need to wait until the process completes and we are almost done. This is the magic of Docker. Docker allows you to create services quite easy with images. So you only need to have one image and then you are going to be able to spin up one service pretty fast and that's cool. You just need to create an image or look for an existing image, run that image, and then you have your service up and running.

Don't worry if you don't know Docker, we are going to learn here. So, okay, you already downloaded this image but where is this image located? Well, if you type Docker images, then you are going to see your image here, which is pretty good. It's a little bit heavy, but don't worry. Okay, so we have. If you must know, if you type Docker info and you grep for root, you are going to know where Docker is saving the files.

So this is the location. If you do something like sudo du -sh and then you give the path, you are going to know how much space is Docker taking. So in this case, Docker is taking this size because we downloaded this image. Okay, cool. So we already downloaded the Jenkins image. Now, it's time to run it. So for that, see you in the next lesson.

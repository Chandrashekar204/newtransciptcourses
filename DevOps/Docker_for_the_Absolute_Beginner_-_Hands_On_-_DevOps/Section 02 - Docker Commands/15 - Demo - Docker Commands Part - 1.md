# Demo - Docker Commands Part - 1

*Section: Docker Commands*

1 Okay, so the next thing that we're going to do is run a Docker container, run our first container. 2 So if you go to hub.docker.com, you'll find images that you can run. 3 So this is Docker Hub, this is Docker's central repository of all containers or all images that can 4 be used to run containers. 5 And if you see here, there are all sorts of images available. For example, for machine learning and 6 AI, you have TensorFlow, PyTorch, 7 you have an image for Python. So there are images available for almost anything that you can think 8 of for any versions of those softwares or applications.

9 There are web servers, there's operating system based images like Alpine, there are databases like 10 Postgres, MySQL, MongoDB, 11 and there's images for Grafana. So almost anything that you can think of would probably have Docker image here. 12 So we're going to start simple. So we'll go to operating systems, and we'll select one of these operating systems. 13 So there's Ubuntu, Debian. So I'm going to go with Alpine. So Alpine is a minimal Docker image based on Alpine Linux.

14 So Alpine Linux is a minimal operating system. And as you can see, its size is 3.6 MB. So that's a 15 super lightweight image. 16 And all we need to do is copy this name from here. And we're going to run an instance of this image. 17 So back in my terminal, I'm going to run a docker run command and paste the name of the image, which is Alpine. 18 So the first time that I'm running this, it's going to download the layers of the image. And because 19 it's so small, it's less than 5 MB, 20 it's downloaded that in a matter of seconds. So I now have the image locally, and it's already run it.

21 Now because this is an operating systems image, it's a base image, it doesn't have any application 22 running on it currently. 23 So it just exits immediately, which is why I'm not able to see that I'm back on my terminal. 24 So I could run commands inside this container. So I could run the docker run command again. 25 And I can run a command such as cat slash etc slash star release star. So it's going to print.

26 So there is nothing much I could do with it. What I could do is maybe run an application or a 27 program that's inside the image already. 28 So I'll probably run a sleep command and sleep for say 10 seconds. 29 And what's going to happen is, it's going to create a container from the image, and then it's going 30 to invoke the sleep command, 31 and it's going to sleep for 10 seconds. And for that 10 seconds, I'm going to be on the terminal, 32 and now it's done and I'm back.

33 Now another thing that we could do is maybe we can explore another application, maybe like a web server. 34 So if I go back to the hub, and if I go to web servers, I have a bunch of different web servers here. 35 I'm just going to pick Nginx for now. And you can see that there are all sorts of different versions 36 of Nginx available here. 37 There's Sling versions and Alpine versions. And for now, I'm just going to look more into tags and 38 versions later in the course.

39 For now, I'm just going to copy the name from here, I'm going to run an instance of the Nginx container. 40 And again, what it's going to do now is it's going to pull the images needed to run an instance locally. 41 So it's going to do that. And this is a slightly heavier image. So it's about 34 MB, so it's going 42 to download that. 43 And it's downloaded that and it's immediately run the Nginx web server.

44 So the Nginx web server is now running on this host. 45 Now, how do you access it? And what port to access? All of that we'll discuss in the upcoming videos. 46 For now, we're just going to focus on running an instance of a container.

# Demo - Creating a new Docker Image

*Section: Docker Images*

1 In this demo, we're going to see how to build our own custom Docker image. 2 So here I have my simple web application application. 3 So a simple six-step process. 4 And what we're going to do is 5 it's important that we first clearly understand 6 how a manual process of running the application 7 and we have these steps written down like this in manual format 8 because then it becomes very easy for you to create a Docker file out of this.

9 If you do not know the steps involved in running the application 10 and if you have not tested and made sure that it's working as expected 11 then you're going to have a hard time building the image. 12 So what I'm going to do is 13 I'm going to, before I build the image, I'm going to run it 14 run these steps manually to make sure that they're working. 15 So that's the best practice I would recommend.

16 So for that, I'm going to start with a Docker image based on Ubuntu. 17 So a Docker container based on Ubuntu. 18 I'm going to run a docker run-it ubuntu. 19 And what it's going to do is it's going to pull the latest image of Ubuntu 20 and kind of connect me to its terminal. 21 So now I'm inside the Ubuntu operating system or Ubuntu container. 22 Now I'm just going to go through each of these steps 23 and run it and make sure that it's working as expected.

24 So the first thing is to update the package index. 25 So that works fine. 26 And next I'm going to run an apt-get install python3 flask. 27 So this is basically installing the python3 flask application. 28 I'm just going to select the time zone. 29 So I've just set the time zone and it's installed the python flask application. 30 And then I have the part where we need to locate the source code.

31 Because this is a container, it doesn't have my source code. 32 I'm just going to, for now, create a file and copy the source code over manually. 33 When we create the image, I'll show you how to copy it over. 34 So we have an instruction for that. 35 So I've just copied the source code over 36 by creating a file and pasting the source code manually. 37 And then the next step is to set the flask app environment variable.

38 So I'm just going to set the environment variable like this. 39 And I just want to make sure... 40 So the app source code is created here, but I specified opt. 41 So I'm just going to move that over. 42 I'm just going to move that to opt, okay. 43 And now the last step is to run the application. 44 So I'm just going to do a fast run. 45 All right, so there it is. 46 It's running and that means that the steps are good and validated.

47 All right, so I'm just going to exit out of that container right now. 48 And I'm back on my local host. 49 All right, so the next step is to build the dockerfile. 50 So I'm just going to go here and create a new file, name it dockerfile. 51 And I'm going to look at the instructions side by side 52 and see how we can convert that to dockerfile instructions. 53 So the first step is to start with Ubuntu.

54 So I'm just going to do it from Ubuntu. 55 So I have the base image set as Ubuntu. 56 The next step is to run a command. 57 So I'm just going to run and fan paste this. 58 The next step is to run another command to install Python flask. 59 So I'm just going to do that. 60 The next step is to copy the source code over. 61 So right now we are in the same folder. 62 So my app source code is in the same folder.

63 So what I'm going to do is I'm just going to do a copy. 64 I'm going to say app.py. 65 And then the target location is slash opt slash app.py. 66 So that's the location inside the image. All right. 67 Next step is to set the environment variable. 68 So I'm just going to do env. 69 So instead of export, I can just do env and set the environment variable like this. 70 And the last step is to start the application.

71 So I'm going to set an entry point. 72 So entry point is what sets the... 73 defines what command would be run when the application starts. 74 So I'm just going to copy and paste that here. 75 And there are some best practices that I'm not following right now 76 because I'm just trying to keep this super simple. 77 But as we progress with the course, we'll learn some of the other best practices. All right.

78 So I have all my instructions here and I have set the environment variable 79 and I've set the entry point. All right. 80 Now I'm going to build the docker image. 81 So I'm going to run the docker build command. 82 I'm going to specify a name for the image. 83 I'm just going to call it web app. 84 And then I need to provide the location of the directory that has the source code. 85 In this case, I'm just going to do the current directory, which is a dot. Right.

86 So as you can see, it's now building the docker image. 87 So it's transferred the files, copied the... 88 it's currently pulled the docker... the Ubuntu image. 89 And then now it's run the steps of installing the apt update and the Python 3 flask. 90 And then it's copied the apt.py over and it's ready now. 91 So there are some warnings, which is... 92 that's because I haven't followed some best practices, 93 which we'll cover when we talk about the command and entry point.

94 So this is... this is supposed to be in a JSON format. 95 But I'm just going to skip that for now. 96 So I have the docker image built. 97 I'm going to run it. 98 So to run it, I'm going to do a docker run. 99 And actually, before that, if I do a docker images, 100 I'm going to be able to see the images that are there. 101 So this is the Ubuntu image, which is 120 MB, 102 which is the base image.

103 And then I have the web app image, which is 247 MB. 104 So this is pretty, pretty heavy for a simple web app like this. 105 But we'll see ways to optimize this. 106 In the future, this should probably be less than 20 MB. 107 All right, so I'm going to do... 108 to run the app, I'm going to do a docker run web app. 109 And if I go, I see that it's running the application. 110 And I can... I can see it here.

111 No, I cannot access it right now because I have not mapped a port to the host. 112 So if I go to this link, it's just going to say fail to load. 113 All right, so what I need to do for that is I need to provide a port mapping here. 114 So 5000 on the container is going to be mapped to 5000 on my host. 115 I'm going to run that again and refresh the page. 116 And I can see that it's working. 117 And it's... the welcome message is visible.

118 I'm going to do, how are you here? 119 And it's going to come back with a second route, which is... which is this. 120 All right, so that's basically it. 121 That's how you build a custom image.

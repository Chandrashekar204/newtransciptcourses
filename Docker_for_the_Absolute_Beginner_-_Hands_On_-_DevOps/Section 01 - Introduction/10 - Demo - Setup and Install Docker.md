# Demo - Setup and Install Docker

*Section: Introduction*

1 Okay, we're now going to see how to install Docker on a Linux VM. 2 So here I have my Ubuntu VM, I'm logged into it. 3 And on the right, I have a browser open. 4 So I'm going to go into docs.docker.com. 5 And I'm going to go into manuals. 6 And here on the left, I have a few sections. 7 So there's Docker Desktop, which we'll look at later. 8 First I'm going to go to Docker Engine. 9 And we'll see how to install Docker Engine on my Ubuntu VM.

10 So I'm going to keep it super simple in this first demo. 11 Later on, we're going to see what Docker Desktop is. 12 So Docker Desktop is basically a set of tools that are around Docker Engine. 13 But in this first demo, I want to keep things super simple. 14 So you understand Docker without any anything else, right? 15 So we're just going to install Docker Engine. 16 That's the first step. 17 So my system is Ubuntu.

18 So I'm going to select Ubuntu. 19 And here I have my instructions on the right. 20 So let's read through this. 21 So at first, it says to get started with Docker Engine on Ubuntu, make sure you meet the prerequisites. 22 And there are a couple of prerequisites around firewall limitations. 23 So Docker is only compatible with IP tables, NFT and IP tables legacy. 24 So rules created with NFT are not supported.

25 So you can just read through those. 26 Then the first requirement is that you need to be on a 64 bit version of one of these 27 Ubuntu systems, right? 28 So these are the different versions available. 29 Let's see where we are. 30 So if I go to my Ubuntu VM and run the cat command slash etc slash star release star is 31 going to display the details of my VM. 32 So I can see that it's an Ubuntu distribution and it's 24.04 noble version, right?

33 And if I go here in the documentation page, I can see that this is a supported version. 34 So that's great. 35 Next, I want to see what architecture I'm on. 36 So I should be on a 64 bit version of the OS. 37 For this, I'm going to run the D package command and the option print architecture. 38 And I can see that I'm on an arm 64 version and I can see that that's supported. 39 Alright, so the prerequisites are good.

40 The next step is to uninstall any old versions. 41 So there are a bunch of packages that are going to get installed when you install Docker 42 and want to make sure that your system does not already have one of these. 43 Now remember, you want to be careful if you're running on an existing VM that is probably 44 already in production with some other things already installed. 45 So you might want to be careful in that situation because this is a new VM, I'm just going to 46 run this command and I can see that there are no packages that are installed already.

47 The next step is to install using the apt repository. 48 So the first thing is to set up the Dockers app repositories, I'm going to copy this command, 49 as you can see, it's going to do an apt update first and then install the certificates and 50 then download the latest version of the Docker package and then make that executable and install it. 51 So I'm just going to copy that and run that those set of commands.

52 Okay, when it's asking me for confirmation, I'm going to say yes. 53 Okay, so that's done. 54 And as the next step, we're going to install the latest version by running the apt install command. 55 Now, as you can see, it installs a bunch of things. 56 So there's the Docker CE, which is a community edition, there's the CE CLI, then there's 57 the container D, we're going to discuss some of these later about Docker compose and build 58 x plugins later in this course.

59 So for now, I'm just going to proceed with the installation. 60 Okay, so that's completed. 61 The next step is to verify that it's running. 62 So I'm going to copy this command, I'm going to run the system cuddle status Docker command, 63 and it tells me that the status is now active and running. Perfect. 64 Okay, I don't need to run this the next command. 65 So I'm just going to verify the installation is successful.

66 By running the Hello World image, I'm going to copy this, run that. 67 So in this case, what it's doing is it's pulling the Hello World Docker image from Docker Hub. 68 And it's going to run that an instance of that locally. 69 So here it is, it's downloaded the newer image, and there's a message Hello from Docker. 70 That means it's successfully installed.

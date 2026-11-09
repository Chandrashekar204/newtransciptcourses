# Getting Jenkins Running

*Section: Setup*

1 Now that you've got Docker installed, 2 now it's time to get Jenkins up and running. 3 Let's quickly break down what we're doing here. 4 And to give you a bit of context, 5 if you're not familiar with Docker, 6 Docker is like a VM, 7 except it doesn't install the complete operating system. 8 Instead, it's going to use the host's underlying kernel. 9 So it means it's incredibly lightweight 10 and the images are only a couple of hundred megabytes.

11 So what this command's doing here is 12 we're going to run a container, which is gonna be Jenkins, 13 and it's gonna be the long-term support version. 14 We're going to expose two ports: 15 8080, where we're going to connect on, 16 and 50000, which is used internally by Jenkins. 17 Secondly, what we're going to do is 18 we're going to create a volume on our local machine 19 and Docker will take care of this for us.

20 It's a folder that's gonna store 21 all the information for Jenkins. 22 Now, this is really useful, 23 because for whatever reason our Docker container stops, 24 we can rerun it using this command, 25 and we'll have all our information saved. 26 So now, let's go ahead and run it. 27 So let's copy this line. 28 Make sure we got Docker running, 29 so we can see Docker Desktop is running. 30 Awesome.

31 Go over to our terminal and hit Enter. 32 (key clicking) 33 So now, it's gonna go ahead and pull down the image. 34 This bit here is really important. 35 This is your key to log in with. 36 So let's copy that and store it somewhere safe. 37 And now, we can see Jenkins is fully up and running. 38 Now, let's go over to our browser, 39 type in localhost:8080. 40 Hit Enter. 41 Awesome.

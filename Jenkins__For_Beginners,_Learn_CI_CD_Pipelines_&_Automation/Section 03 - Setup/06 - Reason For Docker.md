# Reason For Docker

*Section: Setup*

1 Now that you've got Docker installed, 2 now it's time to get Jenkins up and running. 3 Let's quickly break down what we're doing here. 4 And to give you a bit of context, 5 if you're not familiar with Docker, Docker is like a VM, 6 except it doesn't install the complete operating system. 7 Instead, it's going to use the host's underlying kernel. 8 So, it means it's incredibly lightweight 9 and the images are only a couple hundred megabytes.

10 So, what is commands doing here 11 is we're going to run a container, 12 which is gonna be Jenkins, 13 and it's going to be the long-term support version. 14 We're going to expose two ports, 15 8080, that we're going to connect on, 16 and 50,000, which is used internally by Jenkins. 17 Secondly, what we're going to do 18 is we're going to create a volume on our local machine, 19 and Docker will take care of this for us.

20 It's a folder that's going to store 21 all the information for Jenkins. 22 Now, this is really useful 23 because for whatever reason our Docker container stops, 24 we can rerun it using this command, 25 and we'll have all our information saved. 26 So now let's go ahead and run it. 27 So let's copy this line. 28 Make sure we got Docker running. 29 So we can see Docker desktop is running. 30 Awesome.

31 Go over to our terminal and hit Enter. 32 So now it's going to go ahead and pull down the image. 33 This bit here is really important. 34 This is your key to log in with. 35 So let's copy that and store it somewhere safe. 36 And now we can see Jenkins is fully up and running. 37 Now let's go over to our browser. 38 Type in localhost:8080. 39 Hit Enter. 40 Awesome.

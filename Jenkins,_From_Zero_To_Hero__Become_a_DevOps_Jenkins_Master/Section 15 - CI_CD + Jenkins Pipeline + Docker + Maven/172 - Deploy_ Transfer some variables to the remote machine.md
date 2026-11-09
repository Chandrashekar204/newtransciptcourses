# Deploy: Transfer some variables to the remote machine

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to start taking a look at a deployment process. Well, and the first thing that you would need to do is find out how you're gonna transfer some variables to your remote machine. I mean, how are you going to transfer the build tech? How are you going to transfer the password for the registry? If you're using AWS, AWS already has services to do that.

If you are using Google Cloud platform, then probably Google Cloud platform already knows how to handle that. But as we are doing a super simple example in here we will be transferring the data using SSH and for your real applications you will find a way how to do it using AWS or using Google Cloud platform. I'm just gonna give you the hint so that you can know how to do that on your real world. Okay, so let's get started.

Let's go to our Jenkins data. Let's go to the Pipeline. And in here we're gonna go to Jenkins folder. Let's create a new folder that's gonna be deploy, deploy folder, and we will be using it later. So for now, let's take a look at how we can transfer the variables. So the first thing that we need is the name of the image that has being generated, right? So the image is Maven Project. Remember that we're generating the image with that name.

So that's gonna be the first thing that we need to transfer. So let's create a sample. Let's go to the deployment folder and let's go ahead and create a sample deploy file. Like Deploy.sh Let's hit enter. And in here we're going to say, okay, bin bash of course, say Bin Bash. And in here we're going to say, okay, echo maven project. Remember that's the image that we're generating and we're gonna transfer, we're gonna redirect this to slash tmp slash auth.

This is just a simple file that we're going to be creating to transfer later to the machine. So if we execute this script, let's execute it, deploy and you go to Cat tmp dot auth. You're going to find a file that contains the name of your application. Cool. So second thing is that we need to pass the build tag, right? The build tag that Jenkins is going to generate every single in every single execution.

So that's gonna be echo build tag and we're gonna pass it to slash tmp slash auth as well. And we're just gonna export the build tag variables. So that is available and we can test it. Build tag equals to 12, probably, let execute this again and let's take a look at the file that it's generated. Cool. Now we have here the name of the image and the tag that is generated. And the third thing that we need is of course the password.

So let's modify this and we're going to say like echo password and we're gonna pass it to slash tmp slash auth as well. Let's modify this. Okay, and remember, for testing, we're just gonna export this to 12345678. And now we're gonna test it, execute the script, take a look at the file, and you're gonna see all of your three variables. So you have the image, the tag, and the password for that image.

Cool. So now as you can see, our file contains everything we need to deploy our application and now it's time to transfer this file to that remote machine that we create to deploy the application. Remember, this is just a simple example to transfer data because probably if you are already in the cloud using AWS or GCP or Azure, there are already services for that but probably some people wouldn't have AWS or GCP accounts so that's why we're doing it just, you know, in a simple way of transferring a sample file.

So let's go ahead and transfer this file to our virtual machine that we created in this case to transfer a file using SSH it would be SCP, then we're going to say dash I and dash I. It's going to be used to pass the key that we created to connect to our machine. So in that case, remember that we have our key right here, which is prod. So let's say SCP dash I prod and then we say the file that we want to pass.

In this case it's tmp dash auth and we want to pass it to the prod user at Linux facilito dot online don't worry, this is my domain here. You should put your IP and then we say colon slash tmp slash auth. So this means we're gonna pass this file this local file to this machine, and we're gonna put the file in this location remotely. So let's hit enter, let's say yes. And as you can see, the file was successfully transferred.

Remember that this file contains three lines contains the name of the application, the image I'm in, the tag, and the password for the authentication. So if we now log into this machine using SSH dash, I prod prod user at this DNS, and we hit enter, you are gonna see that the file was transferred. So let's take a look at Cat tmp that auth. And here you see the file that was transferred from your Jenkins machine.

So that's super cool. Now, this would be the final step for our script to transfer the file to the remote machine. So let's copy this. Let's go to our Jenkins data folder, pipeline deploy or I mean Jenkins deploy. And here we're gonna modify the file again and we're going to transfer it using this. So that's cool. Remember that you need to have the full pad for this key. So in this case let's say that, or let's say like cp, the prod key that we have, we're gonna copy to OPT.

So in that way, let's say sudo 1234 so in that way we'll have the file in OPT will, we didn't copy that, why, let's copy it again. Set pre CP prod O to OPT. And as you can see, now we've got a key right here. So we can differentiate it using slash OPT slash prod. So let's modify that in here. Let's say that the key is located at slash OPT slash prod. And cool, now we can pass it. So that's super cool.

We can now generate a new file. So now we can simply execute our script and this file is gonna be generated and then it's gonna be transferred to the remote machine. So if you do deploy that SH, well let's give it executable permissions first plus X deploy and then you execute this file. The file is going to be generated and it's going to be transferred to the remote machine. And as you can see, now we have an entering here.

So let's do sudo change chown of this file. We're gonna give you the ownership to the user Jenkins which is gonna be 1000 this path. And now let's try again. And as you can see now, it was successful. So in this way you can generate this file that contains the information that your remote machine needs to know, and then you transfer that file so we can use it in the future. So this is it for this video.

I'll see you in the next lesson.

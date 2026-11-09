# Build: Write a bash script to automate the Jar creation

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to automate the process of creating the jar using Docker because probably you don't want to remember all of this from memory. This is going to be super boring. So let's create a script to automate this process. Let's copy this and let's go to, remember that now we're in the pipeline directory, so let's go to the Jenkins folder that we created.

Let's go to the build folder that we created. And in here we're going to save the script that is going to run this step. So let's create a new one, and then let's say like mvn.sh or something, and we can say /bin/bash, and we can do something like echo and a lot of asterisks, and we say echo again, and we can say like Building jar, like this, I don't know. I'm super bad doing these kind of things.

Let's go and do another echo, more asterisks in here. This is just to inform, you know, just to make it a little bit pretty. Okay so here, we're going to paste the line that we created there. And in here probably we want to reuse this script. So we're going to do something interesting. We're going to copy this command, which is the Maven command, and we're going to remove these lines, and in here we're going to pass this dollar sign, and this at sign, which means in Bash that we can pass parameters.

It means all of the parameters that this script is going to receive. So now we can save this and we can call our script like /mvn.sh, and we can pass this line, which is the line that actually creates the jar in Maven. I'm doing this because probably in the future, you may want to run some different Maven commands and you can reuse it in this way. So you can say like Maven test or Maven something.

Okay, that's cool. So now let's give it executable permission using change mode. And as you can see now it's green. So let's go back, back, at the same level of our Java application and we're going to execute it using Jenkins/build and Maven, remember that this is the full path for our script. So if we don't pass any parameter, probably this is going to fail because of course we haven't provided any goals, any parameters, so now let's go ahead and pass the parameters to build the jar.

So let's hit Enter and now it should work. And as you can see, this is actually creating the new jar and it's going to be saved in the Java app folder using this line, this script which is super cool because I think that this is easier than writing this super long code for this Docker command. So probably you will want to do this. Just go ahead and create your own Bash script to automate your process.

So in that way you know that the only one thing that you need to do is to execute your script, and then you're going to pass the parameters for that script. So let's test that it works. Remember that our jar is being generated under Java-app and target, here is the jar that is being generated. So let's go ahead and remove that jar from this directory. Okay, let's do Java, target, and my something.

Hit Enter. One, two, three, four. And now you can see that we don't have the jar anymore. There is not the jar. So let's execute our script and let's see if this works. Okay, so this is cool as you can see it finished. And now if we take a look at our Java target directory, you're going to find your jar there, which means that our process is actually being executed successfully. So this is it for this video.

I hope that you have learned how to create a simple batch script to automate your processes. So this is it for this video. I'll see you in the next lesson.

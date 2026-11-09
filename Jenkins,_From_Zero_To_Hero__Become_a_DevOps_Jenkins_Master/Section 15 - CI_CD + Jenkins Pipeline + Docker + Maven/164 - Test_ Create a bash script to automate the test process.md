# Test: Create a bash script to automate the test process

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello, and welcome back. In this video, we're going to create a script to automatically execute this command. And that means testing our code automatically, just executing a script. So the first thing that we're going to do here is that we're gonna create a directory under the Jenkins folder. Remember that right now, we are in the pipeline folder at the same level of the Jenkins file. So let's go ahead and create a new directory in the Jenkins folder that's gonna be called test.

So let's go there, Jenkins test, and you can see that we have nothing. So basically, we need to create a script using this line. We already had that, so let's copy that script from the build, maven, and we're gonna paste that in here. So let's modify this script. And we're going to say now, echo fielding, I mean, testing. So we say testing the code. And then we do exactly the same thing, we're gonna keep it like this and we're gonna save it.

We're gonna give it executable permissions. Cool, so now it becomes green. Now, let's go to the level of the Jenkins file. I think this is right here. And now we can execute our script simply by doing Jenkins test maven, and then we say maven test. You can call this script as you want, this is just for you to understand. So if we do this, as you can see, now we're testing the code. Well, we can just fix this later.

And as you can see, the tests are going to be run just simply executing this line. Please make sure that always you are at the same level of the Jenkins file because from here, Jenkins is going to run everything at the same level of the Docker file. So everything you do should be using this relative paths. Okay, so this is it for this video. You already know how to create a script to automate your testing process.

I'll see you in the next lesson.

# Test: Add your test script to Jenkinsfile

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to add our script to our Jenkins file. So remember that in order to test our code, we already created this script, and this is the line that we need to execute to test our code. So let's copy that and let's go to our Jenkins file, and we're going to modify our test step. So we're going to do something like SH, and we're going to execute this line.

So far we have our stage that is a build stage, and in here we're packaging a yard, and then we are creating a Docker image using this yard that was created in here. And then in our test stage, we're actually testing the code to check if everything is working as suspected. So this is as simple as this. Our test stage is only going to have one script, which is going to test the code. So this is it for this video.

I'll see you in the next lesson.

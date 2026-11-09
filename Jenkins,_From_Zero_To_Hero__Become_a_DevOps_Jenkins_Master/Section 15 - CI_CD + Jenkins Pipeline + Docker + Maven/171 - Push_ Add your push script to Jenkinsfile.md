# Push: Add your push script to Jenkinsfile

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to add this script that we just created to our Jenkins file. So let's go to the folder that contains our Jenkins file, and remember the full path to your script. So that becomes jenkins, push and push.sh So if you execute this line, then you're going to be executing the script that is going to push the image to your Docker Hub repository.

So let's wait until this finishes, and we're gonna copy this path. Okay, cool. We're going to modify our Jenkins file and we're going to go to the push section. And in here, we're just gonna call the script that we created. So we're gonna paste that in here, and that's super cool. Now, as you can see, it's actually taking shape. You have your build section where you are building your jar, creating a Docker image.

Then you are testing that code. And if the test are successful, then you're going to push the image that you just created using the field tag and all of the environment variables that we created to your Docker Hub account. So this is it for this video. I'll see you in the next lesson.

# Modify the path when mounting Docker volumes

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. In this video, we're going to do a couple of modification to our build and test scripts. Remember that I told you that everything is going to happen inside of the pipeline Docker-Maven workspace. So everything is going to happen in this folder. So let's go out of here and let's go to our Jenkins data pipeline Jenkins. And here we're gonna grab recursively for PWD.

And you're going to find two results, your build folder and your test folder. And here we're going to have a small issue because we're using the Docker sock. Do you remember? Inside of the container. Then Docker is going to think that PWD will refer to the host PWD and not to the container. So to fix that, we will need to graph the entire path for the workspace of the pipeline. We're gonna copy this and we're going to modify our scripts.

So we're gonna modify the Maven that is H and we can create here a variable that is called workspace or as you want. We're gonna paste the value here. And then here the law, instead of saying PWD, we're going to say workspace. Yes. So we need to do this change in the other script. So let's save this and let's do exactly the same thing. So we're gonna create the project, the workspace. So let's say workspace.

And remember that everything happened inside of the workspace. So whenever a pool of new code occurs, then you're going to be pointing to your workspace and then to the new code. So let's save this and probably you will want to push this to your repository. So let's do Git status. You will have your two files modified there. So let's do git add build and test, and then Git commit dash M and you say fixes path or workspace path for jobs execution, or something like that.

Just do it, Git push, and then you are ready to go. So this is it for this video. I'll see you in the next lesson.

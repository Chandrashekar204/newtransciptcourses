# Post actions

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video, we're going to learn about post actions in Jenkins files. Well, let's take a look at the post-actions file. And as you can see, we have everything the same thing, pipeline, stages, and here we have an step, which is echo Fail, and then we have an exit 1, which in Bash means error. And here at the same level of the stages, we have a new thing, which is the post.

And the post actually have a lot of possible cases. So here we have some examples for you to understand. always, this is always going to be executed. success, if the job success, then and only then this is going to get executed. failure, if the job fails, then this is going to be executed. unstable, if the job was failing and now it's recovered, then this is going to be executed. An important thing in here is that you can use one, two, three, or four, you can use all of them, you can use one or two, you can use the ones that you need.

So let's go ahead and copy this and let's take a look at the pipeline. Let's go to our pipeline project, let's configure it, and let's take a look at some cases in here. So let's remove the old code. Let's paste the new one. In this case, it says echo Fail and this is actually failing. And what do you think that's gonna happen when it fails? Well, when it fails, it's going to fall in here and it's going to say, I will only get executed if this fails.

So let's save this. Let's build now and let's see what happens. And as suspected, we actually have in here our error. So let's go to the Console Output and let's see what happened. And as you can see, here we have two things. The first one is the always instruction, which is this one. I will always get executed, this one. Second one is the failure instruction in here because it actually failed, so this is why this is prompting, because we said if this fails, then please execute this piece of code.

So, super cool. Now, let's take a look at some more cases. Let's go and remove this echo Fail and this exit 1. Let's do echo I am good. Let's save this and let's build this now. And now this shouldn't fail. So let's take a look at what happens. What do you think that's going to be executed? So let's go here, Console Output. And as you can see, we have I will always get executed because this guy will always be executed, and I will only get executed if this success.

This is this instruction, so that's super cool. And as I told you, you can use one or two or three, you can use as many post actions as you want. So don't worry, this is only a little bit of theory, because in the next section, we're going to be using everything we learned about pipelines and we're going to build our own pipeline using the Jenkins file, everything that we learned, and a lot of new things.

So I hope you've learned a lot from this short section. I'll see you in the next lesson.

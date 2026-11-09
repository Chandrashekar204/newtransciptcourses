# Deploy your Jar locally

*Section: Jenkins & Maven*

-: Hello and welcome back. In this video, we're going to learn how to deploy the jar that we are building in the jar that actually passed all the tests. So for this, we're going to go to the configure section. And remember that, or this is something pretty important the first thing is downloading the new code. Second thing, building the jar. Third thing, doing tests and tests are super important because tests inform you how your application is behaving.

Is your application behaving as you thought? If not, then the job should fail and nothing else should be executed. I mean, you shouldn't deploy your jar unless all of the tests are correct because if you deploy a jar with failure test probably your application is going to behave weird. So, okay, now we're going to deploy it because our tests are actually passing. And if Maven finds any test that is actually failing or that's not correct then that job by default, it's going to fail, right?

So we're going to add a new build a step and that's gonna be a shell, a shell step. But before doing that I wanna show you where the jar is being located. Remember, oops, remember that if we go to the output of this execution, we should have the jar around here. Here is the jar. So this is the jar that actually it's being generated. So we're gonna copy this full path. Remember that this is inside of the workspace name of the job, and then this is Maven creating a target folder and saving the jar there.

So we're gonna copy this full pathway here. I'm just gonna copy that and we're going to configure this job. We're going to add a new step, which is a shell step and we're going to say something like echo. We're going to put asterisks in here. Then we're going to say, like, deploying jar. And we're going to do another echo with asterisks just to you know, for this to look good. And in here, to deploy a jar normally you should use Java dash jar and the full path or the relative path for the jar.

In this case, we know that the jar is always being built with this name, with this path. So, we're going to deploy that in this way and then we're gonna see what happens. So let's go ahead and save this and let's click on build now. And we're going to go to the execution console output and we're gonna see what happens. Let's wait until this finishes. And as you can see, this is actually deploying the jar.

So Java dash jar and the path for the jar that we actually built in this case. And this output is Hello World! So congratulations. You are already doing a continuous integration and continued deployment process. So you are retrieving the code from Git. You are building your jar, you are testing it and finally you are deploying your jar locally. So remember that everything is happening inside of your Jenkins container.

If I copy this line and I go inside of the Jenkins container, I am already inside. And if I paste this you're going to see exactly the same output, because Jenkins or the Jenkins container has Java already installed. So pretty cool. This is it for this video. I'll see you in the next lesson.

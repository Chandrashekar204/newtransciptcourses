# Retry

*Section: Jenkins Pipeline - Jenkinsfile*

-: Hello and welcome back. In this video we're going to learn about retries in pipeline. Well, and as you may know retry is nothing else about trying again. So let's take a look at our retry file and you are going to see this simple configuration. So here we have our pipeline, our agent, and our stages. So we are going to have one stage and it's going to be called Timeout, just for reference. And the steps for this stage are defined in here.

So you can see that we have a retry with a number three and then we have what we want to retry. So here we have an sh command and this sh command is going to execute this. And probably if you're a little bit familiar with Linux you know that if you execute this in a terminal this is going to fail because I is not a valid command in Linux. So this is going to fail. This command is going to fail but we want to retry this command three times because normally if a process in your pipeline fails then for some reason you may want to retry it.

So this is how you do it. So let's go ahead and copy this content. Let's go to our configuration, our pipeline job and we're going to go to the configure section. Let's scroll down till we reach our Groovy Sandbox. Let's copy this. Let's paste the new code, and let's save this. Now we're gonna test it, build in it. Let's click on build. And as you can see, now you only have these new box because this doesn't relate at all with the previous boxes.

So this is why you only have one. And as you can see, it was marked as failed. Okay, so let's take a look at logs. If you put the code in here you're going to find all of the three logs. As you can see, show script return, exit code, exit code and exit code, three logs. Now, let's click on this console output. Let's go here. And as you can see, we have this. So it says, I'm not gonna work, and it shows you the error that we were expecting, I not found.

And then after the first time that it fails it's going to retry. Second time it fails. Let's go ahead and retry. And as you can see, we actually retried three times. So probably in your process you may have something that you need to be retried and this is how you do retry using pipelines. So this is super cool. You already know how to retry a command in your Jenkins pipeline. This is it for this video.

I'll see you in the next lesson.

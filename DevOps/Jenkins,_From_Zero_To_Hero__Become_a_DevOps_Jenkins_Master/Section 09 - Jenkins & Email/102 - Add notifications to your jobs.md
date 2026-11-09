# Add notifications to your jobs

*Section: Jenkins & Email*

Instructor: Hello and welcome back. In this video, we're going to learn how to integrate these notifications to our jobs. So we're going to be using this ENV job that we created. So let's go ahead and use it. And we're going to configure this. We're going to go to the last part and you can find these post-build actions. So in here is where we're going to add the email notification. So let's click on this and you're going to see email notification.

So let's click on this and you're going to see two checks in here. So we're going to send email for every unstable build and we're going to send emails individuals who broke the build, you know. So this way we actually have all the information covered by email. So who's gonna be the recipient? Well, it's going to be my email or your email. So type your email in here and the mails are going to be sent to this particular mail that you're providing here.

So we're going to make our job fail. So let's do something like echo1. You know that this camera doesn't exist. As you can see, it's actually in a different color because it doesn't exist and this command is going to cause the job to fail. So if we save this and now we built this project, it's probably going to fail. And as I told you, it actually failed because the command echo1 doesn't exist. And as you can see here, let me show you, echo1 not found.

And as you can see here, this was marked as a failure and therefore it's going to send the notification to my mail. So if we head to our Gmail and we look for our inbox, you're going to have a Jenkins message telling you the build fail in Jenkins and the project environment, the number eight. If you go and up and up the mail, you're going to see the entire output of Jenkins, but not in your mail. So you can scroll down and you can see that, "oh, look at this.

Echo1 is not found." And that's why this is actually marked as failure. So okay, I just received this mail. I'm just going to go ahead and modify the configuration back so I can revert the changes. Let me remove the echo1. I'm just gonna remove this and then I will save this job and let me execute this back. This should work because now everything works perfect and there are no errors in our job. So this should be blue.

And as you can see, this is blue. It means that the job was unstable for one second because you know it was failing and now it's not failing anymore. So if you go again to your mail, you're going to find something here that says, "Jenkins bill is back to normal," and it's going to show you the name of the job and the number of the execution. And it's only informing you that the job, it's already normal And that this is not failing anymore.

But what happens if we execute the job again? Do you think that you're going to get a notification? So I click on the bill button and now we have a 10 execution in here. But if you go to your mail, you're going to find nothing because the job is already working good. So in here we had an event, which was failure and in here we have another event which was something like a recovery from the failure.

But in here, this is normal. We don't have events so that's why we don't have any mail here. So cool. You already know how to integrate mail notifications to your job. So whenever a job fails, you're going to know why this failed because Jenkins is going to send you an email. Isn't it cool? So I'll see you in the next lesson.

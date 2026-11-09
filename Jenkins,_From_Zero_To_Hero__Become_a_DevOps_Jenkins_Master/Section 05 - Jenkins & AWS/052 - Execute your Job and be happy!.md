# Execute your Job and be happy!

*Section: Jenkins & AWS*

Instructor: Hello and welcome back. In this video, we're going to test our project. So let's click on Build with Parameters and let's see how it looks like. It looks great, right? So in here we have some parameters that user can change. So in this case, we have default values. In this case, we have db_host, testdb, and the bucket to upload the file to. So what happens if we're going to click on the Build button?

Let's click on this and let's see what happens. So as you can see, our job executed successfully. So let's click on this. Let's click on Console Output. And as you can see here, this sensitive information is being passed using asterisks, which means that no one knows the values for this sensitive information, which is pretty cool. So if you see here, this is what Jenkins is actually doing and it's executing the script, passing the parameters, and here you can see that this is the message that we created that says, uploading your db.

And now this is the output of the AWS S3 command, which is pretty cool. So this is the name that actually was created. So let's go ahead and copy this. Let's go to our console in S3. Let's reload this. Great, and let's look for it. Pretty cool. So our script is working like a charm. Our Jenkins job is working pretty nice, so let's build it again. And the cool thing about this is that, for example, if you have someone who doesn't know about MySQL, or he doesn't know about Linux, or doesn't even know about Amazon Web Services, but you want that person to be able to upload a backup to AWS, you are just going to tell that person, "Hey, look at this.

You just need to click the Build button. And then the process is going to be automatically done." Cool, isn't it? So let's build it again and let's wait until this finishes. Cool. We have the execution in blue, which means it was successful. Let's go ahead, let's look for the new name. This is a cool part because your backups are going to have different names always. So let's refresh this and let's look for that name.

And this is in here. Perfect. So you already created a Jenkins job that takes a backup from MySQL database and upload that backups to S3. So this is it for this video. I'll see you in the next lesson.

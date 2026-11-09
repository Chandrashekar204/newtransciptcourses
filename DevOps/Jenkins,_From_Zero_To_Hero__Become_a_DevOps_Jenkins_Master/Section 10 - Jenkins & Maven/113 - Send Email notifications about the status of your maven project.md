# Send Email notifications about the status of your maven project

*Section: Jenkins & Maven*

Instructor: Hello and welcome back. In this video, we're going to integrate email notifications using our Maven project that we created. So let me open up my mail and now we're gonna configure this and hopefully, you already know how to add notifications to the job. So, let's go and add a post-build action, which is going to be email notification. And we're going to add my mail or your mail (keyboard clacking) and we're going to click on both of these things and we're gonna click on save.

So now I actually opened my mail and we are going to make this fail by passing an incorrect parameter in here. For example, something like this, which is pretty professional actually, and we're gonna click on save. And now if you build this, this is going to complain because that flag or the thing that you actually type doesn't exist, which means that your job is not correct and which means that a mail should be sent to this email because your job is not correct and your job is failing because of some reason.

So, we're going to go to our mail, and as you can see, we have the error in here and you have everything, all the output in here, and you're going to find the error. So, you can just go ahead and look for it and let's look for the error and here you can see the builder requested. This doesn't exist. What is this? This is the thing that we added. And as you can see, that's actually been passed as a flag.

And Maven is saying, "Hey, what is it?" And that's why your job is failing. So once you figure this out, you say, "Okay I'm just gonna fix that," because you got a notification on your mail so that you go to configure your job because you know what's happening or probably a test is failing so you can call your developers and tell them like, "Hey, your tests are failing. "Please do something," or whatever you want.

But for now, we're just going to remove this thing that we added. We're gonna click on save, and we're gonna build a project. And now it should build without any problem. So, at the end of this execution, we should have a new mail informing that everything is working good and that you can sleep without any issue. So let's go and see what happens. Everything is going good. Our jar was deployed, the mail is being sent.

It was already sent. So, if you go to your mail, you're gonna find out a new email that is telling you, "Hey, your build "is back to normal." So be happy and go and have some beers or whatever you want. So, if you go back, you are going to see your project that now is working and that's pretty cool because you don't have to be every single day looking at the dashboard to know what is failing. Jenkins is just going to send you an email and you're going to be happy.

So this is it for this video. I'll see you in the next lesson.

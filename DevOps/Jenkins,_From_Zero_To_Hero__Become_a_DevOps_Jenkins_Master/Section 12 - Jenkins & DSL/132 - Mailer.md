# Mailer

*Section: Jenkins & DSL*

Instructor: Hello and welcome back. In this video, we're going to learn how to configure the mailer or the mail step using DSL. So let's take a look to our mailer file, and you're going to find exactly the same thing that we did before and I actually added here a new shell step. So you can see that you can add one or two or three, as many as you want. And now we add a new section, which is the publishers.

And in here, you have the mailer, and then you specify the email where the notification is going to arrive. And you define the two boxes that we normally click, true and true. This simple. So let's go ahead and copy this. Let's go to our DSL job. Let's configure this and we're gonna paste this new code in here. Let's delete the current one. Let's paste this, hit save and build this job and see what happens.

The execution was success. So let's go to the dashboard. Let's look to our DSL example. Let's click on configure. Let's scroll down. And now you can see that in the post-build actions, we have already configured this email notification. And the email or the recipient is going to be me@example.com and that configuration is made in here. So you can change the mail to the mail that you want. And this is pretty cool.

Remember that if you want to know more about this, you can always go to the documentation and look for publisher. Let's go to the FreeStyleJob. And we have a lot of publishers, so let's look for mailer maybe. So let's click on this and you're going to find out how to use this from the documentation. So this is it for this video. I'll see you in the next lesson.

# Triggers

*Section: Jenkins & DSL*

Instructor: Hello and welcome back. In this video, we're going to learn about triggers. So let's take a look to the triggers file that I will leave you. And as you can see, we're now adding a new step in here, which is triggers, and we're adding a cron expression in here. So this means that our job is going to be configured in such way that it's going to be triggered using this cron expression. So let's go ahead and copy this.

We're going to go to our main job. Let's go to Jenkins. Let's go to the DSL job, which is the seed job. Let's go ahead and configure this, and we're going to add this new code. So let's delete this. Let's add this code. Let's go ahead and save this. So let's click on Build. The execution succeeded, so let's go outside of here. Let's go to our job D as an example. Let's click on Configure. And as you can see, the configuration is already in place.

We have our source code management, and now we have the trigger already configured. And as you can see, the Build Periodically option is marked, and this kettle is the expression that we passed in this VSL script. So this is perfect. You already know how to trigger your job using a chron expression, and you know how to configure that using DSL. So this is it for this video. I'll see you in the next lesson.

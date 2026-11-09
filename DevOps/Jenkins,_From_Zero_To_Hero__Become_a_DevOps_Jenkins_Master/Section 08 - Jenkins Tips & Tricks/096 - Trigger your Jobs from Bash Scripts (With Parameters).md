# Trigger your Jobs from Bash Scripts (With Parameters)

*Section: Jenkins Tips & Tricks*

Instructor: Hello and welcome back. In this video, we're going to learn how to trigger Jenkins jobs that accept parameters. For example, if you go to your anisible-users-db, you're gonna find out in here that if you click on build with parameters, you need to provide input. Let's go to another one. For example, the backup-to-aws. You actually have to provide like three parameters in here. So how do you pass those parameters and how do you trigger this job from a script?

Well, that's what we're gonna be learning in here. So I'm just gonna leave you this file that I showed you in the previous lesson. I'm just gonna un command this and command this out. And the thing is pretty similar. We will always need to retrieve the crumb. So we're always going to be using this crumb. And as you can see here, we're doing exactly the same thing. We're getting authenticated with the Jenkins user.

Then we're passing the crumb, we're doing a pass to the entire name of the job but now we're passing parameters. So let me show you. If you go here and you right click on copy link address and you paste that in here you're going to see the same thing that you saw before. But in order to pass parameters you need to do build with parameters. You need to pass this expression instead of passing a build, because you're going to pass parameters.

So okay, the first thing that we need to do is that we need to make sure that this is the name of the job. So let's capture the name of the job which is backup-to-aws. Let's copy that and we're gonna paste that in here. So build with parameters is always going to be there. And in here we're going to pass the parameters. So in order to pass the first parameter, we need to include this question mark in here.

And then we pass the first parameter. In this case, the first parameter is the MYSQL_HOST. So let's copy that parameter, and we're gonna paste that in here. And we're gonna pass the value. In this case, we want the value to be the db_host, right? So the second parameter is going to be followed by an ampersand sign, and we're going to pass the second parameter which is the DATABASE_NAME. So let's copy that name and we're gonna paste that in here.

And we do an equals and we pass the name of the database or the value for this variable. And the third it's going to have also an ampersand sign in here, that we're going to pass the name of the third parameter which is AWS_BUCKET_NAME here. So let me remove this, copy and paste. And then we pass the value. In this case, this is the name. So we're gonna copy that in here. We're gonna paste that. And that's it.

You already have your entire URL to build your job with parameters. So remember again, we're generating the crumb here. We're getting authenticated with the Jenkins user. We're passing the crumb. We're doing a POST to the URL of the job. And in this case, we're using parameters. So we need to pass build with parameters. Question mark first parameter ampersand, second parameter, ampersand third parameters.

And you can pass all the parameters that you want. So okay, we're gonna copy this. Let me copy this all, and I will go I will open my crumb, that is age, I will remove this, and I will paste the thing that we created in here. It's time to execute it and see what happens. If you see the last execution of this was the number six, let me reload. Cool. If now I go to my console and I execute the crumb.

Remember that our crumb is actually going to execute this line, which is pointing to the backup-to-aws, and it's going to pass these parameters. So let's go ahead and execute our crumb. Enter. And as you can see, doesn't complain. Let's go to our Jenkins job. And you can see the execution going on. But in this case as I show you in the video, I already deleted the aws key and access key, so they are no longer available.

That's why this script is complaining. But the thing that I want you to see is that we're able to trigger this job from a sample script. So if we execute this again, you are going to see the number eight execution going on, which is pretty cool. It's going to fail again because I already deleted the case. But for example, if I wanted to build another job I am just going to go to the dashboard and I will be picking up the ansible users.

And remember that this guy actually receives one parameter which is the age. So let's go ahead and we're going to modify this. We're gonna trigger this job, which is the ansible-users-db. So let's go ahead here and we're gonna modify the job in the URL. And this is ansible-users-db. And in here, remember that we only need to pass one parameter. So we're going to remove all of these parameters and we need only to pass the age parameter.

So let's copy the age, and we're going to give a number for example, 25. The last execution of this was the number two. So let's see, we're going to pass 25. Let's save this, and we're going to execute this out. And as you can see, the third execution is actually going on right now. If we go inside of the execution console output you are going to see that the Jenkins user was actually the user that triggered this execution, passing the parameters that we are providing from our script.

So this is pretty cool. You already know how to trigger a job. You already know how to pass parameters, how to trigger jobs without parameters, and everything from a batch script. So this is it for this video. I'll see you in the next lesson.

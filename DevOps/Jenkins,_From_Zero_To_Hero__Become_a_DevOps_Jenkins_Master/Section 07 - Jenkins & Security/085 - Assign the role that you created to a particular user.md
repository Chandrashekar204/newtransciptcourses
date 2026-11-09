# Assign the role that you created to a particular user

*Section: Jenkins & Security*

Instructor: Hello and welcome back. In this video, we're going to learn how to assign the role that we created to a particular user. So I want you to know that a role by default does nothing. You need to associate that role to a specific user in order to attach permissions. So for example, if we now open up an Incognito tab, and we type jenkins.local, and we try to log in using the tom user, the password, we're going to see an error in here.

It's because even when we already created the read-only role, we haven't assigned that role to the user. So to do that, we need to click on the Assign Roles. Remember, if you don't know how to reach this, you go to the Manage Jenkins section, you scroll down and you look for Manage and Assign Roles, and then you click on the Assign Roles, and in here you are gonna see that you have something like a table.

And in that table, you're going to have an admin role and a read-only role that you created. And as you can see, no one is using this role currently, but the Jenkins Admin user is actually using the admin. So to add one user in here, we're going to add the tom user that we created. Please make sure that the user that you try to add is currently available. So let's hit Add. And in here we're going to say, okay, I want this guy to have the read-only role that I created before.

So let's go ahead and Save this. And if we now go to our Incognito tab and we reload, you are going to see that the error is gone and you already have a little bit of read permissions. You still can't do nothing in here because we haven't allowed that yet. But as you can see, the error is no longer there. So where are the jobs? If we go to the Jenkins home here, the jobs are in here, but why the user tom can't see those jobs?

Well, and that's because we haven't allowed that yet. So if you want to allow the user toms to view all of the jobs, then you go to Manage Jenkins, you go to Manage and Assign Roles, and remember that if we go to Assign Roles, we have the user tom associated to the read-only role. So we're going to modify it in Manage Roles, we're going to modify that read-only role and we're going to allow the users to read a job.

So as you can see, we have another row of Read, which is this read that allows you to log in without errors. Then you have Credentials, Jobs, Run, and a lot of stuff. So for now, we only mind about Jobs. So we want this user to be able to read. So we mark the Read option under the Job title in here. And as you can see now, we have two permission, an Overall Read permission and a specific permission, which actually allows you to read all the jobs.

So if you move to the name through the header, you're going to read like see a job, you may deny permission, but allow Discover and blah blah. It's actually giving you a summary of what this does. So I'm just gonna click on Read and then you're gonna click on Save. And now what you just did is that you modified that read-only role that you created before. And remember that that role was associated to this tom user, which means that if we go to our Incognito tab and we refresh this then the user is going to be allowed to see the jobs.

But what happens if the user enters or goes inside of one job? Well, this user can't do anything because it only has read-only permissions. It doesn't have any delete or any configure or any build buttons in here because we haven't all allowed that yet. So you already know how to create a role, a read-only role, with certain permissions, and how to associate that role to a certain user in order to allow certain capabilities to that particular user.

So this is it for this video. I'll see you in the next lesson.

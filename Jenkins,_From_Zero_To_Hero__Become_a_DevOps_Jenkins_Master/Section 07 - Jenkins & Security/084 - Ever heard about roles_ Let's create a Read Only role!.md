# Ever heard about roles? Let's create a Read Only role!

*Section: Jenkins & Security*

Instructor: Hello and welcome back. In this video, we're going to learn how to create roles. Before doing this, I want to remind you that if, now, we open up an incognito tab and you try to log in using the Ricardo or Tom user, you're gonna find out errors, and that's because we don't have any role or any permission associated to this user. So, we're gonna fix this right now, and we're going to go to manage Jenkins, and we're going to scroll down, looking for manage and assign roles.

So, let's click on this. And we have manage roles and assign roles. So, we're gonna click on manage roles. So, cool. Now, let's say that we want to add a new role. So, what's a role? A role is basically something that defines permissions. In this case, we have a role which is an admin role, and this admin role actually has capabilities to do all of this. For example, if I wanna create a read-only role, I'm just gonna click on add, and then it's going to ask me for which permissions I want this role to have.

So, for example, I want read-only permissions for this role. I don't want this role to be able to administer or to create or to delete or to update. I don't want anything. I only want read permissions for this role. If you want some other permissions in this role, you can just go ahead and click, for example, on build or on configure jobs or create jobs or run jobs or view jobs, or do whatever you want.

So, we're gonna save this in here. We're gonna scroll down and hit on save. And congratulations, you have just created your first read-only role in Jenkins. So, this is it for this video. I'll see you in the next lesson.

# Test your playbook and see the magic!

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. In this video, we're going to test the playbook that we created. So for this we need to first copy the template that we created in here, which is the table file, the table template, where we have this small logic. So we're gonna copy this to the container. So let's do a copy. Okay, first, remember that I am located at Jenkins Ansible folder where we have our table.

So let's copy that table to the Jenkins home Ansible. Remember that in this place, we have the shared volume between the house and the container. So if we copy this file in here, then we're going to be able to access this from the container. So now we just need to go inside of the Jenkins container, and let's go to the Ansible folder inside of the container. And you are going to see your people.yml file, and you're going to see your table file, which is your template. Cool.

So now we're gonna execute this playbook, which should transfer our template to the remote host. So for this, let's do an Ansible playbook, and we're going to do -i to specify the hosts, and then we're going to specify the name of the playbook, which in this case is people.yml. So let's run this, and let's see what happens. Probably we're going to have an error here. So let's wait. And as I told you, we have an error here because this location on the web container is not readable.

But why? Let me show you, let's go out of this container, and let's go inside of the web container. Let me fix this. Let's go to var ww, and if you look for the permissions, you're going to see that the root user is the owner of that directory, and we're trying to connect to this container using that remote user, so the remote user can't write here because this directory is owned by the root user.

So to fix this, we're going to do something cool, which is change owner, remote user, remote user, and we're going to give the ownership of this directory to the remote user. So we specify the full path var ww html, and you give it recursively. So hit enter and if you now do an ll to var ww, you're going to see that that remote user is now the owner of this directory and should be able to write in here.

So let's go outside of this container, and let's go inside of the Jenkins container, and let's try again. Ansible, we're going to run the playbook again, hit enter, and now it shouldn't fail. So let's see what happens. And as you can see here, now it doesn't complain anymore. Now let's take a look at the web server. Let's type jenkins.local on port 80. And you're going to see all of the records in here, and that's because of the logic.

So let me show you the table. So what happens if People Age is not defined? Then this line or this piece of code is not evaluated, therefore this is only the query. But if People Age is defined, then this piece of code is going to be added. Otherwise, then this is only going to be the query. But what happens if we define this variable? Let's define this variable using an extra variable. We know how to do this from Jenkins, but we don't know how to do this from the terminal, and that's pretty simple.

You just define -e and then you pass your variable. For example, in this case, People Age equals to, for example, 25. So let's hit enter and see what happens. Okay, Ansible didn't complain at all. So let's go to our web server, and let's refresh. And as you can see, we're only having the answer or the result for people who only have 25 years. And how is it even possible? That's because remember in our table, we're defining this little big logic, which is possible thanks to the Jinja templates.

Remember that if we don't define this variable, then the query is going to be this. But if we define this variable, then Ansible is going to add this piece of code to the query, and the result is going to be that you are going to be presented with the results that match your request. So this is pretty cool. I'll see you in the next lesson.

# Ready? Let's create a Jenkins Job to build everything with a click!

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. In this video, we're going to create the Jenkins job that is actually going to do all the magic. So we're just gonna do a click and then everything is going to be done. So for this, let's click new item, and let's call it, for example, like, ansible-users-db, or whatever you want. So let's click on freestyle project and click on OK. Now, the first thing that we want to do is that we wanna create a parameter in here.

So let's click on this project is parameterized, and let's add a choice parameter. So we're gonna call it, for example, AGE, and we're going to put choices in here, like 20, 21, 22, 23, 24, and 25, so the user can pick any of these options easily. Cool. So now we want to go to the build environment and invoke an Ansible playbook. So you know these already. Let's go to the Jenkins container, let's go to the Ansible folder, and let's start populating this information.

So remember that the full path for your playbook is your PWD plus the name of your playbook, which is people.yml. If you hit enter, you're going to have your full path. So you copy this, paste this in here. We're going to choose the inventory as a file and we're going to do exactly the same thing. Copy this, and remember that your host file is your inventory file. So if you type this, then this is going to be the full path to your hosts file.

So you copy and paste this in here. Let's colorize the output of this, click on this option. Now we go to the advanced section. In here we're going to colorize the output and we're going to add an extra variable. So remember, the key, it's going to be the key that we define on the table template, which is going to be the key that Ansible expects, PEOPLE_AGE. So let's paste this in here. And the value, it's going to be the value of the Jenkins parameter.

In this case, it's going to be AGE. So let's copy the Jenkins parameter, and let's put this as the value for this extra variable. So we have these completed, let's click on save. And now, if we build with parameters, let's choose, for example, my age, 21, and let's click on build. Let me reload this. And if now we go to the execution of this, we're going to see that we have colors and the execution was successful.

So let's go to our web server on port 80, and you're going to see only the people who have this age. So let's go back and let's choose another age in here. Let's say age for 25 years, or 23. Let's choose this, let's click on build, and now we're going to go to the execution of this job, wait until this finishes, and then we're going to reload this table to see the output of that. So, queue, as you can see, already finished.

Let's refresh this, and you're going to have people who only have 23 years. So, this is pretty cool. You have a job that actually allows you to print an HTML table with CSS that does a query to a database using PHP based on your input. So if you want, for example, people with 20 years, then you build it and Ansible is going to do the magic, put in the template to your web server, and then whenever you refresh, you're gonna find information that you want, and everything is being done only with one click.

So, you have learned a lot in this section. You learn how to create a database, how to create a web server, how to integrate those guys, how to create a Jenkins job, how to integrate Jenkins with Ansible, how to use a little bit of HTML, CSS, PHP, and how to integrate this all to make one simple task that is clicking a button in order to see a huge result. So, this is it for this video. If you have any questions or any doubts, please make sure that you watch the video again and you understand everything.

Hope you have enjoyed this. I'll see you in the next lesson.

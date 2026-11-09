# Learn how to execute Playbooks from a Jenkins Job

*Section: Jenkins & Ansible*

Instructor: Hello, and welcome back. In this video, we're going to learn how to execute a playbook from Jenkins. So the first thing that I wanna do is that I wanna go inside of the Jenkins container so that we can know where we are, and we're going to go, oops. Let me go inside of the Jenkins. And the first thing that we're going to do is that we're going to go to the home folder, to the Ansible folder, where we have all of our files.

So queue, here we are. So now let's go to the console and let's click on New Item. And we're going to call this Jobs You Want. So let's say, like ansible-test, for example. It's going to be a freestyle project, so let's click on Okay, right. So in this case, we're going to go down and look for the Build section. And in here we're gonna click an add a build step, and we're going to look for Invoke an Ansible Playbook.

Cool, so once we click on this, this screen is going to appear and we need to start populating all of these requirements. So the first thing that we need to provide is the playbook path. So let's look for our playbook inside of the container. If we do an LS, we're going to find our playbook in here. So the full path for this would be PWD, plus the name of these files. So let's copy this, copy slash, and then you give the name of the playbook, and then you are going to have the full path for this playbook.

So let's go ahead and copy. Let's paste this in here. And now we're going to specify the inventory, the hosts file that we created. So it's going to be the same thing, PWD. We're gonna copy this, and then the name of that file is hosts. So if we do an LS to the path that we copied in the hosts file, we're going to have the full path for this file. So let's copy this and let's paste this in here. And now let's look for Advanced, and let's see what we can run.

So I think this is okay for now. So let's click on the Save button, and we're gonna click on the Build Now button in Jenkins. So as you can see, the execution already started. Let's go to the console output for this job. And as you can see, Jenkins is showing exactly the same screen that we saw before when we run the playbook manually. And as you can see still, we have the same result. Everything is working good.

Here we don't have colors, but in future videos we're going to learn how to color this screen, right? So let's look for the remote host in here. Let's go out of the container. Let's go inside of the remote host container and let's look for the tmp ansible file. The file is there. So we want to modify the content of the playbook, but now we're going to make it easier. So we're going to go outside of this folder at the Docker composed file level.

And if we do a VI outside of the container to the Jenkins Home Ansible Directory and Play directory, we are directly modifying the file that is on this path. But remember that this file is actually being shared with the container. So if we modify this file, we're going to be directly affecting the content inside of the container. So let's hit Enter in here, and now we're going to change this to, for example, Hello World from Ansible and Jenkins.

We're going to save this. And if you go inside of the Jenkins container, let me enter in into the container, Jenkins container, and if we look for the Ansible play, you are going to see that the changes are in here. So, pretty nice. Now if we run this again, we're going to run this playbook once again, let's click on Build. Now let's look for this execution, let's go to the console outputting here.

And as you can see, this should now create a file with a content of Hello World from Ansible and Jenkins, so it finishes successfully. Let's go inside of that remote host. In this case, remember that from the Jenkins container we're connecting to that remote host to create a file. So let's log into the remote host container, and let's look for the Ansible file. And as you can see, it has the content that we modified, which means that our job is actually working like a charm.

So in this video, you've learned how to create your own playbook, how to modify your playbook, and how to make a draft using that playbook. And then executing the playbook using the Jenkins dashboard with only one click, which is pretty cool. So, this is it for this video. I'll see you in the next lesson.

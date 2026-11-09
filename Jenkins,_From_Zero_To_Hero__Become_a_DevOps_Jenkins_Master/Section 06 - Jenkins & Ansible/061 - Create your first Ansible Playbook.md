# Create your first Ansible Playbook

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. In this video, we're going to be creating our first Ansible playbook. A playbook in Ansible is something like an script that defines all of the things that Ansible should do. Let's go to our jenkins directory. In here, let's go to our jenkins-ansible directory. Let's create a new file, which is going to be, for example, play.yml. All of the Ansible playbooks are written in yml, so we need to start learning yml format.

The yml format is exactly the format that we have been using for the docker-compose file. I think that you are already used to this. Let's hit Enter to create our file. Remember that we are creating the files in our host machine, but these files are going to be run inside of the jenkins container, but we're creating these in here because inside of the container, we don't have Beam or any editor. We're creating this outside, and then we're going to copy these files to the container.

Now, we need to start creating our playbook. In Ansible, to create a playbook, normally, we'll start with the hosts' instruction, which means: Which host are we going to use to run this task? In this case, remember that if we take a look to our inventory, we only have one host for now, which is the test1 ansible. If we go back to our file, our playbook. Let's define that host. This is test1, cool.

Then, we need to define the tasks. This is all Ansible structure. If you are not sure about this, you can go to google.com and look for Ansible playbook example, or Ansible playbook syntax, or whatever you want. If you want to read the documentation, go ahead. You're going to find it useful. As you can see, this is how a playbook looks like. We'll start with the hosts. We're not going to use variables in here.

In fact, we're going to be using the tasks. Okay, once we have the tasks, we define what we want to do. In this case, we want to use a shell model, which is a pretty simple model, that is something like your Bash command. Everything that you put in here is like if you are executing that from your terminal. In this case, we're going to do something like Hello Word, and then we're going to redirect that to /tmp/ansible-file, for example.

This is it. We have just created our first playbook. Let's save this file. Remember that this playbook is only going to run an echo Hello Word, and then it's going to redirect the output of that, creating a new file in /tmp/ansible-file inside of the jenkins container. Let's save this. Let's copy this play.yml to the jenkins_home ansible folder that we created. We can access this file from the container.

Let's exec inside of the jenkins container. Let's look for the ansible folder. As you can see, here we have our playbook, which has all the modifications that we did. Remember that now we're outside of the container, but we copied that file to the shirt folder. Now, we can access it from the container. How do we run this file to connect to the remote host, which is the test1 host, and create this file?

Let's type ansible-playbook. Now, we're going to type -i, which means the hosts file that we're going to be using, where we have defined this guy. Then, we're going to say the name of the playbook, which in this case is play.yml. Play.yml, hit Enter, and let's see what happens. As you can see here, Ansible is actually trying to connect to the test1 host using the hosts file that we specified. As you can see, the connection was successful and the task execution was successful as well.

Where do you think that this file is living right now? Is it going to be living in the jenkins container? Or is it going to be living on the remote hosts container? Let's find it out. Let's copy this path. If we cat this inside of the container, nope, we don't have it inside of the container. What we're actually doing in here from Ansible is that we're connecting to the test1 host, and we're running this on the remote host.

This is pretty similar to the SSH plugin that we installed on jenkins. Let's go outside of the container, and let's go inside of the remote-host container, which is the host that we're working with. Let's hit Enter and let's cat this path. As you can see, we have our Hello Word file created. Cool. Let's try once again for you to completely understand it. Let's go to the jenkins container. Let's go to the ansible folder where we have all of our configuration, and let's edit our play.yml.

As you can see, we don't have Beam installed here, so that's why we're editing outside of the container. Let's go outside and let's modify the play.yml. We're going to say Hello Word from Ansible for example. From Ansible, we're going to leave it like this. Let's save this. We're going to copy this to the container. Remember that we have shared a home folder. Let's copied to the ansible folder, but we need to define- When I copy the play file to this directory.

Cool. Enter. If we now exec to the jenkins container, and we'll look for ansible folder. Then, we'll look for the play. Now, you are going to see the modifications in here. Let's run the same command again, which is an Ansible playbook. Hit Enter. You are going to see that Ansible is trying to connect to your remote host using the hosts file that you provided in here. It's going to run the task successfully there.

Let's go outside of the jenkins container, and let's login to the remote-host container. Let's look for the ansible-file. Then, you're going to see that the file actually changed based on our modifications. Cool. What we're doing is that we're connecting from jenkins to that remote-host container. We're running commands through SSH. This is it for this video. You've learned how to create your first playbook.

You are going to be learning more. I'll see you in the next lesson.

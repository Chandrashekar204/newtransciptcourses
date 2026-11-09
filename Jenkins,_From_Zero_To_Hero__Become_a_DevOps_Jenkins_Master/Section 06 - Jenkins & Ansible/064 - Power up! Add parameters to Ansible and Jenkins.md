# Power up! Add parameters to Ansible and Jenkins

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. In this video, we're going to learn how to pass parameters to our Ansible playbook. In the previous video, we were modifying the playbook to make changes, which can be a little bit complicated because you need to modify a lot of files and do a lot of manual things. And if we are using Jenkins, then Jenkins can do that for us. So what we're going to do is to create a parameter and we're going to pass the text to that parameter, and then Ansible is going to get that variable and is going to print that to the standard output.

So in this way, we avoid to modify the playbook directly to change the text. So let's go to our terminal and let's modify the playbook because we need to make a couple of changes for this to work. So remember that if we modify this file, we're actually modifying the file that's inside of the container. So let's hit Enter in here. And we want to delete this shell line and we want to use now a debug line.

A debug line or a debug model allows us to print something to the standard output. This is something like the echo command for Linux, this is why it's called debug. So we can print a message in here and we can then print a variable in here, or text plus a variable. So in Ansible, variables are defined like this, using these curly braces. So for example, we want here to define whatever, for example a message that's a variable, and we're going to send this from Jenkins.

So let's save this playbook, or let's just keep this open for now and let's go to our Jenkins configuration. We're going to click on the Configure button because we want to add a new parameter. So remember, the parameters are under the General section. So let's click on This project is parameterized and let's click on the Add Parameter button, and we're going to create a sample string parameter in here.

So we can name it as we want, let's say, for example, ANSIBLE_MSG. And then we're going to give it a default value, which could be Hello World. So this is cool, now we need to pass this parameter to Ansible. How do we do this? Well, we go to the Build section, to our playbook configuration, and we're going to click on the Advanced. In the Advanced section, we're going to find this Extra Variables button.

So we're going to click on Add Extra Variable in here and now we are going to give a key, and the key means that variable that Ansible is expecting. So in this case, Ansible is expecting the message variable. So let's go ahead and copy this in here. And now we need to refine the value of the message, but we want this value to be dynamic. So this value, it's going to be the value of this parameter.

So this is exactly the same thing that we did before on the Bash parameters. So let's copy this parameter in here, and we're going to say that the value for this, it's going to be the value of the Jenkins parameter. So whatever we're putting here for the Jenkins parameter, Ansible is going to take this and is going to pass that as a value, and then it's going to print this with this line. Pretty cool.

So now we can click on the Save button, and we're going to save this playbook as well. So let me save this. Cool. And remember that if you go inside of the Jenkins container, all of the modifications are already in place because we were modifying directly the shared file. So let's go outside of this container. Remember that we're no longer creating files, but now we're just printing to the standard output.

So if we go here and we click on Build with Parameters, you are going to see that now we're able to modify the text of our playbook, pass in the values of parameters. So for example, let's say that I want to say, "Hello World. This is a cool integration with Ansible and Jenkins." So if you hit on the Build button, let's click on the Build number, let's click on Console Output, and as you can see here, Ansible is doing what we were expecting, which is pretty nice.

So Ansible is taking the value from the parameter and is passing that to our playbook using an extra variable and we have been able to print this to the standard output. So let's use another string here, for example, Bye World, just to say something instead of Hello World. We click on the Build button, let me refresh this in here. And if we take collect to the Console Output, this is actually connecting to the remote host in this step.

And then it's printing the variable in here that we are passing as a parameter. So this is actually pretty cool. If we click on the Configure button, let's recap what we just did. We created a sample parameter in here. And then for Ansible to be able to print that, we need to add an extra variable, which is something like a Bash parameter in Ansible, and then we say the key that Ansible is expecting and we specify the value for that key.

And remember that the value should be dynamic, which means that the value should be the value of the Jenkins parameters. So in here, whatever the user passes, we're passing that to Ansible, which is pretty cool. So let's click on Save this. This is it for this video. You've learned how to create Jenkins parameters, how to pass those parameters to your Ansible playbook, and how to print that to the standard output only with one click.

So I'll see you in the next lesson.

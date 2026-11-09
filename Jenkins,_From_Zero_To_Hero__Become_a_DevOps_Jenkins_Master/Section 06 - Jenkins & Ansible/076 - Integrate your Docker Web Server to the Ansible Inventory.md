# Integrate your Docker Web Server to the Ansible Inventory

*Section: Jenkins & Ansible*

Instructor: Hello, and welcome back. In this video, we're going to integrate our Docker web container, that we created, with Ansible. So, to do that, remember that we need to modify our inventory. And if you remember, we were creating our things on the shared folder. And if you remember, that shared folder lives at jenkins_home/ansible, and then we have all of the files that we were creating there.

So, here is our hosts file. And remember that if we modify that file in this location, then it's going to be changed in the host and in the container at the same time. So let's go ahead and modify this. We're going to modify the host file. And now, we're going to add our web container in here. So let's call it like web1. You know that you can give the name that you want in here. And we're going to copy this all.

Because remember that our web container starts from that remote host image. So it's pretty similar. Now, we're going to change a little bit the information in here. So for example, the Ansible host is the web container because remember that in the Docker file we specify the service as web. So if we go out of here and we take a look to the Docker composed file, remember that this is the name that we are using to reach our web container.

So, this is it, web. And then the Ansible user, it's going to be the remote user because remember that this service is actually using the same image than this. So the information is exactly the same, but the host is the only one different. So the Ansible private key is exactly the same key because remember that the image is the same. So, with this, we already integrated our Docker web container to the Ansible inventory.

So let's go ahead and save this file. And let me go inside of the Jenkins container to test this out. So cool. The first thing that we're going to test is that the connection from Jenkins to the web service is working. So if we do ssh web, you're going to see a prompt that is going to ask you if you are sure to connect to this host. So you type yes. And then it's going to ask you for the password, but we don't want to give the password now.

So hit Control+C. And then you are out of this. So the connection from Jenkins to the web container is working like a charm. So now, let's test it using Ansible. Let's go to our Ansible folder inside of the Jenkins container. And let's take a look to our hosts file. And as you can see, the file is modified. And if we now do ansible -m ping -i host, and we pass the web1 host, and we hit Enter, what do you think that's going to happen?

And, as suspected, you can see that the web1 is actually returning a success message, which means that now we can reach this web1 host from Ansible. Pretty cool. So let's make sure that we can still reach the test1 host, which is our remote host container. Let's hit Enter. And as you can see, it's still reachable. So cool. In Ansible, we have another thing, which is ping all, and that's going to ping all of your hosts.

So in this case, on our host file, we have only two hosts. That's why it's only showing two results. But cool. Now your web1 is working. And now you can reach it from Ansible and from Jenkins, which is a cool thing. So this is it for this video. I'll see you in the next lesson.

# Integrate your Docker SSH server with Jenkins

*Section: Jenkins & Docker*

Ricardo: Hello and welcome back. Okay, here we are again on the Jenkins dashboard. And now we're going to configure the authentication over SSH to our remote host. Remember that in previous lessons, we created a new service which is an SSH service. And remember, that if we go to Docker exec -ti jenkins and bash and we try to SSH using that remote_user@remote_host, we're going to have a connection and if we type the password, then we can log into that machine.

Cool. So now we're going to configure this and Jenkins so we have direct connection to the host through SSH. Please remember that all the connections are going to happen inside of the container. So when you configure the host, look at this. If we type this, we have an answer. But if we go out of the container, let me go out, and I do this, then I have an error as you can see. Because if you remember, in our Docker Compose file we define that remote host DNS as this one.

So Jenkins can see that remote host using this DNS because they both belong to the same network, but outside of the container in your machine, you can't see that name because your host is not part of that network directly. So cool. The first thing that we're going to do is that we're going to go to the Jenkins dashboard, we're going to click and manage Jenkins. Once here, click on Configure the System.

And once you've clicked the button, you are going to see this screen. We're going to look for this SSH remote hosts and we're going to click in the Add bottom. So once we click here, it's going to ask for the Hostname that we want to connect. So in this case, we want to connect to that remote_host. Remember that Jenkins resolves this name as a remote host. If I go into the container exec, and if I try a ping for this host, you see that this is actually answering.

So this becomes our host name. So we're saying we want to connect to that remote host on port 22 because by default SSH runs on that port. And here we have a port, which is the credentials port. So, so far we don't have any credentials. So let's click on Add a new credential here. Okay, it looks like we can click on this. So let's click on Credentials here. Let's leave this for a second. And we're going to click on the Jenkins and then Global credentials.

And here we're going to click the button Add Credentials. Cool. So here we have a lot of kinds, a lot of types of credentials. In this case, we want a username and a private key. So cool. Remember that if we take a look at our Dockerfile, which is on the centos7 folder Dockerfile, we created a user called remote_user in the remote host. So to connect to that remote host, we need to use this user remote_user.

Cool. So let's use this user here. And now we're going to enter a private key. Remember the private key? The private key is also under the centos7 folder and it's the remote-key. So we're going to cat centos7, that remote-key. We're going to copy all the content. Remember that we created this key using the SSH-keyscan command. So we're going to copy this and now we're going to paste this, as you can see.

Cool. So let's click on OK. And as you can see, now we have key for that remote_user. We go again to Jenkins, Manage Jenkins, Configure the System, and now we go again to the SSH sites. Click on Add. Remember that the host name is that remote_host. So let me look at the Docker Compose file, remote_host. Let's paste this here, port 22. And now if we click on the Credentials list we're going to see the remote_user credentials that we created before.

So let's click on this. And now the only one thing that we need to do is to click on Check the connection. And as you can see, the connection is successful. So what we have just done is to configure that remote_host which is the Hostname that we want to connect. This is the port that we're going to use and the credentials that actually has the user and the private key needed for the connection. So once we check the connection and it's successful, what we're going to do, so we're going to Save and we are done.

So this is it for this video. See you in the next lesson.

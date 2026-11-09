# Create a Docker Container for Jenkins

*Section: Introduction & Installation*

Instructor: Hello and welcome back. In this video, we're gonna start our service, our container using Docker to spin up the Jenkins service. So, so far we already created the docker composed file and we created a directory here where we're going to save all the files. So remember that we define a volume here and we're saying, okay, docker, place everything that is within the container in this location please save this in this folder.

And this folder means this folder. So if we take a look on the folder itself we see that we don't have any data yet and that's normal because we haven't created anything. So please make sure that this folder has proper permissions so jenkins can write. And what do I mean by proper permissions? Make sure that the user 1000 can write to this folder. And what's the user 1000? So in Linux we have IDs, and as you can see, this user the jenkins user has the user ID of 1000.

So we're gonna do a sudo change owner 1000 column 1000 into this folder. So jenkins home, we're gonna do it recursively. So, okay, when you do this you will do an ll and you are going to see that the user the owner is jenkins, and the group is jenkins. This is because the container uses the ID 1000 to write data. And if you have another ID you are going to probably have an error. So please make sure that you write this command before spinning up your server.

So, okay, we already gave it permissions. We only need to do this once. I mean this time and no more. And once we gave permissions, we're going to spin up this server doing a docker compose up dash d. And what is going to happen here is the docker is going to create the service reading the docker composed definition in here. And if we type docker ps, we're going to see the server running here. So this is a docker container.

We have a SPAN app, our server using docker. You can list your containers using docker ps. So as you can see, this is actually working like a charm. Cool. I will type docker logs dash f and this is going to show me the logs for a certain container. Remember that in our definition of the docker composed file we said that the container name is jenkins. So we do a docker logs dash f jenkins, we hit enter.

And as you can see here, this is one weird hash. We're going to use this later. So for now, what we are going to do is that we're going to hit the IP address of our machine. Do you remember the IP address? So we're gonna grab this IP. We can pick the IP from PuTTY, remember? We can click here, load, and then we will have the IP. So we're going to copy this IP and we're going to paste it into our browser.

So we paste this and we're going to have an error. But if we do a column 8080, and then we hit enter again we are going to be presented with a screen that tells us, Hey, I am Jenkins. Whoa. Finally, we have Jenkins installed and Jenkins wants to make sure that we are the owners. So we need to introduce here a password but what's the password? Well, the password is pretty simple. You go to PuTTY here, you do a docker logs dash f and you will see the password in here.

So this is the password, and we're gonna copy this. Remember to copy and put it, you just do a double click on the thing that you wanna copy, and then you paste it normally here. You paste it and then you click and continue. Pretty simple. So now as you can see here we're presented with a screen that says Customize Jenkins. So what do we do here? I will suggest you to click on the bottom that says Install suggested plugins.

We're gonna click on this and Jenkins we're gonna see this later. Jenkins has a lot of plugins and a plugin is nothing else bad, like a tool an extension for something. So Jenkins, it's quite powerful but you can install a plugin. And a plugin is going to give you additional functionalities for Jenkins. So in this case, we're going to install the suggested plugins by Jenkins because for sure we're going to need it in the future.

So this is going to take a while because it needs to connect to the Internet and then download the files and install them into Jenkins. I will pause the video and I will come back when it has finished. Great. So the download already finished and now we have a screen here that tells us to create a user. And as you can see here, it says, okay, please create the first admin user. So we're gonna call it admin, or you can call it whatever you want.

We're gonna give it a password. Please give a strong password. I will give it 1, 2, 3, 4. I'm actually giving 1, 2, 3, 4 to everything. (Instructor laughs) Okay, so we're gonna give the full name. Let's say that this is gonna be Jenkins Admin. And let's say that the email of this guy is like jenkins@, I dunno, gmail.com. Just to say something. Okay. Then we click on Save and Continue. We click on Never here and here this is going to ask for the URL.

So for now, we're just gonna leave it like this. We click Save and Finish, and then we are done. Finally, we click on Start using Jenkins. And here we have the screen that allows us to log out and log in. So if we click on logout here then we put the credentials that we created, admin and 1, 2, 3, 4 as a password. We can click on Keep me signed in, let's click it and then let's hit the Sign In button.

Cool. So here we are in the Jenkins dashboard and then we're going to start having a lot of fun with all of these features, tools, and icons that you can see here. So don't miss any video and see you in the next lesson.

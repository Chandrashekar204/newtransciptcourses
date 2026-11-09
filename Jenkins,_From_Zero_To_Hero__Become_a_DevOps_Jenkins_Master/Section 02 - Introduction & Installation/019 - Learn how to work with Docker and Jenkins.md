# Learn how to work with Docker and Jenkins

*Section: Introduction & Installation*

Instructor: Okay, cool. So now that we have configured everything and that we're using a better interface, we are going to start learning how to use Jenkins. Remember that if you do an ls, you are going to see this folder, which is Jenkins data. We created that folder before. So just go ahead and change directory to that folder. And if you hit ls, you're going to see the Docker compose file. You are going to use this Docker compose file a lot because remember that this file contains the definitions for the service itself.

So if we go to the browser now and we reload, we have the service up and running. But what happens if we want to stop the service or if we want to reboot our machine? Then to stop the service, we need to do a docker-compose stop and this is going to stop the service itself. So if we reload here, the service is no longer live. And if we do a docker ps, you see that there is no container running. Therefore, you will have a network here.

So if you want to start your service, you do a docker-compose start, and then you do a docker ps and you see that the container is actually up and running. So if I reload here, it takes some seconds for Jenkins to completely boot up. So that's how you work with this. Maybe if you wanna reload your service, you are going to do docker-compose, maybe restart Jenkins, which is the name of the service that you wanna restart.

This is going to stop it, and then it's going to start it back. And what happens if you want to completely delete your entire service? So, okay, you are going to do a docker-compose down. And this down is going to delete everything related to the service, but it's not going to delete what we save on the volumes. Do you remember the volumes? If we take a look on the Docker Compose file, we'll see that in the current pad we have a volume, which is this one.

And if we do an ls here, we're going to see all of the files that belong to Jenkins. So if we recreated this service, this is going to look for the files in this folder, and then it's going to map those files into the container itself. So let's do this, docker-compose up -d creates the service or recreates the services. So if we do a docker ps, the service is up and running. So let's hit the browser and see what happens.

So as you can see, Jenkins is just getting ready to work and we should have all the configuration that we have already done, like installing plugins or configuring the admin password and all of that stuff. So this video is for those guys who don't know how to use Docker, or for people who have never used Docker before and don't know how to use Docker Compose. So that's pretty simple to use the Docker Compose app to create a service or recreate it, stop for stopping it, start for starting it and down for deleting it.

So this is pretty cool. Our Jenkins service is already ready to accept connections, so we can start playing around with this. So see you in the next lesson.

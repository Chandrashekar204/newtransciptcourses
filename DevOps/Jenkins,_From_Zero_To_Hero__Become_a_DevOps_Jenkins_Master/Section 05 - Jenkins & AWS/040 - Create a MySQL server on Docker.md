# Create a MySQL server on Docker

*Section: Jenkins & AWS*

-: Hello and welcome back. In this video we're going to learn how to create a MySQL container using Docker. Remember that we have created all of our services using Docker. We created a Jenkins container and a remote house container. So let's go ahead and create a MySQL container. So the first thing that we need to do is that we need to go to the Jenkins data folder and we need to modify the docker compose file.

So we're going to add a new service. Remember that you can name services as you want. In this case, I'm just gonna name it as db host. And remember that we're going to be using this name to reach this host from this remote host and from this jenkins. It means that if I go inside of this container or inside of this container and then I try to ping this host I will have an announcer. So let's keep it like this.

And now let's add a container name for this service which is going to be db led at an image which is going to be the mysql 5.7 image. Remember that in docker images are like a snapshot and if you have the image for the service that you want then you have all of the configuration for that service. If you are not sure about how to find this image you can simply head to google.com and then look for mysql docker.

And you're going to end up looking at this page. And in here you're going to see that the name of the image is mysql as you can read here. And these are the supported tags. So a tag is like a version. So in this case we're going to use the mysql image colon the tag, which is 5.7. Cool. And now in order to give our database a password we need to read a little bit of documentation and we need to look for this.

As you can see here in Docker, for the mysql image we need to provide an environment variable which is called like this. So let's go ahead and copy this password, this variable, I mean. And now we're going to say, hey docker, compose. I'm gonna pass you an environment variable using the environment instruction. And this environment is going to be the the variable that I just copy. And then I will give you the password.

And guess the password, 1234. Okay, cool. So after this we're going to create a volume. So again, as in Jenkins we're going to create a volume to persist the data. It means if we delete the container then the important data it's going to be saved. So let's go ahead and create a db data folder in here. Let's put a column exactly the same thing as Jenkins. And here we're going to pass the container pad where the mysql data lives.

So that lives in var lib mysql. You can read the docker documentation to find it out. So if I do like var lib mysql then you're going to find examples for this. And as you can see, it means the host directory and then it means the container directory. So we're passing here the container directory and this is going to be a local folder that will be created. So now the last thing that we need to do, guess what it is?

We need to define the networks. The networks are pretty important because without the networks, containers can't reach each other. So let's go ahead and join this container to the net network like the remote host and like the Jenkins container. Let's save this. And now in order to recreate this new service if you hit docker ps then you're going to see only two services. So in order to create the mysql container you need to do docker compose up dash d and that is going to create the service.

So you define this image in your docker compose file, and now you are telling Docker to create this service using that image but that image doesn't exist on your machine. So Docker is going to be downloading this image for you and then you're going to have this image completely. Cool. If you do a docker images then you have your image downloaded here. Pretty nice. Now if you do a docker ps you are going to see your service up and running here.

And if you do on that list you're going to see that the folder that we define in the volume section is actually created in here. Pretty cool. So how do you know when mysql is ready? Because it takes some seconds for this container to be ready. So let's go to docker logs dash f and let's give the name of the container, which is db. If we do this, then you're going to see all of the logs for this specific container.

And in here, as you can see, you should expect for this line, MySQL is ready for connection. Once this line appears, it means that your service is up and running. So let's go ahead and check that this is correct. Let's log in into our newly created container using docker exec dash ti db bash. Remember that db stands for the container name. So hit enter and now we're inside of the MySQL container. So let's try to log in using the root user and the password that we provided in the docker compose file as an environment variable which is 1, 2, 3, 4, hit enter, and then you are connected to your database in a container.

Cool. So if you type something like show databases then you will have all of the information. So this is pretty nice. Let's get out of the container. And now you can see you have your three services up and running using Docker. So this is it for this video. I'll see you in the next lesson.

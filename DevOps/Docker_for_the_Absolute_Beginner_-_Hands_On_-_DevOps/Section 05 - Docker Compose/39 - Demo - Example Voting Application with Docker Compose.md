# Demo - Example Voting Application with Docker Compose

*Section: Docker Compose*

1 Right, we'll now see how to run the same application stack, 2 but on Docker Compose. So in the previous demo, 3 we created a network, we ran the services, we built the application image, 4 we were able to deploy the stack and access the application. 5 Now, we're going to do the same, but we're going to do it with Docker Compose. 6 So if I were to go and look at the images using the docker images command, 7 I see that I have the five images.

8 And if I run the docker ps command, I see there are no running containers. 9 The images are there, but the containers are not there. 10 So what we'll do is we'll create a Docker Compose file, 11 I will call it docker-compose.yaml, 12 but there's already another file, I'll just name it simple.yaml. 13 And note that there are a couple of Docker Compose files in the repo already, 14 those are samples, but we're just going to write one for ourselves.

15 Okay, so I'm also going to have a look at the existing images that we created for reference. 16 So I'm going to run the docker images command, you see that I have these images. 17 Alright, so in our Docker Compose file, I'm going to first define services. 18 So this is the new format. And then I want to list all the services. 19 These are my services. So I have the vote service, we have to add a line for vote.

20 And then I have the result service. And then I have the worker service, 21 I have the Redis service, then I have the DB service. 22 So these are the five different services that I have. 23 And here are the images. So for each of them, 24 I'm now going to add the image, I'm going to say image. 25 Image for the voting app is also called as vote. 26 And image for the result app is called as result.

27 And the image for worker is called worker. 28 And the image for Redis. 29 If you come down here, you'll see that it's Redis Alpine. 30 Copy Redis Alpine. 31 And the image for the database is Postgres 15 Alpine, so I'm going to copy that. 32 Okay, so the images are ready. 33 And now the one thing that's left is ports. 34 So for the vote and result app, we need to do port mapping. 35 So I'm going to specify ports here.

36 And ports is an array of port maps. 37 And the first entry is 8080. 38 It's going to port 80. 39 And for result app, I'm going to add a ports section. 40 And I have the port mapping is 8081. 41 But the application inside the container is exposing it on 80. 42 So 8080 for vote and 8081 for result. 43 Now the only other thing that's pending, so if you go back and look at our 44 the manual command, command that we ran, 45 we get to see all of the details here mapped to the commands here.

46 So we have the names, we have the images, image names, 47 and then we have the port numbers. 48 So these match exactly as here. 49 And the other two things are, the other two containers are Redis and database. 50 And Redis does not have any port. 51 So it's just a direct run, but database has environment variables. 52 So this is one thing that's pending that we haven't configured. 53 So we're going to do that next.

54 I'm going to go to DB, and I'm going to add environment. 55 And this is a dictionary. 56 So I'm going to copy the Postgres user from here, paste that. 57 And you can go back here, the value of your user is Postgres. 58 Similarly, I'm going to copy password. 59 And I'm going to copy the password which is also Postgres. 60 Okay, and the last part is the volume. 61 So we have the DB data volume that needs to be mapped.

62 So for that, what we're going to do is we're going to first create a volume. 63 And we do that by adding a top-level property that's at the same level as services. 64 And we're going to call that volumes. 65 And this is a dictionary, so I'm just going to say DB data. 66 And I'll just specify the name of the volume. 67 Now, under the DB image, next to image and environment, 68 I'm going to specify volumes.

69 And this is an array. 70 And I'll use the same mapping that I have here, which is DB data, 71 to map to Wordlib PostgreSQL data inside the container. So that's it. 72 I have services, I have a list of services, I have images, ports defined, 73 and I have environment, variables, and volumes defined for the database service. 74 Alright, so next we're going to bring up the stack using the docker-compose up command.

75 So I'm going to run a docker-compose-f and specify the file name, 76 which is docker-compose-simple.yaml. 77 I'm going to do an up. 78 And what it's going to do is, if you scroll all the way to the up, 79 you see that it first creates a network. 80 Even though we haven't specified a network in the file, it's created a network automatically 81 with the name of the application, which is the name of this folder that I'm in.

82 And then it's created each container by prefixing the name of this folder. 83 And then the name of the service. 84 And it's created all the services. 85 And you can see the logs from different service 86 with a prefix of that service name and a different unique color to it. 87 So this is the database coming up. 88 Then you have the Redis logs from the Redis service. 89 Then you have the vote result and worker applications. So that's done.

90 Now if I go to localhost 8080 and click on a vote, 91 I can see that it's coming up. 92 And you can see all the logs associated with that particular single action 93 and how it traverses through the different services right here. 94 So it's a pretty good trace of how the request is going through different services. 95 Okay, I'm going to hit Ctrl C. 96 And I'm going to just sit down so that it terminates and removes the entire stack.

97 So now if I do a dockerfs, I see that there is nothing running. 98 All right, next, we're going to do the same thing but slightly differently. 99 So if I do a docker images, I have all the images. 100 Now I'm going to do a docker RMI and delete the result app, the vote and worker. 101 And if I list the images now, I see that only the Postgres and Redis images are there. 102 Now I don't have to build the images manually to then run Docker Compose.

103 What I could do is I could change the image specifications from each service from image to build. 104 And then I specify the directory, which is the vote directory for the vote application. 105 Similarly, I'm going to change this build to the result directory for the result application. 106 Then I'm going to change this to worker for the worker app. 107 And now I'm going to do a docker compose up.

108 Specify the file name first, so docker compose simple. 109 Then I'm going to do up. 110 And this time what it's going to do is it's actually going to build those images first. 111 So it's going ahead and ran the build internally and build images. 112 And now it's brought up the entire application stack. 113 So if I go back and refresh the page, you can see that it's working.

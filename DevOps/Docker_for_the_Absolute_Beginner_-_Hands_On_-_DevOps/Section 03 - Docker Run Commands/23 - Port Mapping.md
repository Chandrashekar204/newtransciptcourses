# Port Mapping

*Section: Docker Run Commands*

1 Now, let's look at port mapping or port publishing on containers. 2 Let's go back to the example where we run a simple web application 3 in a Docker container on my Docker host. 4 Remember, the underlying host where Docker is installed 5 is called the Docker host or Docker engine. 6 When we run the containerized web application, 7 it runs and we can see that the server is running. 8 But how does a user actually access my application?

9 My application is listening on port 5000, 10 so I could access it on port 5000. 11 But what IP do I use to reach it from a web browser? 12 There are two options. One is to use the IP of the Docker container. 13 Every Docker container gets an IP assigned by default like the one here. 14 But remember, this is an internal IP 15 and is only accessible within the Docker host. 16 So if you open a browser from within the Docker host, 17 you can go to that container IP on port 5000.

18 But since this is an internal IP, 19 users outside the Docker host cannot reach it. 20 For that, we use the IP of the Docker host, the one you see here. 21 But for that to work, you must have mapped a port 22 inside the Docker container to a free port on the Docker host. 23 For example, if I want users to reach my application 24 through port 80 on my Docker host, 25 I map port 80 of the host to port 5000 on the container 26 using the P parameter.

27 And so the user can now reach my application 28 by going to that host IP on port 80. 29 And all traffic on port 80 of my Docker host 30 gets routed to port 5000 inside the container. 31 This way, you can run multiple instances of your application 32 and map them to different ports on the Docker host, 33 or instances of different applications on different ports. 34 For example, you could run an instance of MySQL 35 listening on its default port 3306, 36 and another instance of MySQL on port 8306.

37 So you can run as many applications like this 38 and map them to as many ports as you want. 39 And of course, you cannot map to the same port 40 on the Docker host more than once. 41 We'll discuss more about port mapping 42 and networking of containers in the network lesson later on.

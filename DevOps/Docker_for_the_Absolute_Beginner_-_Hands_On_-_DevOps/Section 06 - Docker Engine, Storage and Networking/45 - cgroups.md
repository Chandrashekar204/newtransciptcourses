# cgroups

*Section: Docker Engine, Storage and Networking*

1 So we've seen that the underlying Docker host and the containers share the same system resources 2 like CPU and memory. 3 So how much of those resources is dedicated to the host versus the containers? 4 And how does Docker manage and share them between containers? 5 Well, by default, there is no restriction, a container can end up using all the resources on the underlying host. 6 But there is a way to limit how much CPU or memory a container can use.

7 Docker uses C groups or control groups to restrict the amount of hardware resources allocated to each container. 8 You do this by passing the dash dash CPUs option to the Docker run command. 9 A value of 4.5 makes sure the container doesn't take up more than 50% of the host CPU at any given time. 10 The same goes for memory set the dash dash memory flag to 100 megabytes and the container is limited 11 to 100 megabytes.

12 That's it for now on Docker engine. 13 Next, we talk about Docker storage and file systems.

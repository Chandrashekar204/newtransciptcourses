# Namespaces

*Section: Docker Engine, Storage and Networking*

1 Now, let's try and understand how exactly applications are containerized in Docker. 2 How does it work under the hood? 3 Well, Docker uses namespaces to isolate the workspace. 4 Process IDs, network, inter-process communication, 5 mounts and Unix time-sharing systems 6 are each created in their own namespace. 7 And that's what gives each container 8 the feeling of being its own little system, 9 even though it's all sharing the same host kernel underneath.

10 Let's take a look at one of these namespace techniques, 11 process ID namespaces. 12 Whenever a Linux system boots up, 13 it starts with just one process with a PID of one. 14 That's the root process, 15 and it kicks off all the other processes in the system. 16 By the time the system is fully up, 17 you have a handful of processes running, 18 which you can see by running the ps command. 19 Process IDs are unique.

20 Two processes cannot have the same PID. 21 Now, if we create a container, 22 which is basically like a child system 23 inside the current system, 24 the child needs to think it's an independent system 25 on its own with its own process tree starting from PID one. 26 But we know there's no hard isolation 27 between the container and the underlying host. 28 The processes running inside the container 29 are in fact processes running on the host.

30 And two processes can't both have PID one on the same host. 31 This is where namespaces come into play. 32 With process ID namespaces, 33 each process can have multiple PIDs associated with it. 34 So when processes start inside the container, 35 they're really just another set of processes 36 on the base Linux system, 37 and they get the next available PID, say five and six. 38 But they also get another PID 39 starting from one inside the container's namespace, 40 which is only visible inside the container.

41 So the container thinks it has its own root process tree, 42 and it acts like an independent system. 43 So how does that show up on a real system? 44 Let's say I run an Nginx server as a container. 45 We know the Nginx container runs an Nginx service. 46 If I list the processes inside the container, 47 I'll see Nginx running with a PID of one. 48 That's its PID inside the container's namespace.

49 But if I list the processes on the Docker host, 50 I'll see the same Nginx service running 51 just with a different PID. 52 That tells us all these processes 53 are really running on the same host, 54 but separated into their own containers using namespaces.

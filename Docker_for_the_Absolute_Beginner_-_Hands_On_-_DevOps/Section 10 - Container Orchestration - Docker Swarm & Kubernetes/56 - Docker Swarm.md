# Docker Swarm

*Section: Container Orchestration - Docker Swarm & Kubernetes*

1 We will now get a quick introduction to Docker Swarm. 2 Docker Swarm has a lot of concepts to cover 3 and really requires its own course, 4 but we will try to take a quick look 5 at some of the basic details 6 so you can get a brief idea of what it is. 7 With Docker Swarm, 8 you can combine multiple Docker machines together 9 into a single cluster. 10 Docker Swarm will take care of distributing your services 11 or your application instances into separate hosts 12 for high availability and for load balancing 13 across different systems and hardware.

14 To set up a Docker Swarm, 15 you must first have multiple hosts 16 with Docker installed on them. 17 Then you must designate one host to be the manager 18 or the master or the swarm manager, as it is called, 19 and the others as workers. 20 Once you're done with that, 21 run the swarm init command on the swarm manager, 22 and that will initialize the swarm manager. 23 The output will also provide the command 24 to be run on the workers.

25 Copy that command and run it on the worker nodes 26 to join them to the manager. 27 After joining the swarm, 28 the workers are also referred to as nodes, 29 and you're now ready to create services 30 and deploy them on the swarm cluster. 31 Once your hosts are ready, 32 initialize the swarm on the manager node. 33 Docker swarm init with the advertised adder flag 34 set to 192.168.1.12. 35 The output looks something like this.

36 Copy the join command and run it on each worker node 37 to add it to the swarm. 38 So let's get into some more details. 39 As you already know, to run an instance of my web server, 40 I run the docker run command 41 and specify the name of the image I wish to run. 42 This creates a new container instance of my application 43 and serves my web server. 44 Now that we have a swarm cluster, 45 how do I use it to run multiple instances of my web server?

46 One way to do this would be to run the docker run command 47 on each worker node. 48 But that's not ideal. 49 I might have to log into each node and run this command, 50 and there could be hundreds of nodes. 51 I would have to set up load balancing myself, 52 monitor the state of each instance myself. 53 And if instances were to fail, 54 I would have to restart them myself. 55 So that's going to be an impossible task.

56 That is where docker swarm orchestration comes in. 57 The docker swarm orchestrator does all of this for us. 58 The key component of swarm orchestration 59 is the docker service. 60 Docker services are one or more instances 61 of a single application or service 62 that run across the nodes in the swarm cluster. 63 For example, in this case, 64 I could create a docker service 65 to run multiple instances of my web server application 66 across worker nodes in my swarm cluster.

67 For this, I run the docker service, 68 create command on the manager node 69 and specify my image name there, 70 which is my web server in this case, 71 and use the replicas option 72 to specify the number of instances 73 I would like to run across the cluster. 74 Since I specified three replicas, 75 I get three instances of my web server 76 distributed across the different worker nodes. 77 Remember, the docker service command 78 must be run on the manager node 79 and not on the worker node.

80 The docker service create command 81 is similar to docker run in terms of the options passed, 82 such as dash E for environment variables, 83 dash P for publishing ports, 84 and the network flag to attach the container to a network. 85 Well, that's a high-level introduction to docker swarm. 86 There's a lot more to know, 87 configuring multiple managers, 88 overlay networks, and so on. 89 As I mentioned, it really requires its own separate course.

90 Next, we will look at Kubernetes at a high level.

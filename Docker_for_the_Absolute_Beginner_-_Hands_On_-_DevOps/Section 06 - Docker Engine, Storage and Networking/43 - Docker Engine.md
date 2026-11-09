# Docker Engine

*Section: Docker Engine, Storage and Networking*

1 In this lecture, we will take a deeper look at Docker's architecture, 2 how it actually runs applications in 3 isolated containers and how it works under the hood. 4 Docker Engine, as we have learned before, 5 is simply a host with Docker installed on it. 6 When you install Docker on a Linux host, 7 you're actually installing three different components, 8 the Docker daemon, the REST API server, and the Docker CLI.

9 The Docker daemon is a background process that manages 10 Docker objects such as images, 11 containers, volumes, and networks. 12 The Docker REST API server is 13 the API interface that programs can 14 use to talk to the daemon and send instructions, 15 so you could even build your own tools on top of it. 16 The Docker CLI is the command line interface we've 17 been using all along to run containers, 18 stop them, destroy images, and so on.

19 The CLI talks to the daemon through the REST API. 20 Now, something to note here is that 21 the Docker CLI need not be on the same host as the daemon. 22 It could be on another system like 23 your laptop and still work with a remote Docker Engine. 24 You just use the "-h'' option on the Docker command and 25 specify the remote host's address and port. 26 For example, to run 27 an Nginx container on a remote Docker host, 28 you'd run something like this.

29 Docker with the "-h'' flag set to 10.123.2.1 port 2376, 30 with the TLS verify flag running Nginx. 31 One important update here. 32 As of Docker Engine V27.0, 33 the daemon refuses to listen on 34 plain TCP without an explicit unsafe override. 35 The standard remote access flow now uses TLS on 36 port 2376 with the TLS verify flag and signed certs. 37 If you ever come across an older example using port 2375 with 38 no TLS, treat that as a security red flag.

39 Port 2375 is the unencrypted, 40 unauthenticated Docker API and anyone who 41 can reach it has full root on the Docker host. 42 So stick with 2376 plus TLS, 43 or better yet, just use SSH, 44 Docker with the "-h'' flag set to 45 ssh colon slash slash user at host running Nginx. 46 So far, we've described Docker Engine as three pieces, 47 the CLI, the REST API, 48 and the daemon, but the daemon 49 doesn't actually run containers itself.

50 When you say Docker run Nginx, 51 the daemon hands the request to 52 a second program called container D, 53 and container D hands the real work to 54 a third program called run C. 55 Three handoffs before a container starts. 56 Why all the layers? 57 Because each one has a different job. 58 The daemon handles everything. 59 Docker specific, images, networks, 60 volumes, Docker Hub authentication, the REST API.

61 Container D is a general purpose container runtime. 62 It pulls images from registries, 63 manages the container lifecycle, 64 and supervises running containers. 65 But it knows nothing about Docker as a brand. 66 Run C is the lowest level. 67 Given an image and a config, 68 it calls the kernel to set up 69 the namespaces and C groups and starts your process. 70 Run C implements the Open Container Initiative, 71 or OCI, runtime specification, 72 which is the standard contract for what it 73 means to run a container on Linux.

74 This split is why Kubernetes is dropping 75 Docker a few years ago, 76 didn't actually break anything. 77 Kubernetes was never using Docker D, 78 it was talking directly to container D underneath. 79 Same runtime, one less middleman. 80 Container D is now the de facto standard runtime for 81 the whole container ecosystem, Docker, Kubernetes, 82 and most managed container platforms all sit on top of it.

83 For day-to-day Docker use, 84 you'll never type container D or run C. 85 But knowing the layers helps when you see them in process lists, 86 in logs, or in conversations about Kubernetes, 87 and it explains why some newer features like 88 the container D image store we'll see in 89 the next lesson show up the way they do.

# Images and Registries

*Section: Introduction*

1 There are a lot of containerized versions of applications readily available today. 2 Most organizations have their products containerized and available 3 in public Docker repository called Docker Hub. 4 Docker Hub is the most popular registry, but there are many others too. 5 So you have GitHub Container Registry, Google Artifact Registry, AWS ECR, 6 and Azure Container Registry. 7 You can find images of most common operating systems, databases, and other services and tools there.

8 Once you identify the images that you need and you install Docker on your host, 9 bringing up an application is as easy as running a docker run command with the name of the image. 10 So running a docker run ansible command will run an instance of ansible on the Docker host. 11 Similarly, you can run an instance of MongoDB, Redis, and Node.js using the docker run command. 12 If you need to run multiple instances of the web service, 13 you simply add as many instances as you need 14 and configure a load balancer of some kind in the front.

15 In case of one of the instances where to fail, 16 simply destroy that instance and launch a new one. 17 There are other solutions available for handling such cases that we will look at later in this course. 18 For now, don't focus too much on the commands. 19 We'll get to that in a bit. 20 So we've been talking about images and containers. 21 Let's understand the difference between the two. 22 An image is a package or a template, 23 just like a VM template that you might have worked with in the virtualization world.

24 It is used to create one or more containers. 25 Containers are running instances of images 26 that are isolated and have their own environments and set of processes. 27 As we have seen before, a lot of products have been dockerized already. 28 In case you cannot find what you're looking for, 29 you could create your own image and push it to a Docker Hub repository, 30 making it available for the public.

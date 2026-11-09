# Why Docker

*Section: Introduction*

1 We're going to start by looking at a high-level overview on why you need Docker. 2 Let me start by sharing how I got introduced to Docker. 3 In one of my previous projects, 4 I had this requirement to set up an end-to-end application stack, 5 including various different technologies, 6 like a web server using Node.js, 7 a database such as MongoDB, 8 a messaging system like Redis, 9 and an orchestration tool like Ansible.

10 We had a lot of issues developing this application stack 11 with all of these different components. 12 First of all, their compatibility with the underlying OS was an issue. 13 We had to make sure that all of these different services 14 were compatible with the version of OS we were planning to use. 15 There have been times when certain versions of the services 16 were not compatible with the OS, 17 and we've had to go back and look at different operating systems 18 that was compatible with all of these different services.

19 Secondly, we had to check the compatibility between the services 20 and the libraries and dependencies on the OS. 21 We've had issues where one service requires one version of a dependent library, 22 whereas another service requires another version. 23 The architecture of our application changed over time. 24 We've had to upgrade to newer versions of these components 25 or change the database and so on.

26 Every time something changed, 27 we had to go through the same process of checking compatibility 28 between these various components and the underlying infrastructure. 29 This compatibility matrix issue is usually referred to 30 as the matrix from hell. 31 Next, every time we had a new developer on board, 32 we found it really difficult to set up a new environment. 33 The new developers had to follow a large set of instructions 34 and run hundreds of commands to finally set up their environments.

35 We had to make sure they were using the right operating system, 36 the right versions of each of these components, 37 and each developer had to set up all that by themselves each time. 38 We also had different development, test, and production environments. 39 One developer may be comfortable using one OS, 40 and the others may be comfortable using another one. 41 Also, we couldn't guarantee that the application that we were building 42 would run the same way in different environments.

43 All of this made our life in developing, building, 44 and shipping the application really difficult. 45 So I needed something that could help us with the compatibility issue 46 and something that will let us modify or change these components 47 without affecting the other components 48 and even modify the underlying operating systems as required. 49 That search landed me on Docker. 50 With Docker, I was able to run each component in a separate container 51 with its own dependencies and its own libraries, 52 all on the same VM and the OS, 53 but within separate environments or containers.

54 We had to build a Docker configuration once, 55 and all our developers could now get started 56 with a simple Docker run command. 57 Irrespective of what the underlying operating system they run, 58 all they needed to do was to make sure 59 they had Docker installed on their systems. 60 And that's the problem Docker solves. 61 Docker takes the matrix from hell, 62 the tangle of services, libraries, dependencies, and operating systems, 63 and packages each piece into its own self-contained container.

64 The same setup runs the same way on every developer's laptop 65 in test and in production. 66 No more chasing version conflicts, 67 no more pages of setup instructions for new developer, 68 one Docker run command, and you're up.

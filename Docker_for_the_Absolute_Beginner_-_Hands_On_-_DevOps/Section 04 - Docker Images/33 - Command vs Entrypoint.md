# Command vs Entrypoint

*Section: Docker Images*

1 In this lesson, we will look at commands, arguments, and entry points in Docker. 2 Let's start with a simple scenario. 3 Say you were to run a Docker container from an Ubuntu image. 4 When you run Docker run Ubuntu, it runs an instance of the Ubuntu 5 image and exits immediately. 6 Now, if you were to list the running containers, you wouldn't 7 see the container running. 8 If you list all containers, including those that are stopped, you will see 9 that the new container you ran is in an exited state. Why is that?

10 Unlike virtual machines, containers are not meant to host an operating system. 11 Containers are meant to run a specific task or process, such as hosting an 12 instance of a web server, an application server, or a database, or simply to 13 carry out some computation or analysis task. 14 Once the task is complete, the container exits. 15 A container only lives as long as the process inside it is alive.

16 If the web service inside the container is stopped or crashes, the container exits. 17 So, who defines what process is run within the container? 18 If you look at the Docker file for popular Docker images, like nginx, you 19 will see an instruction called cmd, which stands for command, that defines the 20 program that will run within the container. 21 When it starts, it runs the nginx command. 22 For the MySQL image, it is the mysqld command.

23 What we tried to do earlier was run a container with a 24 plain Ubuntu operating system. 25 Let's look at the Docker file for that image. 26 You will see that it uses bash as the default command. 27 Now, bash is not really a process like a web server or database server. 28 It is a shell that listens for inputs from a terminal. 29 If it cannot find the terminal, it exits. 30 When we ran the Ubuntu container earlier, Docker created a container 31 from the Ubuntu image and launched the bash program.

32 By default, Docker does not attach a terminal to a container when it is run. 33 And so the bash program does not find the terminal. 34 And so it exits. 35 Since the process that was started when the container was created finished, 36 the container exits as well. 37 So, how do you specify a different command to start the container? 38 One option is to append a command to the Docker run command. 39 And that way it overrides the default command specified within the image.

40 In this case, I run the Ubuntu image with sleep five as the added option. 41 This way, when the container starts, it runs the sleep program, waits 42 for five seconds, and then exits. 43 But how do you make that change permanent? 44 Say you want the image to always run the sleep command when it starts. 45 You would then create your own image from the base Ubuntu 46 image and specify a new command.

47 There are different ways of specifying the command. 48 Either simply in shell form or in a JSON array format. 49 Remember when you specify it in a JSON array format, the first element in 50 the array should be the executable. 51 In this case, it's the sleep program. 52 Do not specify the command and parameters together as a single element. 53 The command and its parameters should be separate elements in the list.

54 I now build my new image and name it Ubuntu sleeper, and I can simply 55 run the image and get the same result. 56 It always sleeps for five seconds and exits. 57 But what if I want to change the number of seconds it sleeps? 58 Right now it is hard-coded to five seconds. 59 As we saw before, one option is to run docker run with the 60 new command appended to it. 61 In this case, sleep 10. 62 And so the command run at startup will be sleep 10, but 63 it doesn't look very good.

64 The name of the image Ubuntu sleeper already implies that 65 the container will sleep. 66 So we shouldn't have to specify the sleep command again. 67 We only want to pass in the number of seconds the container should 68 sleep and the sleep command should be invoked automatically. 69 That is where the entry point instruction comes into play. 70 The entry point instruction is like the CMD instruction in that you can 71 specify the program that will run when the container starts and whatever you 72 specify on the command line gets appended to the entry point.

73 So the command run when the container starts is sleep 10. 74 That's the difference between the two. 75 With the CMD instruction, the command line parameters passed will 76 replace the command entirely. 77 With entry point, the command line parameters are appended to it. 78 In the second case, what if I run the Ubuntu sleeper image without 79 appending the number of seconds? 80 Then the command at startup will be just sleep and you get the 81 error that the operand is missing.

82 How do you configure a default value for the command? 83 If one was not specified on the command line, that's where you would use 84 both entry point and CMD together. 85 The CMD instruction is appended to the entry point instruction. 86 At startup, the command would be sleep five. 87 If you didn't specify any parameters on the command line, if you did, that 88 value will override the CMD instruction.

89 Remember for this to happen, you should always specify the entry point and 90 CMD instructions in the JSON format. 91 And finally, what if you really want to modify the entry point during 92 runtime, say from sleep to an imaginary sleep 2.0 command. 93 In that case, you can override it by using the dash dash entry point 94 option in the Docker run command. 95 So the final command at startup will be sleep 2.010.

96 That's CMD versus entry point. 97 Use them together for the most flexibility. 98 Now fixed, executable, overridable arguments.

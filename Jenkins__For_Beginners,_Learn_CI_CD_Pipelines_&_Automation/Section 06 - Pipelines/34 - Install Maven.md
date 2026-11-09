# Install Maven

*Section: Pipelines*

1 We are gonna get started 2 with a pipeline very shortly, 3 but there's one key step we need to add. 4 I'm going to open up a new tab 5 and I'm going to run docker container ls. 6 What we need to do is install Maven. 7 So what we're gonna do is copy the container ID. 8 And apologies on my terminal, 9 I made it bigger so you can see it. 10 If I open up another terminal screen, 11 let me show you what it will look like.

12 So here you can see the container ID. 13 The command we need to run is docker exec -it -u root. 14 Paste in the ID and then /bin/bash. 15 And again, let's quickly break this down. 16 If you're not familiar with Docker, what this is going to do 17 is effectively log us into our container. 18 It's gonna give us an interactive terminal 19 so we can type and get the output. 20 We're gonna log in as root 21 and the command we're going to run is /bin/bash.

22 So it's gonna give us a terminal. 23 Now let's go ahead and hit Enter. 24 Awesome, so you can see now root@ and our container ID. 25 The commands we need to run are apt-get update. 26 Then apt-get install, and maven. 27 Type Y for yes to continue. 28 And we'll leave that running. 29 Quick word of warning on this. 30 All the information about Jenkins is persisted. 31 Unfortunately, plugins like these 32 won't be with our container.

33 So for whatever reason it goes down, 34 you'll need to reinstall Maven. 35 And again, this will also be the same process. 36 If you want to experiment with other tools 37 inside a Docker container, this is the way you can do it. 38 Ideally though, you may want 39 to look into building your own Docker image 40 if this is something you're gonna be doing more frequently 41 as you can save all these steps.

42 And if you want to find out more 43 about building Docker images, I have a course on Docker. 44 I'll teach you everything you need to know. 45 Brilliant, now we've got Maven installed. 46 Now let's exit out of the terminal session. 47 Awesome, and we can close this tab down. 48 So now let's get started with our pipeline.

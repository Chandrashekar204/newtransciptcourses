# Delete Volumes

*Section: Clean Up*

1 To view our volume, 2 we can "run docker volume ls", 3 and it's worth copying this name. 4 Now, if you want to keep what you've created so far, 5 don't delete this volume, 6 but if you want to, this is what I'm gonna show you now. 7 Now with Docker, it's a bit unusual what they do. 8 When we create a container, 9 it's almost like starting up a VM. 10 And when we stop it, 11 it effectively puts it in a stopped state 12 so we can start it up again.

13 Now, this is a bit annoying, 14 but the way you can see it 15 is running "docker container ls -a". 16 And again, your screen is gonna look 17 a lot different to mine, 18 but if we scroll up to the top, 19 as you can see, when filming this course, 20 I spun up and stopped my Jenkins container multiple times. 21 So I would need to run "docker container rm" on these IDs. 22 Now there is a nuclear option, as some would refer to it as.

23 So to do that, we've run "docker container rm" 24 and then dollar sign in brackets, 25 "docker container ls -aq". 26 A returns all of them as we've seen, and Q returns VIDs. 27 Go ahead and hit Enter, and it's run. 28 So now if we run "docker container ls -a", 29 we can see I have no containers on my system. 30 Now we can delete the volume. 31 So now we can run "docker volume rm", 32 and paste in the name.

33 So there we go. 34 We've now cleared up GitHub 35 and we've also cleaned up Docker and Jenkins.

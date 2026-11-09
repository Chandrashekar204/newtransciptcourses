# Image Tags

*Section: Docker Run Commands*

1 We will now look at some of the other docker run commands. 2 In this first part, let's talk about image tags. 3 We learned that we could run a Redis container 4 with a simple run command, 5 which gives us the latest version of Redis, 6 currently version 8.6.1. 7 But what if we want to run another version, 8 like say an older version, such as 7.4? 9 Well, you specify the version separated by a colon.

10 This is called a tag. 11 In that case, Docker pulls an image 12 of the 7.4 version of Redis and runs that. 13 Also notice that if you don't specify any tag, 14 like in the first command, 15 Docker considers the default tag to be latest. 16 The latest tag points to the latest version 17 of that software, 18 which is governed by the authors of that software. 19 So as a user, how do you find information 20 about these versions and what is latest?

21 Over at Docker Hub, look up an image 22 and you'll find all the supported tags in its description. 23 Each version of the software can have multiple short 24 and long tags associated with it. 25 For example, version 8.6.1 also carries the latest tag today. 26 Now, every time we pull a new version of an image, 27 Docker stores it on the host as a separate entry. 28 So if I pulled both Redis 8.6.1 and Redis 7.4 earlier, 29 they're both sitting there on my host.

30 To see all the images I have locally, 31 I run the docker images command and it gives me a table, 32 the repository, the tag, and the image ID for each one. 33 And if I want to clean up a specific version 34 that I no longer need, 35 I run docker rmi followed by the exact tag. 36 For example, docker rmi redis 7.4. 37 That removes just that tagged image 38 and leaves the other versions alone. 39 Now, one quick note on the latest tag before we move on.

40 The latest tag is convenient for quick experiments 41 and trying things out, 42 but in production, you should always pin to a specific tag, 43 something like redis 7 for Alpine. 44 The reason is that latest is a moving target. 45 The day you redeploy, 46 the image authors may have pushed a new version 47 and your container quietly upgrades under you, 48 sometimes with breaking changes. 49 A pinned tag gives you the exact same image every time 50 and you decide when to bump the version, 51 not the upstream maintainers.

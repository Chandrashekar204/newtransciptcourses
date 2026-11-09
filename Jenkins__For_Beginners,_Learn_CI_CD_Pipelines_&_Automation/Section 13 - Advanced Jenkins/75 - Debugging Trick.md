# Debugging Trick

*Section: Advanced Jenkins*

1 Hi, and in this video, I'm going 2 to show you a really useful debugging trick. 3 Now, this is useful if you need 4 to insert some sort of delay. 5 Quite commonly, you might see something like this 6 with Kubernetes where you need to wait for something 7 to actually deploy before moving on to the next step, 8 because sometimes you can get failures. 9 And also when running cleanup jobs, 10 especially with Kubernetes, it doesn't delete 11 the resources automatically.

12 Sometimes it could be checks 13 or it'll start complaining that once you've run 14 one cleanup item and tried to run a next, 15 it complains that the other one is in use. 16 Now that's a bit of a niche case, 17 you may be doing something completely different, 18 but let me show you how we can go ahead and add in a pause 19 or some sort of break to say wait X amount of time. 20 So what I'm going to do is use this job here, My Pipeline.

21 Click on configure, 22 and this is really, really straightforward. 23 Inside steps, what we can do 24 is add this function called sleep. 25 And inside brackets, we put in seconds 26 how long we want Jenkins to pause. 27 So if we need to wait 10 seconds, we'll put in 10 seconds. 28 If we need to wait five minutes, we add in 300 seconds. 29 So let's go ahead and add 10 seconds. 30 What it'll do is go ahead, clean up, 31 clone in for GitHub Repo, run Maven install, 32 and then it's going to pause for 10 seconds.

33 It's not going to do anything else. 34 And then once it's ready, 35 it will go ahead and run the next stage. 36 Let's go ahead and save that, and let's build it now. 37 Although the times don't show it, the build was quick, 38 but it did sleep for 10 seconds. 39 And again, this is really useful for debugging 40 and also when needing to add a pause for something. 41 I mentioned before about Kubernetes.

42 Sometimes if you try and do something like kubectl delete 43 and you start with the service 44 and then you do deployments, 45 sometimes Jenkins can get a bit funny with that 46 because it doesn't like you automatically trying 47 to run something else while it's still waiting 48 for the first object to get deleted. 49 So normally the way we would get around this is we would put 50 kubectl delete and we put in all the things, 51 set deployment service on a line.

52 And then if we had something else we had to delete, 53 we'd put in a 30 to 90-second sleep break in there 54 and then run the next kubectl delete. 55 And let's say it was two separate deployments 56 with services, et cetera. 57 We'd wait for deployment one, then put in our 30 58 to 90-second break, and then go ahead 59 and put in the second one to go ahead 60 and delete deployment two. 61 Up next, let's have a look at some groovy logic, 62 more specifically if statements.

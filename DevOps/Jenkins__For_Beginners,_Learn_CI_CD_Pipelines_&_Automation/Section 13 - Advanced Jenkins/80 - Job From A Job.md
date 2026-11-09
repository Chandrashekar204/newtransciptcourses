# Job From A Job

*Section: Advanced Jenkins*

1 Hi, and welcome to this lesson. 2 You're going to learn how to build a job from a job. 3 Now, you can have something like an IF statement block, 4 and you may have a separate job for deploying. 5 So you might say is if the build is successful, 6 then go ahead and run the deployment job, 7 and you can trigger that from the current job. 8 So now let's have a look at how you set that up. 9 What I'm going to use is the pipeline job.

10 So I'm going to click on my pipeline, 11 and we're going to go to configure. 12 Scroll down to the bottom. 13 And what we might want to do in here is remove 14 the sleep statement so it runs a bit faster. 15 Inside, we've got this test stage, so we want to copy that. 16 Just below it, let's paste it. 17 And we're going to call this build remote. 18 Now we don't need this DIR. 19 And what we're going to run is build, 20 but in single quotes, the name of the job.

21 So I'm going to use boolPipeline. 22 And we know by default it's got a parameter 23 and that is set to false, so this is going to work. 24 Now we'll just quickly check formatting on this 25 and matches, that matches, 26 and this will be for stages. 27 Excellent. 28 Now let's go ahead and save this 29 and let's build it. 30 Awesome. 31 And we can now see it's building remotely. 32 Now if we click on the logs, we can see scheduling project, 33 boolPipeline, and we can see it's running build number six.

34 So now we can go to build number six 35 and we can see boolean parameter is set to false. 36 Up next, let's have a look at how we can change that.

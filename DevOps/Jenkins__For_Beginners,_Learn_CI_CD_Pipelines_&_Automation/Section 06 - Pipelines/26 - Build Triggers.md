# Build Triggers

*Section: Pipelines*

1 A quick word in build triggers. 2 Probably the two most popular ones you'll see 3 are poll SCM and build periodically. 4 Now, what the build triggers do 5 is they say when to run this job. 6 And the reason these two are so popular, 7 we'll dive into now. 8 With build periodically, 9 you can set an interval of when to build it. 10 Now, for example, if you have something like a cleanup job, 11 and this is something 12 probably us operations engineers will look at, 13 we might say, let's deploy an environment in the morning 14 and let's tear it down at seven o'clock at night.

15 So that's something we might want to do periodically. 16 Or maybe a cleanup job you might say every hour 17 we need to clear something down. 18 Perfect. 19 The other option is poll SCM. 20 Now again, this is probably 21 one of the most popular ones there are. 22 With poll SCM, what it will do 23 is then look at our source code management. 24 So this is probably going to be GitHub or Bitbucket. 25 And if a developer or one of us makes a change, 26 what will happen is Jenkins will pick up on this change 27 and then run the job.

28 And again, this is why 29 the whole CI/CD process is so popular. 30 So this means as soon as the developer makes a change, 31 commits it to GitHub, the job now runs, builds, tests, 32 and it's all taken care of. 33 Now let's have a look at getting started with our pipeline.

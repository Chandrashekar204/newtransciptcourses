# Maven Setup

*Section: Pipelines*

1 What we're going to be using 2 for the demo is this simple Java Maven app 3 from Jenkins themselves. 4 Maven is used to build the Java file or the main executable, 5 and if you're working on a project that uses Java a lot, 6 you'll probably either see they're using Maven 7 or Gradle to build the Java file. 8 Now because it's something you'd see so often in industry, 9 I thought I had to include it in the course 10 just so you get a bit of exposure.

11 But also this is great for pipeline work, 12 especially as a demo, 13 because now what we can do is add more steps to our pipeline 14 so we get really experienced and know what we're doing. 15 Now because of one of the limitations 16 of what we're going to encounter, 17 we're going to add an additional step 18 where we're actually going to pull this in. 19 Normally what we do in a real-life setup 20 is like we've done here, 21 and again, I'll include a link to the documentation 22 so you can have a look through, 23 is they have a file in here called Jenkinsfile.

24 So normally what they do is they'd set up a Jenkins job, 25 and you can specify what file are you looking for 26 and even the folder structure. 27 They'll say look in simple-java-maven-app for Jenkins 28 and look for a file called Jenkinsfile, 29 and it would be this pipeline here. 30 Now, if this syntax looks a bit weird to you, 31 I'm going to take you through step by step 32 exactly what this does, 33 but we're not going to be using this.

34 Instead, we're going to be creating our own pipeline. 35 And now if we go back, 36 what would happen in a real-life situation, 37 which is what we're going to see later on, 38 is that if we use something like this, 39 what we're going to see if we use something like this 40 is that we'd have the application of what we want to build. 41 We'd have it inside the GitHub repo, 42 meaning what we do is we configure the Jenkins job 43 using GitHub or Bitbucket.

44 It would then look for the Jenkins file, 45 and from there it would do all the work. 46 So this is something we'd normally add inside. 47 This is going really off tangent, so let's realign our focus 48 and get started with our pipeline.

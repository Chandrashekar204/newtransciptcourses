# Settings Explained

*Section: Jenkins 101*

1 Freestyle Project is the most common 2 one to use. 3 It's like a blank slate. 4 We can create whatever we want. 5 Next up, we've got Pipeline. 6 Now, if you remember from the CI/CD lecture, 7 when we had those different phases, we had build, test, 8 deploy, those would be part of a pipeline. 9 As part of a pipeline, there'd be different steps. 10 And you'll see when we come around to using the pipeline 11 that this is where we create our declarative pipelines.

12 Multi-configuration projects. 13 These aren't used as often, 14 but they're an interesting concept. 15 So if we have a project and we need to run the same job, 16 but with slightly different parameters, 17 this is a good option to use. 18 Folder is self-explanatory. 19 This is a way of organizing our jobs. 20 A tool might have a folder for testing, a folder for build. 21 It's a nice way we can keep our jobs neatly organized.

22 GitHub Organization, very similar to Multibranch, 23 but for GitHub. 24 Now, Multibranch is probably the most powerful 25 type of pipeline you can set up. 26 If you're used to working with GitHub 27 and different branching strategies, 28 probably the most common one is GitFlow, 29 Multibranch pipelines are incredibly powerful 30 because now what you can do is set up a job, 31 but now it can run every single branch of that repo.

32 And for those of you not familiar with GitHub, 33 we have a repository and we could have multiple branches. 34 A branch is like taking the code and making the changes 35 in our own little environment. 36 Then later, what we'll do is merge those changes 37 back in to another branch. 38 Now, the advantage of Multibranch pipeline, 39 as we mentioned, is that if we have multiple branches, 40 we can have one job that runs on every different branch.

41 Again, why this is so popular? 42 If you're working in a team and you create a feature branch, 43 you don't have to set up another job. 44 The Multibranch pipeline will take care of that for you. 45 Now let's get started with a Freestyle project. 46 So what we're going to do is call it "My First Job." 47 Click Okay. 48 Awesome. 49 So this is the page you're greeted with. 50 And also, as I mentioned before, that a lot of courses 51 will expect you to work in this sort of environments.

52 Truth be told, you'd be probably using some sort 53 of source control management like GitHub, Bitbucket, 54 and what you do is you'd have your Jenkins file 55 inside the repo and you'd configure what you want to set up. 56 Now that's a bit complex to what we're looking at right now, 57 this is to gently get you started with Jenkins. 58 So what we want to do is scroll down to the bottom. 59 Where it says Build, add a build step.

60 So we're going to say Execute Shell. 61 And we're going to add echo "Hello 62 From My First 63 Jenkins Job!" 64 Now let's click Save. 65 And now what we can do is click Build Now. 66 Excellent. 67 Now if we click on this icon here, number one, 68 go to Console Output. 69 You can see our first message. 70 And there we go. 71 Setting up a Jenkins job is as simple as that.

# Setting Up the MultiBranch Pipeline

*Section: MultiBranch Pipelines*

1 So we've got two options now. 2 We can either create the branch now 3 or we could set up a job. 4 What we're going to do for way is elect copy this URL 5 because what we're going to do is set up a new pipeline. 6 So let's go back to Jenkins, new item, 7 and we'll call this multi-branch. 8 And we'll select multi-branch pipeline. 9 Notice there are a few differences. 10 So let's start by adding our source.

11 This is going to be Git. 12 Now by default, 13 what Jenkins is going to do is automatically look 14 and discover any new branches. 15 Next, let's move down to the build configuration, 16 and you can see here, 17 Jenkins file is the only option available. 18 What we need to do is set up a path, 19 which we said is in Jenkins/Jenkins file. 20 Often the item strategy, we're not too worried about this 21 because what we want to do, 22 if we build anything, we want it to delete it.

23 And then we've got this last setting here, 24 scan multi-branch pipeline triggers, 25 and we want to set the interval. 26 As I mentioned before, when I've been working in industry, 27 two minutes seems to be the perfect time. 28 This may vary on the project or team you're working with. 29 This gives enough time usually that if you're the developer 30 or the DevOps engineer, by the time you've gone ahead, 31 sorted out with Jira, created a new branch and so on, 32 it's usually already picked up and set off for job.

33 If not, there's a trick we can use to force it to scan 34 and pick up the branch. 35 So now let's go ahead and save this. 36 So now what it's doing, the scan multi-branch log is 37 it's now querying GitHub to say on our repo, 38 how many branches are there? 39 And we saw there were two, so there is this BitWiseman patch 40 and we've also got Master. 41 And we know Master's got our pipeline in, 42 and we've also got this complete stage.

43 And we know the BitWiseMan one has been copied across 44 when we clone the repo. 45 So now let's go back to multi-branch. 46 We can see we have BitWiseman and that's going to fail. 47 More than likely it doesn't have a Jenkins file 48 in that branch. 49 Now we're going to ignore that for now. 50 What we're interested in is Master. 51 Now let's go ahead back to our repo where it says Branch. 52 We're going to click on it and we're going to create one.

53 Now this might be something like a bug fix 54 or it might be a feature. 55 So what I'm going to do is simply call line, New Pipeline. 56 And then what we want to do is click on create branch. 57 And this is going to say create branch, 58 new pipeline from Master. 59 There we go, we click on that. 60 And now we can see here back in branch, 61 it now says New Pipeline. 62 It's all going to happen shortly in about two minutes.

63 It's going to scan and it will pick up a new branch in here. 64 But if we want to force it, 65 what we can do is click on Scan Multi-Branch Pipeline Now. 66 And as we can see, if I refresh, 67 it's now picking up new pipeline. 68 And there we go, that's now built. 69 As an example to show how it's different from Master, 70 for those not familiar with branching, we might say, 71 okay, we don't want that message at the end.

72 We don't want it to show complete. 73 So we can go in here, we can edit. 74 We can go down to our stage. We can remove it. 75 And we'll put in here removed, 76 completed, stage. 77 I want to put that in quotes. 78 Just makes it obvious. 79 And we want to commit it directly to new pipeline branch. 80 So commit the change. 81 Awesome. 82 Go back to our multi-branch. 83 And if we scan it now, 84 same thing again, like how it pulled SCM, 85 it will pick up and see if it is a new change.

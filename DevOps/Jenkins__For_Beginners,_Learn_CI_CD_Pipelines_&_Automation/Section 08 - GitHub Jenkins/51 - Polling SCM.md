# Polling SCM

*Section: GitHub Jenkins*

1 Hi, and in this video, I'm gonna show you 2 how you can set up your Jenkins job to check 3 for the latest change and pull it in. 4 So you may hear this term called Poll SCM, 5 which means Jenkins is going to check on your platform. 6 So this might be GitHub or Bitbucket, 7 and it's gonna check for any changes. 8 And if it detects a change, 9 it's going to go ahead and build the job. 10 And it's pretty straightforward to do, 11 and you'll see later with the multi-branch pipeline 12 that this is the default option.

13 So let's have a look. 14 Let's go on our GitHub pipeline, click on Configure, 15 and here we have Build Triggers. 16 It's usually two of the most common ones 17 are build periodically. 18 Now, this is quite useful if you have something like 19 a pipeline or something that you need to deploy once 20 or at a set times. 21 With some companies, they try and cut back on costs. 22 So what they'll do is they'll say at 7:00 at night, 23 shut down the environment, 24 and this usually with something like Terraform.

25 And then what they can do is set a Jenkins job, 26 so in the morning at say 8:00, 27 an hour before everyone comes in. 28 Go ahead and recreate the environments. 29 And this wouldn't be for prod, 30 this would be for like testing, 31 dev, QA, that sort of thing. 32 But that is where build periodically 33 can come in and it's quite popular. 34 What we're interested in here, for the example, is poll SCM.

35 And what we can do in here is set a schedule, 36 how often we want to check. 37 Now, from what I've seen in industry, 38 the most common interval for this is two minutes. 39 Some people complain if they set it to one minute 40 that it runs too frequently, 41 and five minutes it can cause delays with dev and testing. 42 So two minutes seems to be the golden time. 43 Now you have to set this up as if it were a cron job.

44 So what I found here is this tool, 45 and I've used it a couple of times in the past, 46 called Crontab Guru, and I'll include a link to it as well 47 because if you're not familiar with cron jobs 48 and you start seeing all the asterisks 49 and wondering why some have numbers 50 and when it's gonna run, 51 this tool is gonna make your life so much easier. 52 So if we want to set it to two minutes, 53 we set two in a minute.

54 The hour, we want it to run every hour, 55 so we'll add an asterisk. 56 And this is where we want to put in the poll SCM schedule. 57 So let's do that now. 58 Two, star, star, star, star. 59 So this is saying run two minutes all the time. 60 So let's go ahead and save that. 61 So you may see this pop-up come up here, 62 and you may be wondering what this H does. 63 So let's set this. 64 What it does is it sets a hash and it picks a random time.

65 So we've said run every two minutes. 66 What this will do is then pick a random time, 67 so between zero and 59. 68 So it may run at two minutes and 37 seconds, 69 or it may run at two minutes and one second. 70 So let's go ahead and save that. 71 So now every two minutes, it's gonna scan for a change, 72 and if it picks one up, it's gonna go ahead and build it. 73 So let's go back to our code in GitHub, go to our scripts, 74 and go to our Jenkins file.

75 So what we could do is add a stage. 76 And we could call this Complete and steps. 77 Let's remove that and put an echo. 78 I'm gonna use single quotes 79 to match what we've got set up here. 80 And we're gonna say Job Complete. 81 Now we want to save this. 82 So we'll say, added completed stage to pipeline. 83 Let's commit the change. 84 Awesome. 85 And we're going to enable auto refresh on this.

86 And what we should see is in roughly two minutes 87 or so that it will pick up a change and build it. 88 And as we see here, it's now polled the SCM 89 and it's seen there's another commit, so it's now building. 90 Awesome, and now it's completed. 91 And here we go, we can see my commit message, 92 added completed stage to pipeline. 93 And we can see that here. 94 So that's how we can poll SCM to pull in the latest changes.

95 And this is something you'll see commonly 96 when working as a team with developers. 97 So every time we make a change, 98 they commit it, start to build. 99 That wraps up this lesson. 100 Up next, we're gonna be looking at 101 multi-branch pipelines. 102 I look forward to seeing you in that video.

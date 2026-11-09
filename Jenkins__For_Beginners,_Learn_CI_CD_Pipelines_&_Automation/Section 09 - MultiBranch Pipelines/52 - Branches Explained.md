# Branches Explained

*Section: MultiBranch Pipelines*

1 Hi, and in this lesson, 2 you're going to learn about multi-branch pipelines. 3 If you're familiar with Git, 4 and have worked with it before, 5 and know the concept of branches, 6 brilliant, you can jump ahead, 7 but if you're new to Git and not quite aware of 8 what branches are, let's have a quick look into those now. 9 So as you can see here, we've got two branches, 10 but what exactly is a branch?

11 Now in the last demo, what we did is 12 we made a change on Master. 13 Now, if you're working on a team, this is a huge no, 14 you should never directly make a change on Master. 15 Master would normally be one of the latest releases. 16 And in other words, you could call it 17 like the absolute truth. 18 This is like the stable code, 19 we know it works, and it's in production. 20 If I then want to make a change, 21 if I can't make it directly on Master, 22 what I'll do is I'll create my own branch, 23 and if you're working in a team, 24 or using something like Bitbucket, 25 you'll have Jira integration, 26 so you might call the branch name the ticket number.

27 Then what you can do is go ahead 28 and make your changes, check for your work, 29 and this is where the multi-branch pipeline comes in, 30 which we're gonna cover very shortly, 31 and then if you are happy your branch, 32 which is basically a snapshot of Master, 33 but now plus your changes, if you're happy 34 that's now working, what you can do is then go ahead, 35 and merge it back into Master.

36 Then fast-forward when your team make new changes, 37 they'll also include yours. 38 So now let's jump into the multi-branch pipeline, 39 and you'll also get a really good understanding 40 of how these branches work.

# Stages Recap And Build

*Section: Pipelines*

1 So first step is to run a cleanup, 2 clean up anything we've run before 3 and make sure nothing has persisted. 4 The most likely thing that's going to remain 5 if we don't include this is this folder here. 6 So when GitClone runs again, it would complain 7 and say that there's already a folder inside. 8 Next, what we're going to do 9 is clone down the repo from GitHub, 10 then we're going to go ahead and build it.

11 And lastly, we're then going to go ahead and test it. 12 So what we can do is copy all this, Control A, Control C, 13 go back over to our browser inside our pipeline. 14 Before we go ahead and paste it, 15 well worth running refresh 16 just to make sure we're still logged in. 17 In my case, I've been logged out, 18 so what I want to do is log back in. 19 Now what we can do is paste in our pipeline script.

20 And as you can see before, as I mentioned, 21 this will be incredibly hard and annoying to show you this 22 in a tiny little editor like this. 23 We're not going to set any options here, 24 we're just going to go ahead and click save. 25 And then when we're ready, we can click build now. 26 Also worth using, enable auto refresh. 27 It will refresh a page every 10 seconds. 28 And now it's finished building, let's disable auto refresh.

29 It can get a bit annoying when you're looking through things 30 and it starts kinda refreshing the page. 31 But there we go, congratulations, 32 you have built your first pipeline. 33 So if you've seen this before, 34 wondering what these green blocks are, 35 those are your stages. 36 Now let's have a little breakdown 37 of some of the options with Jenkins, with our pipeline.

# Replay

*Section: Pipelines*

1 One of the biggest pains with Jenkins is 2 if your Jenkins file is inside a repo. 3 That means if you need to make a change 4 because there's an error, 5 you then need to clone it down 6 or pull down the latest change, 7 make your change, commit it, 8 push it up, and build the job again 9 more than likely to find you missed a curly brace 10 or put it in the wrong place 11 and have to repeat the process again.

12 So what I'm going to show you now is probably 13 one of the most powerful debugging tools in Jenkins. 14 And to use it, we click on the build job 15 and click on replay. 16 A quick word of warning on this, 17 in certain organizations, 18 this may actually be disabled for security reasons. 19 If it is enabled, you're in luck. 20 So as you can see here, we have our pipeline script, 21 but what Jenkins allows us to do 22 is actually go ahead and edit it.

23 So what we can do, again, 24 if we were using GitHub, we can go inside, 25 put in our experimental changes in here, 26 and then once we've got it working, 27 we can keep failing as many times as we need. 28 But then what we can do is once we have the perfect config, 29 copy it, paste it inside from that Visual Studio Code, 30 and commit the change. 31 And as far as everyone else is concerned, 32 we did it in a single commit.

33 And, again, this is really useful for debugging. 34 But one word of warning, 35 if for whatever reason your job fails again 36 and it shows up in red, 37 usually because of some sort of syntax error, 38 what's really annoying is Jenkins will display 39 this really horrible looking error page 40 and you won't see this. 41 But, again, this is really useful if you need 42 to make some quick changes or want to test something.

43 So rather than, again, pushing something up 44 and waiting for Jenkins to build, 45 you can go ahead, click replay, make a minor tweak, 46 and if you're happy that works, 47 then go ahead and commit it.

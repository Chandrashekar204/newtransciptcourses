# DIR Explained

*Section: Pipelines*

1 With Jenkins, it creates a folder, 2 usually the job name and a random string of numbers, 3 so unique identifier. 4 And what can happen is each stage 5 will effectively revert back to that original parent folder. 6 But also, if we do something like SH and CD, 7 what can happen is this next stage will revert back 8 to the original parent folder, and it will fail. 9 So the way we can get around that 10 is using something called DIR.

11 It's the equivalent of running CD, 12 but it's persistent and every step or action we take 13 in between the brackets 14 will always be inside that directory. 15 If you're wondering why we need this, 16 when we clone down this repo, 17 it's gonna create a folder called Simple Java Maven App. 18 So what we need to do is work inside it. 19 So now let's go ahead and add it.

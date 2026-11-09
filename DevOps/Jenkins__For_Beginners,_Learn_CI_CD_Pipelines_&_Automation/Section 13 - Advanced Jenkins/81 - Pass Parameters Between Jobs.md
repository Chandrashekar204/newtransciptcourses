# Pass Parameters Between Jobs

*Section: Advanced Jenkins*

1 So in our last lesson, we set a parameter, 2 and we triggered off the Boolean pipeline job. 3 Now, we're gonna take it one level further, 4 so let's copy our pipeline script, 5 so we'll go to my pipeline, 6 go to configure, 7 scroll down, and we can see we got build bool pipeline. 8 Let's copy over code and go over to Visual Studio Code. 9 I'm going to put it inside our parameters folder, 10 create a new folder, and we're gonna call this remoteJob.

11 Inside, you've guessed it already, 12 we're gonna create a Jenkins file. 13 Paste it in, and let's save it. 14 Same as before, we're gonna use build, but instead, 15 we're going to add an additional word, which is build job, 16 followed by a colon, the name of the job, 17 so we've got our job name, which is boolPipeline, 18 followed by a comma, and we're gonna set up parameters next. 19 These are the parameters we want to pass across.

20 I'm going to include a link to the documentation 21 because it's not the easiest to understand, 22 and this link here is gonna be a bit confusing. 23 We then create an array, 24 and we have a nested list of objects, 25 and inside the top one is our Boolean one, 26 which has a name and a value, which our name 27 is gonna be the name of the Boolean parameter, 28 and the value, we're going to set to true.

29 So bear with me, 30 because this is gonna be a little bit confusing, 31 but let's break it down. 32 So we said it goes in an array, and then it's nested, 33 so it's an array within an array. 34 Then we need to use class, colon, 35 and then, in single quotes, 36 "BooleanParameterValue" followed by the name, 37 which we can check out if we go to boolean/Jenkinsfile. 38 We see it's called myBoolean, 39 so let's go ahead and copy that.

40 Again, in single quotes, followed by a comma, 41 and then the value. 42 We're gonna set this to true. 43 There we go. It's a bit complicated. 44 In fact, what we're doing is passing over this array 45 with our parameters. 46 So now, let's copy this code, go back over to Jenkins, 47 control A, delete all of it, paste it in, 48 give it a second or two. 49 No major warnings, which is good, 50 and now, let's go ahead, save, and let's run it.

51 Awesome, and now, let's go ahead, check out our build job, 52 check out our console output, and there we go. 53 We have now passed a parameter to another job. 54 It's a little bit confusing, 55 but once you get your head around it 56 that what we're doing is then passing the name 57 and we're putting it into an array, 58 and it's a little bit messy, but we've got this file. 59 You can always reference it if you need it, 60 and again, I'll include a link to this page, 61 because it's gonna tell you all the options 62 and parameters you need to pass in.

63 Next up, let's have a look at plugins.

# Clean Up Stage

*Section: Pipelines*

1 Let's get started with our first stage, 2 so now let's type in stage, put it in brackets, 3 and inside double quotes, what we want to call the stage. 4 For this first stage, I'm going to call it "clean up." 5 The reason we're adding a cleanup stage 6 is because when Jenkins runs a job, 7 he creates a folder on the system, 8 and sometimes, what can happen 9 is there can be remains from a previous build.

10 What'll happen is this will then cause errors 11 and stop the job from running, 12 so good practice is to add a cleanup job 13 at the beginning of your script. 14 You could add it at the end, 15 but if there's some sort of failure halfway through, 16 then the rest of the job won't continue, 17 so by putting it at the beginning, 18 we guarantee our environment is clean and pristine 19 every time we start.

20 Let's continue. 21 Inside the stage, we add another set of curly braces, 22 and inside, we then add steps. 23 This is what we want to do during this stage, 24 and again, in curly braces, 25 we want to run a Jenkins pipeline option called deleteDir, 26 with a capital D, and put it in brackets. 27 This will clear the working folder we're using 28 inside Jenkins. 29 As you can see, this plugin is incredibly useful.

30 We already have four sets of curly braces, 31 and we're only about a quarter of a way through. 32 In case you're wondering 33 where I got this deleteDir option from, 34 in the pipeline basic steps, if I type in "DIR," 35 we can see deleteDir, or deleteDir or Directory, 36 is a function we can add. 37 Surely, we're going to be using the DIR option, or dir, 38 to work inside the folder from the Git repo 39 we're going to pull down, 40 and again, in here, I've included the link.

41 There's some really useful stuff, 42 and if you ever get stuck on how to use it, 43 you can always have a look online, Jenkins, 44 put in the command name, hit enter, 45 and you'll probably find something on StackOverflow 46 or some documentation on another site, 47 but again, this is just how powerful Jenkins is, 48 with loads of different built-in options. 49 Now, let's go back to our pipeline.

50 Next, let's add our next stage.

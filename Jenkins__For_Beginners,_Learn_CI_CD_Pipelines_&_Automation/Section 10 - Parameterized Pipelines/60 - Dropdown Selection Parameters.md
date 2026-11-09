# Dropdown Selection Parameters

*Section: Parameterized Pipelines*

1 Okay, we're back over in Visual Studio Code. 2 Let's copy our script, let's go back to our folders, 3 and inside Params, we're gonna create another folder. 4 We're gonna call it Choice, 5 and inside, we're going to create a new file 6 again called Jenkinsfile. 7 Paste it in. Let's go ahead and save it. 8 Let's minimize this. 9 So as we mentioned before, we had string input here, 10 which is really neat, so we can manually type in 11 which environment we want it to deploy to.

12 Now, the problem with this is things like string validation 13 and maybe an engineer isn't sure 14 which environment name to use, 15 so that's where we can standardize it with a dropdown list. 16 So to do that, we swap out String for Choice. 17 I'm going to leave the name as is, 18 and we're gonna knock out this default value, 19 because normally, what it's gonna do 20 is revert to the first choice.

21 And we set it up like this. 22 Choices, colon, and then in square brackets, 23 we add the options. 24 Because we're gonna be dealing with strings, 25 we're gonna go in double quotes. 26 So we might say "TEST," 27 "DEV", "QA", 28 "PRE-PROD," 29 and we'll add in "PROD" as the last one. 30 Now, the square brackets, 31 again, if you're familiar with programming, 32 this is an array, 33 and if you're not familiar with arrays, 34 they're a way of storing multiple variables or values.

35 So in this case, we're storing multiple strings, 36 which are our environment names. 37 And we'll sort this out and we'll set string to Choice. 38 Save that, let's copy it, 39 and now let's go back over to our browser. 40 New Item. Going to call this choicePipeline, 41 and select Pipeline. 42 Let's go ahead and paste it in. 43 Save it. 44 We'll click on Build Now, so it picks up. Awesome. 45 And let's see what it's defaulted to. Test.

46 And that's why we don't set the default value, 47 because it's always going to revert 48 to the first one in the list. 49 Now, let's go back over to our browser, back to Dashboard, 50 back to choicePipeline, 51 and now we can see Build With Parameters. 52 And now we've got a dropdown. 53 Which environment to deploy in. 54 And again, let's pick PROD. Click Build. 55 There we go. And now let's check the output.

56 Awesome. And there we go. 57 That's now set to PROD.

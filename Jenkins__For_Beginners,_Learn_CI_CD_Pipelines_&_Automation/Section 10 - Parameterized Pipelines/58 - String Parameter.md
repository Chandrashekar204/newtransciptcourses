# String Parameter

*Section: Parameterized Pipelines*

1 Okay, we're now back over 2 in Visual Studio Code. 3 So now, let's have a look at how we can get a text 4 as user input. 5 What I'm going to do is copy this code here, 6 and we're going to use this as our template. 7 Inside our parameters folder, 8 I'm going to create a new folder and call this input. 9 Inside here, I'm going to create a new file 10 and call this Jenkins file, paste in our code, 11 and now, let's make some small changes.

12 Boolean param is now going to become string. 13 Now, if you've had a look at the link I've included, 14 you may see that there is text and there is string. 15 Now, what's the difference? 16 They both do the same thing except text supports multi-line. 17 Now, ideally we only want to get one word in, 18 so that's why we're going to use string. 19 We'll set the default value so we could say maybe 20 what environment is this going to deploy into?

21 So we'll start with, in double quotes, we'll put test, 22 and we'll say which environment 23 to deploy in. 24 Might have to be a bit careful calling it something like ENV 25 because that is actually used by Jenkins 26 for environment variables, 27 so instead we might call it deploy, 28 and then ENV. 29 So something like this and in camel case. 30 And we'll put it inside here. 31 String is set to, and it's the same thing again, params, 32 dot, and in this case, we said it's called deploy ENV.

33 Let's go ahead and copy the code. 34 Back over to our browser. Back in Jenkins. 35 Let's create a new item, 36 and we'll call this string pipeline. 37 Select pipeline, click okay, 38 and paste in our script. 39 Save that. 40 And again, we're going to have to click on Build Now. 41 Let's quickly check. Yes, it's picked up our default value. 42 Let's go back to dashboard, back to our pipeline, 43 and now, we can see build with parameters.

44 Let's click on that, 45 and now, you can see which environment to deploy in. 46 We're feeling brave, 47 so we're going to go ahead and deploy into PROD. 48 Let's build now. And there we go. 49 Let's check the output. And there we go. 50 We can see it's now set to PROD. 51 This is great for setting a custom variable 52 or something we need to type in, 53 maybe a build number or maybe a Git commit, 54 or even a branch we want to use 55 if we really need that fine-tuned customization.

56 But something like which environment to deploy into, 57 if someone doesn't know if it's PROD or PRD 58 or production, it'd be useful to have a dropdown, 59 and that's what we're looking to next.

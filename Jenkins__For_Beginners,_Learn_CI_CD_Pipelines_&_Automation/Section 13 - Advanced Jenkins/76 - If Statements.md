# If Statements

*Section: Advanced Jenkins*

1 Hi, and welcome to this lesson. 2 You're going to learn about if statements. 3 And I mentioned before in the challenge 4 that what we wanted to do 5 is have some sort of launch control button. 6 If you can imagine like in the submarines 7 where you have the two keys 8 and you both have to turn them at the same time 9 and then press the button, 10 same principle, 11 but with a boolean parameter to go ahead and deploy.

12 Now why this is useful, 13 you'll see this a lot when it comes to prod. 14 You may have multiple parameters you need to pass in. 15 And what you don't wanna do 16 is go ahead and deploy something 17 that could be a wrong setting 18 or something in there you want to fail safe. 19 So what I'm gonna do is show you two things. 20 One, how we implement an if statement, 21 but secondly, how we implement that logic 22 that you can then go ahead and use.

23 So what we'll do is we'll get started. 24 So inside our params folder, 25 we've got our boolean parameter we've set up. 26 So let's go ahead and copy the code. 27 And what I'm gonna do is create a new folder 28 and I'm gonna call it launch. 29 Makes it sound a bit fancy and something interesting. 30 We're gonna create a new file 31 and we're gonna call this Jenkinsfile. 32 Let's go ahead and paste our code.

33 And now let's go ahead and get started. 34 So we've got a new block we need to use, 35 and that is script. 36 Now, if we want to do anything with Groovy, 37 it needs to go inside this block. 38 Now I'm gonna come back to this statement very shortly. 39 So inside here, we want to create our if statement. 40 So if, then in brackets, 41 and then curly brace. 42 And inside what we want to do is say if params., 43 and we said our name is myBoolean, 44 so do myBoolean.

45 If it's equal to false, 46 and again, we use double equal signs here for comparison, 47 then what we want to do 48 is use this special Jenkins function, 49 which is currentBuild.result 50 = "SUCCESS". 51 And then we want to return. 52 Now what the return is gonna do 53 is it's going to stop the pipeline completely, 54 but as a nice touch, 55 what we can do is rather than them marking the job 56 as a failure, 57 we can mark it as a success 58 because it's not so much that the job has failed, 59 but rather we've not gone ahead and ticked the checkbox.

60 And again, we don't really want to pollute, 61 especially in prod, 62 people might start getting a bit panicked 63 when they start seeing that thunder cloud 64 because the job is failing. 65 And in reality, it turns out 66 that someone hasn't ticked a checkbox 67 to go ahead and deploy. 68 So this will cut off the job. 69 And optionally, what you might see is an else statement. 70 So if it's not set to false, 71 then go ahead and do this.

72 So what we'll do is we'll take this line here 73 and inside here, what we'll do is paste it in 74 and set equal to and put TRUE. 75 Now let's go ahead and copy this 76 and go over to Jenkins, new item, 77 and I'm gonna call this If Statement, 78 and we're gonna create a new pipeline. 79 Go ahead, paste it in, 80 and let's click Save. 81 Now as before, we're going to have to build now 82 to get the option of build with parameters, 83 but the default value is set to false, 84 so we'll still see some sort of success.

85 Now if we go Back to Dashboard, 86 back to If Statement, 87 and now let's Build with Parameters. 88 So we'll do it as false. 89 As you can see, it worked. 90 Now let's build it again, 91 but let's tick it so it's enabled to true. 92 Awesome. 93 And now if we have a look inside, 94 we can now see boolean is set to TRUE. 95 So that's how we use if statements in Jenkins. 96 And again, nice little feature you've got there.

97 You can now set this as a launch control parameter, 98 as I would call it. 99 So now if you want to go ahead and deploy to prod, 100 you'd have all your different options 101 and you'd have something like here, 102 confirm deployment, 103 and you would tick that and then build 104 and it will not continue with the rest of the pipeline 105 until that is enabled. 106 So there we go, you've now learned about if statements, 107 and they are so powerful 108 and you can really leverage them to your needs.

109 Up next, let's have a look at functions.

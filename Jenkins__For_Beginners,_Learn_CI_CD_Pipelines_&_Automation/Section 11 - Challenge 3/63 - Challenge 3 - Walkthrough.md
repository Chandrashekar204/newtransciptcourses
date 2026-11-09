# Challenge 3 - Walkthrough

*Section: Challenge 3*

1 How did you get on with the challenge? 2 Were you able to complete it? 3 Let's go through how to do it. 4 So we'll start with a pipeline. 5 Let's click on New Item. 6 Select Pipeline, 7 and this is called challenge3. 8 Let's click OK. 9 And we can keep this open 10 because what I'm going to do 11 is create the code in Visual Studio Code. 12 So we're gonna create a new folder, challenge3. 13 Right-click, New File, 14 and we'll call this Jenkinsfile.

15 So as before, we have our pipeline block. 16 Set the agent to any, 17 and now we have our parameters. 18 So let's work in order. 19 We'll start with the first one, 20 which is a string. 21 Set the default value. 22 Now I didn't mention what this was, 23 and we could leave it blank, 24 which is what we're gonna do here. 25 We're going to set it to a blank string. 26 Next, we're gonna set the description, 27 and we're gonna set the description to Deployment Name.

28 And lastly, we have to give it a name, 29 so we'll call this deploymentName. 30 Okay, that's the string set up. 31 Next, we've got our dropdown. 32 So I'm gonna set the choice, 33 and we're gonna set choices. 34 So with our choices, 35 we're gonna put them in square brackets. 36 Inside there, double quotes, 37 and to put in our Availability Zone, 38 so EU-WEST-2A. 39 Now I'm gonna copy this, 40 put it in a comma, 41 and do so again, 42 and let's change these out.

43 So we'll do 2C, and we'll set it with 2B. 44 Again, we don't need to set a default value 45 because that value is going to be EU-WEST-2A. 46 Next, we'll set a description, 47 and this will be What AZ or Availability Zone. 48 And then we need to give it a name. 49 So we'll call this azDeploy. 50 And lastly, we have our checkbox. 51 So that's gonna be booleanParam. 52 Default value, 53 we're gonna set it to false.

54 In the challenge, 55 we said what we want to do is have this like a fail safe. 56 So if you ever see those movies 57 where you have to turn the two keys 58 and you have to lift the flap 59 and then press the button, 60 that's kind of the same principle we're looking for here. 61 So this would be, 62 you could set the deployment name, 63 you could pick your AZ, 64 but it won't deploy until you click this checkbox.

65 Now we haven't actually covered yet 66 the logic to implement that, 67 and that wasn't part of the challenge. 68 The key goal here was to set up the parameter, 69 because what we'll do very shortly in the next section 70 is look at how we set that logic up. 71 So now we have the description, 72 and we could set this to CONFIRM DEPLOYMENT, 73 and we'll put that in caps, 74 make it really obvious.

75 And next, we're gonna set the name 76 to confirmDeploy. 77 So we can now set up our three parameters. 78 So the string has got a default value of empty, 79 but that technically still is a valid string. 80 We've got our choices. 81 These are our Availability Zones. 82 And lastly, we've got our Boolean parameter, 83 so our checkbox, 84 and it's set to false. 85 And now what I'm going to add as an additional step 86 is to verify this works.

87 So what I'm gonna do is add stages, stage, 88 and we'll call this Deploy. 89 Then we'll add steps. 90 And in here, I'm going to add a few echo statements, 91 String set to, 92 and we can use our interpolation. 93 And we said it's called deploymentName. 94 And something we might optionally want to use 95 is /n on the end, 96 which represents a new line, 97 because sometimes what can happen 98 is with all these echo statements, 99 it could bunch them up onto a single line.

100 So now we'll set choice set to, 101 and let's confirm the name of that, azDeploy. 102 And we'll set this one. 103 We'll call it bool. 104 And we'll get the variable name, 105 which is confirmDeploy. 106 So now let's copy our code back to our browser. 107 And inside our pipeline, 108 let's paste it. 109 And a quick word of warning here, 110 the first time you run this, it may fail, 111 and that's because it's not happy about the empty string.

112 Now let's go ahead and save it. 113 We'll Build Now. 114 And as you can see, 115 we get this very angry red error message, 116 "No such property: deploymentName." 117 That's because we haven't set it yet. 118 So now we go back to our dashboard, 119 click Build with Parameters, 120 and this time, it's going to work. 121 If I were to leave it blank, 122 you will see that it will now pick up this empty string.

123 Now we're getting green. 124 And as you can see here, 125 the string is empty. 126 It's picked up our first option from the choices, 127 and the Boolean is set to false. 128 Now let's go ahead and build with parameters again. 129 So our deploymentName, 130 will call this challenge3. 131 We want to deploy to EU-WEST-2B, 132 and we want to confirm. 133 We want to go ahead and deploy. 134 So now let's Build.

135 Awesome. 136 Now let's check. 137 It's picked up our name. 138 It's set up our Availability Zone, 139 and it's picked up that it's true. 140 There we go. 141 That's how you complete the challenge. 142 So now you've got 143 some real hands-on experience setting up parameters. 144 Up next, we're going to have a look at variables. 145 I look forward to seeing you shortly.

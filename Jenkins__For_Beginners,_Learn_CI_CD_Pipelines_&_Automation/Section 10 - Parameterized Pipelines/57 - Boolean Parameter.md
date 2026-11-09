# Boolean Parameter

*Section: Parameterized Pipelines*

1 Let's get started with the first option, 2 which is a boolean parameter. 3 So first, let's go ahead and set up our folder. 4 I'm going to call this "params," short four parameters. 5 Inside I'm going to create another folder, 6 and I'm going to call this "boolean." 7 For those not familiar with programming, 8 boolean is simply a variable that can be set 9 to either true or false. 10 And inside here, I'm going to create a new file 11 called Jenkinsfile.

12 Same as before, we start out with our pipeline template. 13 Inside, we set our agent, 14 and we're going to set this to "any." 15 Next, what we're going to add 16 is something called "parameters." 17 These go in curly braces. 18 And again, we can have multiple ones in here, 19 but we're going to start with boolean. 20 And what we're going to do is effectively use this 21 as our template, but set up the different types 22 of parameters we can pass in.

23 Underneath it we've then set our stages. 24 Add in our stage. 25 We'll call this "Demo," add our curly braces, 26 then our steps. 27 And we'll come back to this very shortly 28 because we're interested in our parameter. 29 So to use a boolean, it's "booleanParam." 30 And then inside our brackets we set some options. 31 First one is "defaultValue." 32 So that it's not blank, you could set this to true or false.

33 Basically, do you want it enabled or not? 34 Usually good practice is to set it to "false." 35 But on the flip side, if it's something we don't want 36 disabled, then we could set it to "true." 37 Then with a comma, we can add in a description. 38 And this is a line of text presented with our checkbox. 39 And as the name implies, it gives it a description. 40 Quickly minimize this. 41 More we might put in here is something 42 like "Enable service." 43 And like a variable, we need to give it a name.

44 So we do that name in double quotes 45 and we'll call it "myBoolean." 46 And you may be wondering here at this point 47 why we have things like this, lowercase and then uppercase. 48 Lowercase, uppercase, and again, lowercase, uppercase. 49 This is called camel case, and it's the preferred style 50 and part of the coding best practices 51 for when it comes to Jenkins. 52 So now we've got this set in our steps.

53 Let's get the value. 54 So we'll type in "echo." 55 And we'll enter the text saying "booleanParam is set to," 56 put a colon, and this is called string interpolation. 57 So we're going to put dollar, curly brace, curly brace. 58 And what this does is, when we go ahead and run this step, 59 it's going to display this line. 60 And whatever we put inside, in this case, 61 it's going to be this value from booleanParameter, 62 it's going to replace the dollar sign and the curly braces 63 and the variable name we put inside, 64 and instead it's going to display the value.

65 So interpolation is a fancy way of saying replacing. 66 So to use our parameter, we do so like this. 67 params, dot, and the name of the variable. 68 This case, we called it myBoolean. 69 And be careful with the camel case 70 because this is an easy way to get caught out. 71 And also check the spelling. 72 I often joke on my courses that to be very careful with it, 73 and it's been a few times I've been caught out myself 74 because I've misnamed something 75 or I've used an uppercase lowercase.

76 So just keep an eye on it, especially here 77 when we're using things like boolean, 78 which is quite an unusual spelling. 79 But this all looks good to me, so I'm going to save that, 80 copy it, and then go back over to my browser. 81 Let's click on New Item. 82 Pipeline. 83 And I'm going to call this "boolPipeline." 84 I'm putting the name in camel case, but that's optional. 85 Next click on Okay.

86 Come down here, down to our pipeline, 87 and paste in our Jenkins file. 88 Now what we want to do is click Save. 89 Now what we'd expect to see here is something 90 that says, "Build with parameters." 91 Now normally if we're pulling this in with GitHub, 92 Jenkins would pick it up automatically. 93 Now this is going to work because we set a default value, 94 so it's not going to error out, 95 but no value has been presented.

96 So what we want to do now is click Build Now. 97 It has executed. 98 Now if we click on the logs, we can see it's set to false. 99 Now this isn't great because we haven't seen 100 how to build with parameters. 101 So let's go back to dashboard, back on our job, 102 and now we can see Build With Parameters. 103 Jenkins has now picked this up. 104 So if we click on Configure, 105 we can now see we have a boolean parameter added.

106 It's a bit unusual, but it hasn't picked up the default 107 value, but that is set. 108 And we can see that if we now click on Save, 109 and now click on Build With Parameters. 110 And this is what we expect to see. 111 Now normally we might give this a different name, 112 so this might be a service. 113 So this could be something like Kubernetes 114 and you might say "Deploy with Ingress" 115 and a variable name could be set to ingress.

116 But see the description down here, Enable Service. 117 Now we can check it or enable it and click on Build. 118 Awesome. 119 Now let's check out the output. 120 We can now see it set to true. 121 Next up, let's have a look at how we can get user input.

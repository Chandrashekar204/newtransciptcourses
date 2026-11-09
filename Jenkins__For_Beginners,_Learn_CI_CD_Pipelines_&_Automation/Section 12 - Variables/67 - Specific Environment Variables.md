# Specific Environment Variables

*Section: Variables*

1 Hi, and welcome to this lesson. 2 What we're gonna be having a look at now 3 is Jenkins' specific environment variables. 4 I'll include a link to this page because it has a list 5 of the environment variables available, 6 and probably one of the most common ones you'll ever see 7 and probably use is this one here, which is build number. 8 So like an environment variable in Linux 9 that's available everywhere, 10 it's exactly the same with Jenkins.

11 So instead of us defining it, 12 it's automatically available. 13 We're also very nice and we give us a nice little demo. 14 So let's go ahead and set up our own with build number. 15 What we'll do is we'll go ahead, copy this, 16 and, again, I'll include a link if you want to follow along. 17 What we'll do is we'll get back to Jenkins, new item, 18 and we'll type in envPipeline. 19 (keyboard clicks) 20 Create a new pipeline, click Okay, 21 scroll down, let's paste it in, 22 and what we'll do is we'll swap this out.

23 So let's get rid of that. 24 And we said it's gonna be _BUILD_NUMBER. 25 Close up that curly brace, 26 and let's swap out running 27 and we'll say Build Number 28 and we'll set that equal like this. 29 So why is this so useful? 30 Well, especially when it comes to build numbers, 31 if you have Docker, 32 rather than you automatically trying to increment 33 or worst of all, setting latest, 34 which you should never be doing, especially in prod, 35 using build number, you can set that as a tag.

36 So with Docker, you'll have your repository URL 37 as part of a name when you have the application name 38 and that tag can be the build number. 39 And as you see here with the string interpolation, 40 you can use that as part of setting 41 either the variable or using it in the code 42 where you're setting the tag. 43 And just to show a quick demo of that, 44 you might see something like ecr.com 45 or whatever your registry is, 46 and you might have something like webserver, 47 and then you put a code on 48 and you would do something like this.

49 So you'd probably have a line, 50 something similar to sh docker image tag or build, 51 (keyboard clicks) 52 and it would look something like that. 53 So now, it automatically puts in the build number. 54 That was a bit of a tangent, 55 but also very useful to know. 56 So now, let's go back. 57 Again, if you're not familiar with Docker, 58 go ahead and check out the Docker course. 59 And now, let's go ahead and run this.

60 Select Save and let's build. 61 Let's check the logs, build number one. 62 Let's run build now. 63 So go run it a few more times. 64 Here we are, build number 10. 65 There we go, build number 10. 66 So now, it also increments for us. 67 Well worth having a look through here, 68 but I'm gonna tell you now, 69 build number is probably the most common one 70 you're ever going to use. 71 And with that, we wrap up the entire variable section.

72 Like I said, it really is that fast. 73 Now, you've learned a lot about variables, 74 let's jump into the advanced section next. 75 I look forward to seeing you there.

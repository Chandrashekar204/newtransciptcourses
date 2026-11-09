# Jenkinsfile Name

*Section: Advanced Jenkins*

1 A concept I'm going to cover 2 is Jenkins files with different names. 3 Now, throughout the course, we've been creating folders 4 to try and get around this by creating a file 5 called Jenkins file. 6 Now, there is a bit of a downside to this, 7 which I'm going to show you now. 8 If I go back over to VS Code, 9 we see we have this Jenkins file here. 10 Now, I can copy this, paste it, 11 and it's put the extension .1.

12 Now, sometimes what you might see 13 is if it's environment specific, 14 you might see something like this, 15 you might have prod.jenkins file. 16 And now we can see it's created for new file. 17 Now, if we have a quick look at the difference 18 between the two, we have Jenkins file like this, 19 it's colorful, it looks nice, 20 and then we have this one, perfectly valid, 21 it will still work, however, as we can see, 22 it's not as colorful and it looks a bit plain.

23 Unfortunately, at the time of writing this, 24 and look, even when I was a consultant, 25 I couldn't find a workaround for this 26 and my solution was really hacky. 27 So what we'd normally see was every different environment, 28 or maybe every different application, 29 so we'd have app one, app two, app three .jenkins file. 30 Some engineers I knew would work on it like this, 31 and look, I don't know about you, 32 but I'm so used to different colors 33 and getting used to the plugin as well 34 with the curly braces that I couldn't do it, 35 so all I used to do was rename the file and knock that out.

36 Now, it won't let me do it here 37 because I've already got a file called Jenkinsfile, 38 but that is how I would get around it 39 so that you can, again, see it all in color. 40 So you can go ahead and delete this, 41 because what we'll do next is I'll show you a demo 42 and show you that this does work. 43 And as we can see here, this is colorful, 44 this is what we want, 45 and let's say back in that example, we change it, 46 and then once we're done, we'd go ahead and rename it 47 to sort of something like prod.jenkins file again.

48 And that will go ahead and work. 49 So up next, let's have a demo of that working.

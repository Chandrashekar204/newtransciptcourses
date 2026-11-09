# Troubleshooting

*Section: Advanced Jenkins*

1 If you've been following along with a course, 2 you'll probably have this VAR pipeline set up. 3 If not, don't worry, just go ahead and watch. 4 So I'm gonna click on that, 5 and as we've seen, we can normally replay a job. 6 Now, if we go to job number two, 7 first warning sign here is you see replay. 8 No sign of a script, 9 but we've got this option here that says Run. 10 And now we can see we've got this page, 11 which doesn't look particularly good, does it?

12 We've got all this output 13 and there's not a lot we can really do. 14 And unfortunately, this puts us in a really bad position 15 because now we can't run replay. 16 We've then got to work out one of two things: 17 we can go back 18 and we can have a look for a successful build. 19 And normally this would be in the reverse order. 20 So normally you'd have successful, successful, then failure.

21 So you could then run replay on the successful one. 22 But the key thing to look at 23 is what change have you put in that has broken it? 24 And remember how I said check the curly braces? 25 That again is probably one of the number one reasons 26 you're seeing that error. 27 Other things include syntax error. 28 So normally one of the best things you can do is again, 29 if we do console output, 30 in this case, I made a bit of a mistake with the positioning 31 and it wasn't too happy about it.

32 But also here in the console output, 33 it's now told me why it was failing. 34 And if you're not sure, again, I highly recommend this, 35 and honestly, I don't think enough people do this at times, 36 is to have a look on Google, copy the error. 37 So at this point now, 38 we're trying to debug, 39 work out why and how it's not working. 40 My case here, I didn't put the variables in the right place.

41 It wasn't too happy about it. 42 And again, we can see this output 43 is giving me an indication, 44 but they're in the wrong place. 45 And if I go to replay, I get this horrendous error. 46 Now, if you're using something like Git, 47 you could always revert that previous commit 48 and then run your pipeline again. 49 But if you're doing it manually like we've been doing here, 50 probably not the best thing, 51 but again, go back to the successful build 52 and have a really close look 53 as to what change you put in that's breaking it.

54 And secondly, have a look at the console output 55 to try and work out where the issue is. 56 Usually it's again, the curly braces, 57 one of them missing. 58 It will throw off this huge error 59 and it's quite an annoying one, 60 but it's also one why I stress so much 61 that really do check it out.

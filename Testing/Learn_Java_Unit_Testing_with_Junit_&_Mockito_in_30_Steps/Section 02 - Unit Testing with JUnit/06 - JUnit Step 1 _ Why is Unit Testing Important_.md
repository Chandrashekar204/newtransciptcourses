# JUnit Step 1 : Why is Unit Testing Important?

*Section: Unit Testing with JUnit*

Instructor: What you're looking at on the screen is a simple method, truncateAInFirst2Positions. What this method does is if you pass any string to it, so I'm passing in AACD as an example string, so it checks the first two characters to see if any of them is A. if they're A's, then they're getting truncated. So, here, I have A's in first two positions, those are truncated and removed from the string and the output is CD.

If you consider this particular string, CDAA, this does not have A's in the first two positions, so there's no change. And, similarly, this particular thing, it has A in first position only, so that gets truncated and remaining string remains as it is. So, that's basically what this method does. I mean, in a typical application, there would be hundreds of methods like this doing some business logic or the other.

Let's say, this particular method is part of a large web application. So, you have a large web application where this method is being called from somewhere, and somewhere, let's say, this particular value is shown on the screen. So, the output, CD, is shown on the screen somewhere, let's say that's the fifth screen in a web application, I want to check whether this is working fine or not. The traditional way of doing that is this Java file would be part of a big web application.

So, I would build a wire, deploy it to a web server, and then navigate to the specific screen, and check whether the output is coming properly or not. That's the traditional way we used to do it. And, now, if I want to check whether the next test case is working, I would manually go there and check whether the output on the screen matches whatever I expect. Let's say, there's a small change in logic.

So, now, instead of this, I found that there's a defect, and I'm making a change in the logic. Now, to test these scenarios again, I have to go through the steps, all of the steps that we discussed until now, again, manually. And that's where the unit testing comes in. Unit testing tries to address this problem. So, when we write some business logic in a method, in a unit, we try to test the unit on its own.

So, this particular thing is a unit. I would pass in AACD and check whether the output is CD, I would pass in CDAA and check whether the output is CDAA. So, I would test this unit on its own. And that's one of the most important concepts of unit testing. So, in unit testing, you try and test a specific unit. The unit can be a single method, a group of methods, or it can also be a set of classes. Typically, in most scenarios, when we talk about unit testing, we would be talking about testing a method or a specific group of methods.

The advantage of unit testing is that once I write a unit test for this particular method, I would be able to run the unit test automatically within milliseconds and check whether all the test conditions for that particular method are matching or not, or the right words would be, if all the test conditions for that particular method are passing or not. Now that we understood the need for unit testing, we would start with the first unit test in the next section.

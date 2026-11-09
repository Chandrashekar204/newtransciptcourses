# 16.2 — Call Stack

> Section 16: Recursion

So to understand recursion, it's important to understand the concept of the call stack, because every time we call something recursively, we're putting a new method on the call stack. And earlier in the course we actually created a data structure called a stack. And we said it was like a can of tennis balls. Well this analogy applies to a call stack as well. So if you have a method that is running, that's the method at the top of the call stack.

That's that top tennis ball. When it gets done running, it is only then that the next method can start running again until it finishes. And that's popped from the call stack. And then finally, that last method on the call stack can run and we remove that. So let's move this over to the side. And we're going to use this for our call stack. Let's say we call a method that's called method one, and all it does is print out a string that says one. What do we call this method?

It gets added to the call stack like this. Then we print out one. And then this method is done running and we pop it from the call stack. But let's bring this back and put it on the call stack and add a line to our method. We're going to have this method call method two. And when it calls method two it puts method two on the call stack. And all this is going to do is print out a string that says two. But before we print that out, we're going to have this method call method three, which will push method three onto the call stack.

And this method is going to print out a string that says three. Except we won't have this one call another method. Since method three is at the top of the call stack, it's the only method that can run right now. So we'll print out this string three. And now method three is done running. And we can pop that from the call stack. So now method two is the active method. Running. Method two was waiting for method three to be done and be popped from the call stack.

So it could move to this line of code and print out two. And that was the last thing that method two is going to do. So we can pop that from the call stack. So now you can see that method one is at the top of the call stack. That means method one is the method that is actively running. Method one was waiting for method two to finish running so it could go to this line. Print out one. And now we can pop that from the call stack. So notice that the order that we called our methods was one, two, three, but it printed out three, two, one.

And the reason for that is that's the order the methods came off of the call stack. So let's bring our three methods up like this. And then we'll look at all three of these and IntelliJ. There are the three methods that we just created there. And then of course, we have to have a main method that's down here. And the only thing the main method does is kick things off by calling method one. So instead of just running this, I'm going to do something a little different.

Right here next to method one I'm going to come over here next to this line number. And I'm going to click. And we get a red circle. And you can see this whole line is highlighted and red. Then I'm going to come up here to this button that says debug. If I hover over this it says debug main and I will click on this. So this has started running our code. And you can see on the call stack here we have main that is this main method. Then down here you can see this is highlighted.

The highlighted line is the line that is about to run. So the really important button here is this one right here. So I'm going to hover my mouse pointer here and it says step into. And clicking this button over and over will allow us to walk through all of this code line by line. So like I said, this highlighted line is the one about to run if I click this. You can see this has added method one to our call stack. And the highlighted line here shows that we're about to launch method two.

So if I click this again you can see this has added method two to our call stack. Our highlighted line here shows we're about to start method three. So I'll click on this again. And you can see that method three has been added to the call stack. So this line that's about to run here is going to print out the string three. So I'll click on this. And you can see this console tab here has this little yellow marker here. I'm going to click on the console.

And you can see it's printed out three. So I'm going to click back on the button on the left for the debugger. And keep walking through this. So this line here is showing that this method three is done running. And we're about to pop this from the call stack. So when I click the step into. You can see that removed method three from the call stack. Now we're about to print out two. I click the step into like this. And our console. Now says two. So I'll move back over here to the debugger and do the step into again.

And because this is at the end of method two where it's highlighted, that means that's going to pop method two off the call stack. And now method one, the only thing left for it to do is to print out one. I'll click on this again. And move over to this console, and you can see that that's where it's printed out, one to the console. And I'll move back to the debugger here. And that was the last thing that method one needed to do. So when I step into this again, it's going to pop method one off the call stack.

And now you can see down here that we're at that closing bracket for the main method, which means it's going to pop main off the call stack. Like that. And that runs all of our code. So like I said at the beginning of the video, to understand recursion, it's important to understand the call stack that each time the method is calling itself, it's creating a new instance of a method and adding that to the call stack. So we'll use an example where we're walking through the call stack with a recursive method in the next video.

But for now that is our overview of the call stack.

----------------------------------------

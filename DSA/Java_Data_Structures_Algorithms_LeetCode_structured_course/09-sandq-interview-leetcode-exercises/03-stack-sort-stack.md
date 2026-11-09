# 9.3 — Stack: Sort Stack

> Section 9: <> S&Q: Interview / LeetCode Exercises

So now we're going to learn how to do sort stack. So if we have a stack of numbers like this, we want to sort it where it ends up like this. So I'm going to put this back. And in order to do this we're going to have a second stack. And we're going to have a variable I'm going to call mine temp. So we'll take that top item from the first stack, pop it and set temp to be equal to that value. And if the second stack is empty we'll just push this onto that stack.

And then we do the same thing again where we pop from the first stack and put it in temp. So what we're going to want is to have the lowest numbers at the bottom of the second stack. So we're going to compare that value of one to the value of three in the second stack. And in order to do that we have a method called peek. And all that does is look at the value of the top item in the stack, and you will need to use that in your solution. And because three is greater than one, we're going to move this back to the other stack and put the one at the bottom.

So now we'll do the same thing again. Pop from the first stack put it in temp. But because three is greater than one we're going to add this to the stack. And then we go back and do this again. Four is greater than three. We'll add this to the stack. And then we'll move the two up here. And now we're going to use that same logic that we saw earlier. Four is greater than two. So we're going to put this on the other stack. Three is greater than two.

So we're going to put this one over here. And now finally we can add the two to this stack. And because temp is empty we can empty this other stack. And now our stack is sorted. And that is how we do sort stack.

----------------------------------------

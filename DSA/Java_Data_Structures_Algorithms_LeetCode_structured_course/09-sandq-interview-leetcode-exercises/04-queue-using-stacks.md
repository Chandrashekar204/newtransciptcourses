# 9.4 — Queue Using Stacks

> Section 9: <> S&Q: Interview / LeetCode Exercises

So now we're going to talk about implementing a queue with stacks. And I'm only going to have one video for the next two coding exercises. And you might be wondering how do we implement a queue with stacks. So remember a queue is first in first out. So if we add an item to the queue this is the first item in the queue. This will also be the first item removed. What we cannot do when we add the second item is do this because the nature of a stack is we don't have any way of getting to that one.

So I'm going to remove this. So in order to do enqueue, which is going to be the next coding exercise, you'll pop that one from the first stack and push it onto the second stack. Add the next item and then do this in reverse. And then to add a third item we're going to do this. Add the third item and move these back. That is how we enqueue these items. And then we'll do one more. Let's move all of these over to this stack. And then we'll add a fourth item.

And then move all of these back. That's how we enqueue the number four is by moving everything to the other stack and then pushing the four on. And then moving everything back. So that's what you need to do to write the code for enqueue. And then once you do this dequeue is very easy. Remember the first item that we added to our queue was the one. And then it was the two and the three and the four. Now I'll have students ask me if this is an efficient way of implementing a queue.

And I'm going to tell you that it is not. This is a very inefficient way of doing this, but it is a common interview question to see if you can implement a queue with stacks.


########################################

# 8.3 — Stack: Push

> Section 8: Stacks & Queues

So now we're going to create our push method. We'll bring up our stack like this. And push is going to look like this. So this is going to be very similar to Prepending an item to a linked list. So now let's start writing our code. We're going to call this push. The return type is void. And then we'll pass it a value. We'll use that value to create the node that we're going to push on to the stack like this. So the first situation we're going to code for is if the stack is empty.

So we'll say if the height is equal to zero that is this situation where top is equal to null. And then we'll say top equals new node like this. So the other situation we're going to code for is if the stack already has items in the stack. So we'll say else. And now let's build out this else statement. So the first thing we'll do is say new node dot next equals top. So that is new node dot next equals top which is going to make that arrow point to the same node that top is pointing to.

And then we'll say top equals new node. That moves that up there and adds that into our stack. So now let's add this into the rest of our code. And the only thing left to do is to increase the height by one. So we'll look at this code in a moment in IntelliJ. And when we do we're going to create this stack that just has one node in it. And then we'll push a new node onto this with a value of one. And then we'll do a print stack. And we should see a stack with values of one and two.

Okay. So let's flip over to IntelliJ and take a look at this. So there is our push method that we just created having been added to our stack class. So now I'm going to come up here to our main class that contains our main method. So this line here creates our new stack with one node with a value of two. And this line here will print out that stack. I will run this. And you can see that to begin with, we have a stack with that one item with a value of two.

So I'm going to come over here. And I'm going to paste in this line. And this is going to push a new node with a value of one onto the stack. And then we will run print stack again. And we should see one and two. So I'll run this. And you can see that we now have one and two. All right. So that is our method for push.

----------------------------------------

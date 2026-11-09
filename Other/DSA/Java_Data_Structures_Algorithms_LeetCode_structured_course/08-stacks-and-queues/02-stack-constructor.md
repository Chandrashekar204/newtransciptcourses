# 8.2 — Stack: Constructor

> Section 8: Stacks & Queues

So now let's build our constructor for our stack. In order to do this, the first thing we have to be able to build is a node. And this node is going to be just like what we saw before with value and next. So our node class is going to have these same variables that we saw before. And we're going to have the same constructor where we pass this a value. And we just say this dot value equals value where we pass this value to here we set this dot value equal to that.

And this dot value is this value up here. So now let's build our stack class. So in a linked list, we had a couple of pointers to nodes called head and tail. But in a stack these would be top and bottom. But as I mentioned in the last video, we don't need this bottom pointer. So I'm going to remove this. So in a linked list, we kept track of the length in a stack. We will call this height. So now let's start building our constructor for the stack.

And let's focus in just on this. So the first thing we'll do is create a node. We'll use that value that we passed the stack class. Pass it to the node class. And create this node. They will say top equals new node which points top at that node. And then we'll say the height is equal to one. Except visually. We should represent that node like this. So now let's go over to IntelliJ and look at all of this code that we just created. So there is our stack package that's the lowercase s.

And then we have our stack class. That's the uppercase S. I'm going to double click on this. And scroll to the top here. And this is all of the code that we just created to create the stack class. And then inside of it the node class. And we have our two class variables for stack up here top and height. And our constructor for stack is down here. And just like I did with our linked list classes, I'm going to scroll up here. I have created a few methods to be able to look and see what is going on with our code.

And those methods are called print stack, get top and get height. So now I want to come back over here to our package, and we're going to click on this main class here and open this. So with this line here, we're going to create a new stack called My Stack. And it will have a node with a value of four. And then down here we're going to run get top get height and print stack. And I'll run this. And we can see here that top is pointing to a node with the value of four.

The height is one. And then when we run print stack we get this one item returned. And that is our stack constructor.

----------------------------------------

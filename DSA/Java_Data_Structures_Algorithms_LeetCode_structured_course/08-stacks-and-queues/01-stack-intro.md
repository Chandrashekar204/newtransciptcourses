# 8.1 — Stack: Intro

> Section 8: Stacks & Queues

Now let's look at stacks. So my favorite analogy for a stack is a can of tennis balls. Let's go ahead and remove these and I'll add one back. This is pushing an item onto the stack. And then of course we can push a second one onto the stack. But the thing that makes a stack a stack. Is you can only get to the last item that you pushed onto the stack. That second tennis ball, as soon as you push that second one on, you can't get to the first one without first removing the second one.

And then when we push the third ball on, we can't get to the second one. The only one we can get to is the one that is on top. This is called LIFO. Last in, first out. So after we remove that third ball, it is only now that we can get to the second one and then we can get to the first one. So let's look at an example of where you might use a stack. Let's see. We have a web browser and we go to Facebook. And then after that we go to YouTube and then we go to Instagram and then we check our email.

What we have created to the right of this computer screen is a stack of all of the previous websites that we have visited. So when we hit the back button, we are popping an item off of the stack, and it is only by removing that item that we can hit the back button again and get to the next item, and so on. A common way of implementing a stack is with an array list. An array list works better than an array here, because we don't know how many items we're going to be adding to the stack, so it's better to have a dynamic data structure.

So technically we could use either end of the array list for adding and removing items. The only requirement for a stack is that we add and remove items from the same end. So if we do that at that end of the array list where I just did this, that is O of one for both adding and removing items. However, if we do this on the other end and we're going to remove this item because of all of the re-indexing we have to do, and also bringing that item back, we would have to re-index this to push something back onto the stack.

This ends up being O of N for adding and removing from the stack if we do it on that end. So if you use an ArrayList to implement your stack, you always want to do it on the end, not the beginning. Since stacks are usually represented vertically, you can think of it like this. This would be popping an item from the stack and pushing an item onto the stack. So another way to implement a stack that is common and it is the way we will implement it here is with a linked list.

And just like with an array list, you can add and remove items from either end as long as it's the same end. So in other words, your stack could look like this with the null terminated end at the bottom of the stack. Or it could look like this. So let's put this back as a linked list, and look at which one of those two is best from a big O perspective. So it is O of N to remove an item from this end and O of one to put this back on. It is actually better from a big O perspective to do it from the other end, because both removing and adding are O of one.

So when you're using a linked list for your stack, you always want it to look this way with a null terminated end at the bottom. So let's put this back this way. There are a couple of methods that we wrote for the linked list that we can leverage for our stack, and those linked list methods are remove first and prepend. Except with the stack. We're going to call that pop. And push. And then went the length list. We had head and tail. But since we represent a stack vertically, we're going to change these names to top and bottom.

But with a stack we never add or remove anything from the bottom. We do everything at the top, so we don't even need that bottom pointer. We can do this just. With top. And that is our quick introduction to stacks.

----------------------------------------

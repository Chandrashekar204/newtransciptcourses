# 10.5 — BST: Insert - Intro

> Section 10: Trees

So now let's look at what we would have to do to insert a node into a binary search tree. So I'm going to bring up a tree here. And we're going to insert this node. So you can look at this and see that this node is going to go right here. But what I want to do here is go through all the steps to figure out where that goes and then insert it. So in this video we're not going to have any code. We're just going to go through the steps. So the first thing that we need to do is create that new node.

So I'm going to put that over here on the left create new node. And then I'll add to this all of the steps that we're going to need to go through. So I'm going to move this over to the right. And what I want to simulate here is if you took a piece of paper and started writing out all of the steps, what would that process look like? So the next thing we need to do is compare that 27 node. To this root node, and we know if it's less than we go to the left, and if it's greater than we go to the right.

So let's add this to our notes on the left of the screen here. We'll say if it's less than we go left. Else it's greater than. And we go right. So in this situation we're going to go left. So now that we've made the decision on which way we're going to go, there are two possibilities. Either the spot to the left is open, in which case we'll just insert this node here or it's not open. And if it's not open, we need to move down to here and do that comparison again.

So let's add this to our notes. We'll say if it's null. In other words that spot is open. We will insert the new node. Else we'll move to the next node. So now that we're down to this 21 node, we'll do this again. If it's less than we go left, else if it's greater than we go right. In this case we're going to go to the right because 27 is greater than 21. Then we come down here. If that pointer to the right is null, insert the new node and we insert that there.

But one of the things that should jump out at you is that we did both of these lines here for this node. And then we came down and did it again with this node. This is an indication that these should be inside of a loop. Then we have to figure out is this a for loop or a while loop? Well, a for loop is great if you know how many steps you're going to iterate through something. But we don't know that here. So this is going to be a while loop. So now let's add a while loop to our notes.

Here. We'll put those if statements inside of this while loop. So another thing we're going to need is a variable to move through this tree. So we'll come up here this arrow we'll call it temp. And that is what is moving through this tree as we are iterating through this. So let's bring this back up here. When we initialize this variable we'll set it to be equal to root. And that needs to go above our while loop like this temp equals root. So I'll remove these and take our node that we're inserting and move this down here.

And we're going to look at a couple of edge cases. One of the edge cases is if we have an empty tree. If we have an empty tree we'll just set root to be equal to the new node. And if this happens, we're not going to need to declare the variable or go through the while loop. So this needs to go above where we declared the variable. So now let's bring our tree back like this. So these steps that we have on the left cover just about everything. But we do have one other edge case.

And to illustrate this, instead of inserting the number 27, I'm going to insert a node with the value of 76. So we'll take this node, compare it to the root, and then we go to the right. And this is where the problem is. We already have a 76 in our tree. And we can't insert a value that we already have in the binary search tree. So we're going to insert a line here that looks for duplicates. And we're going to put it right here. It has to go inside of the while loop because you are comparing the new node to every single node as you're moving through this to see if there's a duplicate.

So it has to go inside of the while loop. So these are all of the steps to insert a node into a binary search tree. And we're going to pick up right here in the next video and use all of these steps to help us code this. But for now, that's our introduction to insert.

----------------------------------------

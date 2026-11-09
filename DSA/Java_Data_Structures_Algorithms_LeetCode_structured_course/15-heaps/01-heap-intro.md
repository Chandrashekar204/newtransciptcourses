# 15.1 — Heap: Intro

> Section 15: Heaps

Welcome to heaps. And I'm going to bring up this heap. And if you've never seen a heap before, the thing that's probably jumping out at you is this looks a lot like a binary search tree, and a heap is a binary tree, but the numbers are laid out in a different way. In a heap, each node has a value that is greater than each of its descendants, and because of that, the maximum value is always going to be at the top. So this node also has a value that is greater than each of its descendants.

And you can see this one does as well. A key characteristic of a heap is this tree will always be complete. And we talked about what makes a tree complete and the binary search tree section. But I'm going to review it here. So I'm going to drop these nodes out. And then I'll bring these in one by one. So a complete tree fills from left to right without any gaps. So if I add this node here it remains complete. But if we skip a spot this is no longer complete.

So I'm going to put a node into this spot to make it complete again. And then I'll add one more to finish out this line. So one of the other things that makes a heap different than a binary search tree is that in a heap you can have duplicates. So for example that 72 node could be 99 and have the same value as its parent. I'm going to go ahead and put that back as a 72. So the particular type of heap we have here is called a max heap. That's where the maximum value is at the top.

But you could also have a min heap where the minimum value is at the top. And each of the descendants is greater than. I'm going to go ahead and put this back as a max heap. So other than the maximum value being at the top, there is no particular order to the other nodes. So for example, on the second line we could take these two nodes and switch them. And this is still a valid heap. So you can do it this way. Or you could do it this way. Also in this heap we have the second and third highest values on the second line.

But that doesn't necessarily have to be the case either. We could take these two nodes and swap them and it's still a valid heap. You just need each node to be greater than each of its descendants. So I'll go ahead and put these back. So the biggest difference of all between a heap and a binary search tree in this course will be how we implement it. We implement a heap with an array list, and we're not going to have a node class. All we're going to do is store integers in this array.

So the root goes in that first spot. And then we just go line by line. So in the second line we put this value here and this value here. And then we go to the next line. And then we add all of these values as well. So there are two common ways to store the heap. The first way is to do it the way we've done it here and use the index of zero. Another common way to do it is to leave that spot open and move everything to the right. And because it is common to see it both ways, I'm going to talk about both in this course.

So you can think about this tree as being like this, where you can take all of these values and just drop them in like this. So I'm going to put this back as a tree. And I want to emphasize what are the points I made earlier about this needing to be a complete tree. If the tree was not complete, that would mean that you would have a gap in these numbers and they have to be a contiguous set of numbers. So I'll go ahead and put that back. So now we're going to do a little bit of math.

If you wanted to find the children of this node, the way you do it is you say that the left child is equal to two times the parent index. In this case the parent index is one one times two is two, and then the right child is going to be at two times the parent index plus one. In this case that is going to be three. So now let's do that for a couple more of these. Let's find the children for this node. This is at the index of two. Two times two is four.

Then plus one is five. So now let's do one more. We'll find the children of this. This node. This is at the index of three. Three times two is six plus one is seven. So now that we know how to calculate the left and right child, let's look at the calculation for finding the parent. Let's find the parent of these two nodes. And the way we'll do this is by taking the index and doing integer division by two. So if we take six and divide it by two we get three.

And if we take seven and divide it by two we get 3.5. But because we're doing integer division, everything to the right of the decimal place gets dropped. And this becomes three. And the node at the index of three is the parent node. So we'll go ahead and put these back. And the next video we're going to talk high level how it is that we insert a node into the heap. But for now that is our introduction. On to heaps.

----------------------------------------

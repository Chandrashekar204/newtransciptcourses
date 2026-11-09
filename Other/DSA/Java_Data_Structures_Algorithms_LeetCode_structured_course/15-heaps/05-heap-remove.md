# 15.5 — Heap: Remove

> Section 15: Heaps

So in this video we're going to write the remove method. I'll start out by bringing up a heap like this. And with remove there is only one item we will ever remove from the heap. And it doesn't matter if this is a min heap or a max heap, we will only remove and return that top item. And once we do that, we need to rearrange these nodes where this once again becomes a valid heap. And the first step in doing that is we're going to make the tree complete.

If you were going to make this tree complete in one move by moving one node, what node would you move? Well, the only node you can move to make this tree complete in one step would be to move the node that's to the bottom right. So now that we've satisfied the first step of making this complete, now we need to move that 65 node into the appropriate location. And this is similar to what we did with insert. With insert we inserted something on the bottom right.

And then we bubbled it up with remove. We take the node from the bottom right, put it at the top, and then we sink it down. And the way we sink it down is we take that 65 node, compare it to each one of its children. We determine which child has the highest value and swap it with that child. And then we'll compare it to its child again. But in this case 65 is greater than 60. And when this happens, that means we have a valid heap. And we'll just stop right there.

So I'm going to bring up this ArrayList that represents this heap. And there are three situations we need to code for. We need to write code for when we have two or more items in the heap. And then we need to write code for when we have one item in the heap, and then also write code for when we have an empty heap. So we'll start our remove method out like this. It returns an integer. So the first situation we're going to code for is when we have an empty heap.

So if the heap size is zero we're going to return null. Then we'll write code for. When we have one item in the heap we'll say if the heap size is equal to one. So we want to do two things here. We want to not only return that value of 80 but also remove it from the heap. So we're going to say return heap dot remove at the index of zero. So the heap dot remove is going to remove this. But that return statement is also going to return it. So now we're going to write code for when we have two or more items in the heap.

And the first thing we'll do here is we'll say max value equals heap dot. Get at the index of zero. So that takes this value of 80 at the index of zero and sets max value to be equal to 80. And we will return that at the end of this method. So technically this number 80 at the index of zero is going to remain in the array list. But we know we're going to remove that and overwrite it. So I'm going to gray this out in the array list and in the tree.

So what we want to do next in the tree is move that bottom right node up to the top like this. In the array list. What we want to do is remove the last item and then move it down here and take that value and put it in at the index of zero. And we'll do that with this line of code, which removes the last item, and then sets the index of zero to be equal to that value. So now what we need to do is take this node with the value of 60 and sink this down in the tree to its appropriate location.

And we're going to do that with the helper method that we write in the next video. So what I'm going to do here is I'm just going to say sink down. We're going to pass it the index of zero. And it's this sink down method that's going to take that 60 node and sink it down into the tree to its appropriate spot in the array list. That's going to look like this. Now the only thing left to do is to return max value, that value of 80 that was at the top of the heap before we started this process.

And that is all of the code for the remove method. So we'll write the sink down method in the next video. But for now that is our method for remove.

----------------------------------------

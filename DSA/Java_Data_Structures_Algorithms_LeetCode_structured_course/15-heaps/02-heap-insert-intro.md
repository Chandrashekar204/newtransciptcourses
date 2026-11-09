# 15.2 — Heap: Insert (Intro)

> Section 15: Heaps

In this video, we're going to have an introduction to how it is. We insert something into a heap. So I'm going to bring up this heap. And what we're going to do is insert the value of 100. And if you look at this you can see that 100 is going to be the highest value, and it's going to end up at the top of the heap. But the question is where do we insert it to begin with, you might look at this and think that we should insert this at the top, but it doesn't matter what the value is.

We will always insert here, because the number one thing that we need to do with the heap is always keep it complete. So I'll go ahead and move this back over. And we do this by first comparing that 100 to its parent node. And because 100 is greater than 72 we will swap these two values. And then we will once again compare this to its parent. And because 100 is greater than 99 we will do this. Now this process of bubbling, this value up to the top is going to exist within a while loop.

And if it ever reaches the top of the heap, this will be one of the things that breaks this out of the while loop and lets us know that we now have a valid heap. Now let's try this again with a value of 75. We'll compare that 75 node to its parent. It is greater than. So we will swap these two. And now we will once again compare that node to its parent. But in this case the parent value is greater than. And this is the other situation that can break us out of our while loop.

And if we have this situation, we'll stop. And we know that we have a valid heap. So I'm going to take that 75 node and that 100 node, and I'm going to remove them and put the tree back the way it was. And I'm going to bring up the ArrayList that represents this heap. So when we add that node with a value of 100, what we're doing is adding that 100 to the end of the ArrayList. Then we're going to compare that 100 node to its parent. And we determine the parent by taking the index of five, dividing it by two.

But because this integer division this becomes two, we're comparing it to the value at the index of two, because it's greater than we need to do a swap in the tree. I'll do it like this. In the ArrayList it looks like this. So then we'll compare 100 against this parent again because it is greater than and the tree will do a swap that looks like this. And in the ArrayList we'll do a swap that looks like this. And because that 100 has reached the top of the heap, we're going to stop running the while loop.

And now we have a valid heap. So now let's insert 75 into our heap. We're going to take that new value and add it to the end. And then we'll compare it against its parent this 61 node. And we determine that by taking the index of six we divide it by two and get three. So we're comparing it to the value at the index of three because it's greater than we'll do a swap. And the tree that looks like this. But what is actually happening is in the ArrayList we're doing this.

So now we're going to take that 75 and compare it to its parent. Again the way we determine the parent is dividing three by two. But because this is integer division this becomes one. So we're comparing it against the value at the index of one. And because 75 is not greater than 100 we're going to stop right here. And we have a valid heap. Now so far we've been leaving this index of zero open. When I implement this, when we write the code I'm going to go ahead and use that index of zero.

But like I mentioned before, it is very common to leave that index open. That's why I wanted to show it this way as well. So in the next video, we're going to write some helper methods that will make our code a little simpler to write when we write our insert and remove methods. And then in the video after that, we'll write the code for inserting a value into the heap. But for now that is our introduction to insert.

----------------------------------------

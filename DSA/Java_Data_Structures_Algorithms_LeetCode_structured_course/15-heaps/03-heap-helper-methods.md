# 15.3 — Heap: Helper Methods

> Section 15: Heaps

So in this video we're going to write our constructor and a few helper methods. So I'll bring up this heap. And as I mentioned previously, when we write our code, instead of leaving this spot open, we're going to move everything over. So we're going to call our class heap. And we're going to have a list of integers that we call heap. When we implement this list in the constructor, we'll implement it as an array list. And we will also have a method called get heap that will return a copy of the heap.

So we'll say return new array list and pass this the heap. So this will be returning a copy of the heap. And the reason that we're going to return a copy is we don't want to give anyone access to the heap, because if they change a number it can make the heap invalid. So in addition to these we're going to have a method called left child. So when we had that index of zero open we said that the left child was two times the index. But because we are using this index of zero, this equation changes a little bit.

And we're going to return two times the index plus one. So I'm going to bring in a heap like this just so we can visualize this. So if we're looking at this node which is represented in the array list here two times zero is zero plus one is one. And that is indeed the left child. So now let's look at this node that's represented here at the index of two. Two times two is four plus one is five. And that is the left index. And for the right child it'll be similar to what we saw before.

The right child is one more than the left child. So we'll just say plus two instead of plus one. Previously we saw that the parent was the index divided by two with integer division. This will be the index minus one divided by two with integer division. And then we'll have one more helper method. This will be called swap. And this just takes the values at two indexes and swaps them in the array list. In the next video, we'll write the code for inserting an item into the heap.

But for now these are the heap helper methods.

----------------------------------------

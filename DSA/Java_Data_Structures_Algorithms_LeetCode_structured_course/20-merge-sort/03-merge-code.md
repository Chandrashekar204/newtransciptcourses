# 20.3 — Merge: Code

> Section 20: Merge Sort

So now we're going to write the code for the merge helper method. So I'll start out by bringing up two sorted arrays like this. I'll shrink these down. So we have room for our code. And we'll start our method like this. So we're going to pass this two arrays array one and array two. And remember both of these arrays have to be sorted arrays. And the return type is an array of integers. So the array that we're going to return is going to be called combined.

And since it has to hold all of the values from both arrays, the length of it is going to be the length of array one plus the length of array two. So now we have a few other variables to create. The first one I'll call index. That'll be the index of the combined array. And then we have I. We'll use that to iterate through this array. And then we'll have J that we'll use to iterate through this array. So now we can create our first while loop in this method.

And this is going to run until one of the arrays is empty. So this is testing to see if the first array is empty. And this is testing to see if the second array is empty. If either of the arrays are empty, it will cause us to break out of this while loop. So we'll start out with an if statement that says if array one at the index of I is less than array two at the index of J. And that is the case here. Then we'll say in the combined array at the index of index, in this case zero.

We'll set that equal to array one at the index of I like that. Then we need to increment the index which moves that pointer over. And then we'll increment I which moves that over like that. So I'm going to move the while loop up like this. And in this next iteration of the while loop, the conditional in this if statement ends up being false, because now the item at the index of j in the second array is less than the item at the index of I in the first array.

So to deal with this situation, we'll say else. Then we're going to add into the combined array the item in array two at the index of j just like that. And then once again we need to increment index. Move that pointer over. And we have to say j plus plus to move that j over. So now we can just keep running through this while loop. And what I'm going to do is I'm going to do all three steps at once. I'm going to move that three up, but I'm also going to move both of the pointers over at the same time, and do that for the next item and the next item and the next item.

So this while loop is only going to run until one of these arrays is empty. And now that the second array is empty, that will break us out of this loop. But we still have items in the first array. So to deal with that I'm going to remove this code. And we're going to start another while loop that will only loop through array one. So we'll say while I is less than array one dot length. In other words, while array one still has items in it. Then we'll add to the combined array array one at the index of I which moves that item up.

And then we need to increment index. Then we'll increment I, which moves that arrow over. So now we'll run through this while loop again. And now that array is empty. And that'll break us out of this while loop. So in this situation we emptied the second array first, and then we had to run through the remaining items in the first array. You can have the opposite situation as well, where we run through the first array and still have items in the second array.

And for that situation we'll create this while loop, which is almost identical to the one right above it, except we're running through the second array if that still has items in it. Now the only thing left to do is to return this combined array. So now let's take a look at this in with the rest of our code like this. And this is our entire merge method. That'll take two sorted arrays and combine them into one sorted array. So now let's flip over to intelligence and take a look at this.

So all of this code is contained in our merge sort class. And then I'll scroll up here. And this is the merge method that we just created. And I'll scroll up yet again. I've created a ray one and a ray two, and these are identical to what we just saw in the diagram. So down here we have a long line of code. But all we're doing is printing out the array that the merge method returns. And I'll run this and you can see this returns a sorted array one through eight.

And that is our method for merge.

----------------------------------------

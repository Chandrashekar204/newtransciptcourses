# 19.6 — Insertion Sort: Code

> Section 19: Basic Sorts

So now we're going to write our code for insertion sort. We'll pick up where we left off in the last video with this array. And I'll move this down to the bottom. And then we'll start writing our code. We'll call this insertion sort. We'll pass it an array of integers that we call array. And the return type will be void. So we'll start this out with a for loop. So with most of our for loops we've seen we've set I equal to zero. But in this case we're going to start with the second item in the array which has an index of one.

Then we're going to store that value in a variable called temp. So temp will be set equal to array at the index of I. So for this first iteration temp is going to be equal to two. So we're going to have another variable called J that points to the previous item. We'll do that like this j equals I minus one. So what I'm going to do is put this back and I'm going to skip down to here because all of the items are in order until we get to here. And then we'll point J at that previous item and we'll go into our while loop.

So we'll say while temp is less than array at the index of j. And this is j here that for and temp is this item. So this conditional is true. We'll say array at j plus one equals the value that's at array at the index of j. So what that does is just move that four over. So the next thing we need to do is move that three into this spot. We'll do that by saying array at the index of j is equal to temp. And then we need to move j over. And we'll do that by saying j minus minus.

Then we'll run the while loop again. But in this case temp is not less than array at the index of j. So we'll just put that right there. So there is an edge case that we have to deal with. And in order to explain that I'm going to take the first two items in the array and I'm going to switch them. So we'll set temp to be equal to one. And then j will be the index of the item before this. So we'll go into our while loop. And we'll say while temp is less than array at the index of j.

And that is the case here. And they will run this line here, which moves that two over, and then we'll run this line which moves this over. But the problem happens when we say j minus minus. And the problem is when we move j over, it's now pointing to the index of negative one, which of course does not exist. So we need to add something to our while loop. So we have to add this part here. J has to be greater than negative one. So one of the things that's very important when you write this conditional is these two things have to be written in the right order.

So I'm going to take these I'm going to switch these. If we do it like this, we're going to be looking for a ray at the index of negative one, and we're going to get an error. So we have to check to see if J is greater than negative one first. So it is very important that this order is correct. And now that deals with our edge case. So now that runs correctly. And we can drop that right there. And that is all of our code for insertion sort. We'll look at this code in a moment in IntelliJ.

And when we do, we'll start with an array that looks like this. And then we'll run insertion sort on that and then we'll print it out. And we would expect that array to be sorted. So now let's flip over to IntelliJ and take a look at this. So there is our insertion sort method there. And I'll scroll up. And in our main method we'll start by creating that array that we just saw. And then we'll run insertion sort on the array with this line here. And then we'll print that out and I'll run this.

And you can see that we now have a sorted array with one through six. And that is our method for insertion sort.

----------------------------------------

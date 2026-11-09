# 19.4 — Selection Sort: Code

> Section 19: Basic Sorts

So now we're going to code selection sort. We'll pick up where we left off in the last video with this array. And we'll shrink that down into the corner like that. And then we'll jump right into writing the code. So we're going to call this selection sort. And we'll pass it an array that we're just going to call array. And the first thing we're going to do is create a for loop that starts at the index of zero and goes through the length of the array.

So let's take a look at that variable I from the for loop. That's going to be this item here. And this is what we initialize min index with that index of zero. So min index needs to be equal to I. So let's add this in with the rest of our code min index is going to be an int. And we'll set it equal to I from the for loop. And once we do that we'll create another for loop that compares that to the rest of the items in the array. So notice that we start this at I plus one.

So our first time through this this index is going to be I. And then J will be I plus one. So we're going to start out with min index being equal to I, which in this case is the index of zero. But if the value at the index of j is ever less than the value at the index of I, we're going to replace that with J. So let's add this in with the rest of our code. We'll bring this back. But we only want to set min index to be equal to j. If the item at the index of j is less than the item at the index of min index.

If that is the case, then we'll set min index to be equal to J. So let's enlarge our array here and then we'll walk through this to the end. Min index is now equal to one. And then we move j across like this until we get to a value that's less than the value at min index. And that is the case here. So we'll set min index to be equal to j again here which in this case is the index of four. And then we run through this to the end of the array. So now we know the index that contains the minimum value.

It's at the index of four. So now we can swap these items. And that will mean the item at the index of zero is now sorted. So I'll color that in green. But we have to write the code to swap these two items. So let's bring back our code like this. We'll use these three lines here to swap those two items. And I'm not going to walk through these three lines here because we did something very similar to this. And the bubble sort coding video. But these three lines will swap the values in those two indexes.

But now I'm going to bring this back up and talk about another scenario that we should code for. So now we're going to run through that second for loop again. So now I is equal to one. And then J is this next item over here. So we start out with min index being equal to I which in this case is the index of one. But you can just look at this and see as we move j through the array there are no items that are less than two. So we're going to move this all the way through.

And we're not going to change min index. So if min index is equal to the same index that I is equal to, that means we don't need to do a swap. Now that does mean that the item at the index of one is sorted. So I'll go ahead and color that in green. But our three lines of code that we use for swapping items does not need to be run here. So we'll create an if statement that says if I is not equal to min index only then do we run these three lines of code.

So let's bring in the rest of our code like this. And this is the entire selection sort method. So if we keep running through these for loops, we'll end up with an array that looks like this. So we'll look at this code in a moment in IntelliJ. And when we do we'll start with an array that looks like this. And then we'll run selection sort. And that should sort that array. So now let's flip over to IntelliJ and take a look at this. So I call this class selection sort.

And this is our selection sort method that we just created here. Then I'm going to scroll up here. And that is our main method. And with this line we're going to create that array that we just saw in the diagram. And then we'll run selection sort on that array. And then with this line we'll return the sorted array. And I'll run this. And you can see up here that the array is sorted one through six. And that is our method for selection sort.

----------------------------------------

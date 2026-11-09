# 19.3 — Selection Sort: Intro

> Section 19: Basic Sorts

So in this video we're going to walk through the steps for selection sort. And then in the next video we will code this. So I'll start out by bringing up our array that will represent like this. But with selection sort we're also going to need the indexes. So I'll go ahead and bring those up. So with selection sort we start with this first item. And what we're going to do is we're going to look for the index that contains the lowest value. So this is the only one we've looked at so far.

So we're going to have a variable called min index. And we're going to set it to zero. So I want to emphasize that this variable does not hold the value of four. It holds the index of zero. So then what we'll have is a loop where we start with the next item and say is the value of this item less than the one at the index of zero. And in this case it is. So we're going to set min index to be equal to one. Then we'll look at the next item. This one is not less than.

So we won't do anything there or there. But when we get to this value this one is lower. So we'll update min index to be equal to four. Then we'll continue through the end of the array. And once we've finished looping through, we know that our min index is at the index of four. So now what we're going to do is take these two items and swap them. And when we do that one is sorted. So I'll color that in green. And then we'll start the process again with the next item.

We'll set min index equal to one. And then we'll have a loop that loops through the rest of the array. And you can tell by looking at this that the two is the lowest item. So this is a different situation. We're not going to have a swap. And that's something we'll talk about when we code this. How do we handle the situation when we don't need to do a swap. But we are going to loop through this like this. And when we get to the end min index is equal to one.

And that means that item is sorted. So let's do this for the six and min index is two. And I'm going to move this variable over because we're going to run out of room over there in a moment. But we compare it to the five. Now that's the lowest then the four that's the lowest and the three. And now that item is the lowest. And now that we've run to the end, we know that the min index is that the index of five. And we'll swap these. And now that three is sorted.

So now we just have a couple more times to run through this. So we'll just take the five min index. Is that the index of three. That next item is lower. So we'll update min index. And now we know min index is at the index of four. We swap these. The four is sorted. And we'll do this one more time where we compare the five at the index of four to the six. And these don't need to be swapped. So these are both sorted. So we'll code this in the next video.

And when we do we'll kick off that video with an array that looks like this. And then we'll write the code to sort that. But for now that is our overview of selection sort.

----------------------------------------

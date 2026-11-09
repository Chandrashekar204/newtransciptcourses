# 19.7 — Insertion Sort: Big O

> Section 19: Basic Sorts

So now let's look at the big O of insertion sort. And obviously we had a loop within a loop. So that's going to be O of n squared as our worst possible scenario. But our best possible scenario is when we have sorted or almost sorted data. So let's bring up our list that is almost sorted that we saw in the last couple of videos. And let's look at the number of operations to sort this. So let's look at this item here because it is already greater than the item before.

It's not going to run that second loop that compares it to all the items before it. That one just gets left in place. Same is true with this one. This item is less than the item before it. We'll move that over and drop that in. And then for the rest of this list we're going to go through it linearly. So if you have already sorted or almost sorted data, the time complexity for this is going to be n not n squared. And you have to take that into consideration when you're looking at insertion sort.

Big O.


########################################

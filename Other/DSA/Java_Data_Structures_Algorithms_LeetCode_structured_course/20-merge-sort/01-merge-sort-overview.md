# 20.1 — Merge Sort: Overview

> Section 20: Merge Sort

Now let's do merge sort. So the idea behind merge sort is this if you have two sorted lists and these are both sorted, it is very easy to combine these into a new sorted list. So let's say we started with a list with eight items unsorted like this. What merge sort is going to do is first, break this list in half and break it in half again and break it in half again, until the only thing that we have left are lists that only have one item in them.

So there will be eight separate lists with one item in each list, and a list with one item in. It is by definition sorted. So now that you've gotten these all down to single item lists, we can take two of the items. And create a new list that's sorted, and we'll do that with the next two. And so on until we have four lists, in this case with two items each. Then we'll do it again with these two lists like that. And with those two lists. And now we can take these two lists and combine them into one sorted list.

And that is our high level overview of merge sort.

----------------------------------------

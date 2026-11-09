# 20.6 — Merge Sort: Big O

> Section 20: Merge Sort

Now let's look at the big O of merge sort. Let's bring up a list here. And the first thing I'm going to talk about is space complexity. So with Merge Sort you start out with this original list. Then you create two new lists called left and right. And then you continue breaking these down. So you start out with your original list. And then you have eight new lists that each have a length of one. So the number of items being stored in memory have been doubled.

So that means this is O of N for space complexity. The previous sorting algorithms that we've looked at are sorted in place. That means we take the original list and we move things around inside of that list. Merge sort is different than that in that it creates new lists. So let's put this back up here and look at time complexity. When we're breaking this in half, we do this in one, two, three steps. We had eight items. It took us three steps. This is going to be log in because two to the third power is eight.

It took us three steps to break this in half with eight items. But let's look at what happens when we put these together like this. So think back to our merge function. Our helper function. It had those while loops in there that went through each number one by one to be able to combine these into a sorted list. So breaking these apart is O of log n, putting it back together because of having to loop through each item with the merge function is o of n, and so that's where we get the o of n times log n time complexity for merge sort.

So let's look at this on the graph. And when it comes to sorting algorithms, only the two on the left really matter. I'm going to gray out the ones on the right. The first three sorting algorithms that we created were O of n squared, bubble sort, insertion sort, selection sort. But this one is much more efficient O of n times log n o of n times. Log n is the most efficient that you can make a sorting algorithm that's going to sort multiple types of data.

There are certain efficiencies and sorting only numbers, and there are some sorting algorithms that can run more efficient than this. But you can only sort numbers with them. But if you're going to sort multiple types of data, this is as good as it gets. So o of n times log n is much more efficient than O of n squared. And it may not look that way on this graph, but the axis on the left, the y axis only goes up to 75. If the axis went to a thousand or it went to a million, you would see that there is a huge difference between O of n squared and O of n times log n, and that is our overview of merge sort.

Big O.


########################################

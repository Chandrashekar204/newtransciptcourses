# 21.5 — Quick Sort: Big O

> Section 21: Quick Sort

Now let's look at quicksort. Big O. Let's bring up our list here. So the first step with quicksort is to run pivot. When we run pivot our list ends up looking like this. And if you'll recall in the pivot function we had a for loop that went all the way through the list. Looking at each item, that process of running pivot is going to be o of n. But the recursive part. We've done one step here. Here's two steps and three steps. So let's say we have approximately eight items here.

And we did this in three steps. Two to the third power is eight. We've seen this before. That's O of log n. So quicksort is O of n times log n, just like merge sort. And on the graph that is much more efficient. Then O of n squared. But the n times log n for quicksort is actually just for the best case and the average case. The worst case is not n times log n. So let's take a look at that. Our worst case is if we already have sorted data. So we start out with our pivot point being that one, we're not going to move anything else in the graph, and that one is going to be sorted.

And normally we run quicksort on everything on the left and everything on the right. But we only have items on the right. So we're going to run pivot on everything else. Again. Remember pivot is O of n. So we're going to do this again. And then we're going to do it again all the way down. So we're running that pivot function on every single item. So that O of n function pivot, we're running it in times in order to get this sorted. In other words this is O of n squared if you have already sorted data.

So O of n squared is actually the worst case with quicksort. So long as you don't have sorted data, you know you're going to have data that is very out of order. You can count on it running an n times log n times, but if you have sorted data, it might be better to use something like insertion sort. So we saw earlier that insertion sort is generally O of n squared. But the best possible scenario for insertion sort is O of n. So that becomes one of the things you have to consider when you're looking at sorting algorithm.

Big O.


########################################

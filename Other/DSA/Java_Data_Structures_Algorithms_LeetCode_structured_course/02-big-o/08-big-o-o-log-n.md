# 2.8 — Big O: O(log n)

> Section 2: Big O

Now let's look at O of log N. And to explain this I'm going to bring up a sorted array. And to do what we're about to do here the data does have to be sorted. So let's say we want to find a particular value in this array. We'll say we're going to look for the number one. What is the quickest way to narrow this down to get to that one. Well the quickest way would be to cut the array in half and see if the one is in the first half or the second half.

So it is not in the second half. So we don't have to look at any of those numbers so we can remove those. And that may not seem like a big deal when you have an array with only eight items in it. But if you had an array with a million items in it, that's a half a million items that you don't have to look at. So that is a pretty big deal. So then we can take the array and do this again. And we know it's not on the second half. So we can remove those.

And then we'll do it again. And then we'll find the number that we're looking for. So let's bring back all of the other items in the array. And look at how many steps this took to find the number one. It was one two. Three steps. And remember we had eight items in this array. And it just so happens that two to the third power is eight. So now I'm going to take this equation and turn it into a logarithm. And we're not going to get really deep into this math.

This will be pretty simple. But when we convert this to a logarithm it looks like this log sub two of eight equals three. And I'm going to put this back and let's look at this again log sub two of eight equals three. So what this is basically saying is two to the watt power equals eight. Two to the what? Power equals eight. Well, two to the third power equals eight. To put it another way, if you took the number eight and you repeatedly divided it by two, how many times would it take to get down to one item.

And that is three times. But the real power of this is when we're dealing with very large numbers. Let's say we take log sub two of this number and this is over a billion. How many times would you need to cut this number in half to get down to one item. And it is 31 times. So you could have an array with over a billion items in it, and find any number in that array in 31 steps. And that is the power of O of log n. So now let's take this and look at it on a graph.

So you can see that this is very flat, very efficient. It's not as efficient as O of one, of course, but it is the next best thing. And so everything we're going to look at this course is going to be one of these four. Except for I'm going to show one other one here. And this one is O of n times log n that is used with some sorting algorithms. So we're going to see this with quicksort and merge sort. But other than that everything else will be one of these four.

So that. Is O of log n.

----------------------------------------

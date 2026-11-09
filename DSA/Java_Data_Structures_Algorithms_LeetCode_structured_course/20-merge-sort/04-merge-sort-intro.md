# 20.4 — Merge Sort: Intro

> Section 20: Merge Sort

So in the last video we created merge that takes two sorted lists and puts them together. Now we're going to look at Merge Sort. That also needs to take a list and break it in half, and then break it in half again and then do it again. Once we've gone through this process of breaking it in half, it is only then that we can use that helper function merge to take sorted lists and combine them like this. And then we'll do it again and do it again. To create the sorted list.

So what we're going to do here is write the code that breaks lists in half. And this is going to be the first time that we've used recursion. Remember we had two rules for being able to use recursion. First, it has to do the same thing over and over. And this is just going to break lists in half over and over. So it meets that criteria. The second criteria is that you have to be making the problem smaller. Well if you're breaking things in half then by definition you're making things smaller.

So this is a perfect place to use recursion. And we're going to use the recursion until we reach a base case. And the base case is going to be when we've broken it down to where the length of the list is one. So once we've done our recursion to break things in half, we've reached our base case to stop breaking things in half. When we've gotten down to one item. That is when we'll use merge, which we created in the last video to put the list back together.

So these will be the three steps of merge sort. Break it in half until we get it down to one. Then we use merge to put everything back together. And that is our quick overview. Of Mergesort.

----------------------------------------

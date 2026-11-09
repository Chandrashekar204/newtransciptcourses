# 13.7 — Set: Remove Duplicates

> Section 13: <> HT: Interview / LeetCode Exercises

So now we're going to move on to sets. And if you're not familiar with sets, right before this video I included an article explaining some of the details about sets. And this is a very common application for a set. We're going to start with an array list. And then we're going to pass the array list as an argument to when we create a set. And one of the characteristics of a set is that it does not allow duplicates. You'll end up with a set that looks like this.

And ultimately what we want is an array list with all of the duplicates removed. So we'll take the set and then pass that as an argument to creating a new array list. Now I want you to notice that the array list and the set are in square brackets, but they are not the same data structure. Sets do not allow duplicates and they don't have indexes. One of the other characteristics of a set is when you look up by value. Let's say we're going to look up the value four in this set.

That is an O of one operation. Whereas if we look up the value of four in this array list, we have to iterate all the way through the array list looking for a four. That's O of n. So sets are O of one to look up by value and array lists are O of n to lookup by value. And that is our quick overview for remove duplicates.

----------------------------------------

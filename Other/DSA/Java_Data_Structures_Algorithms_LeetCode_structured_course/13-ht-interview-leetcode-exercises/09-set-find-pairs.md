# 13.9 — Set: Find Pairs

> Section 13: <> HT: Interview / LeetCode Exercises

The next coding exercise is called find pairs and you will pass this method three arguments array one, array two, and a target. And for this example we'll use six. And we want to find all of the combinations where a number from the first array and a number from the second array when they are added together equals six. There's two and four, and there is one and five. I'm going to start out by showing you the inefficient way of doing this. And that would be with a nested loop.

If we had a nested loop, we would start with the first item up here and then look for the corresponding number, the number that you would add to this to equal six. And the corresponding number of course would be five. So we would check to see is this a five. It is not. Is this a five. That's not a five either. Is this a five? Well, now we have found the corresponding number, and we know that we have a one and a five that can equal six. But we have touched every item in that second array.

And then the nested loop will go to here. And then look at every item again. So I'm not going to go through all of the steps here. But it is much more efficient to use a set. So we'll take that first array and use that as an argument in creating a set. So what I'll do is I'll remove these indexes and this is the set that it will create. Now we can iterate through this array and looking up values in that set looking for that corresponding three is an O of one operation.

And then we move to here and the corresponding number is two. And looking up that number two is o of one It is much more efficient than using that nested loop. So what we'll do with this pair is put them in an array two and four. Then we move to the next item. And that second array. We look for the corresponding number which is one, and create another array with one and five. And these are the two combinations that add up to that target of six. And what we're going to return is an array list that contains these two arrays.

And that's going to look like this. This is what we are going to return. So I want to emphasize this is not an array list with nested array list. This is an array list that contains two arrays. And that is how we most efficiently find pairs.

----------------------------------------

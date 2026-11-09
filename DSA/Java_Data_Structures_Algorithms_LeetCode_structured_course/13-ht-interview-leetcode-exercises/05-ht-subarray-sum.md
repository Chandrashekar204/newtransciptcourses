# 13.5 — HT: Subarray Sum

> Section 13: <> HT: Interview / LeetCode Exercises

So the next exercise is going to be subarray sum. And what we're going to do is find the subarray whose numbers total a particular target number. In this case we'll use the target of nine. And the correct subarray is this two plus three plus four equals nine. And you might be looking at this thinking that well four plus five equals nine. Why can't that be the subarray. And the reason is that as we are iterating across the array we're going to see these three numbers first.

And then what you'll return is an array with the indexes that are the beginning and the end of the subarray. And those will be returned in an array one and three. If we have a situation where there are not any subarrays that equal the target, let's say the target was 100, you would just return an empty array. So I'll go ahead and remove that. And of course we're going to need our hash map. And we'll have an iterator I that's going to iterate across the array.

And one of the variables that we'll use I call it currentsum. You could call this running total. So what I mean by this is at this point in the array current sum is one. And then after moving to here the current sum is three because it's one plus two is three plus three is six plus four is ten plus five is 15. So that's what I mean by current sum. And during each iteration we're going to take current sum minus the target. So in this case current sum is one minus nine is negative eight.

And we're going to look in the hash map to see if there's a negative eight in the hash map, and obviously the hash map is empty. So there is not. So we're going to add current sum and the index to the hash map. So that means at the index of zero the current sum was one. And then we moved to the next number. And then we do the same thing. We take the current sum minus the target is negative six. And we look in the hash map to see if there's a negative six.

And there's only a one. So we put the current sum of three and the index of one. And then we move to the next number. At this point current sum is six minus nine is negative three. And we check the hash map to see if there's a negative three in there. And there is not. So we add the current sum and the index to the hash map. And then we move to the next item. At this point current sum is ten, minus nine is one, and one is in the hash map at the index of zero.

And what that means if that index is zero in the hash map that our subarray starts with, the next index and the end of the subarray is going to be where I is pointing the index of three. So now we have the information to be able to return this array of one and three the beginning and ending index of the subarray that equals the target. So now I'm going to put everything back the way it was like this. And I'm going to make a change to the array. I'm going to move the one to the end.

And this brings us to the one edge case that I need to show you. And now our range starts at the index of zero. And this is a particular edge case starting at the index of zero. To deal with this, we have to pre-populate the HashMap with this, with a current sum of zero and an index of negative one. Now obviously arrays don't have negative indexes. We're only putting this in the HashMap. But I am going to put this in the array. And like I said obviously arrays don't have negative indexes.

But I'm just going to put that there as a visual. And as we work through this you'll see why it is that we need to do this. So we're going to start at the index of zero. That value of two. So current sum is two minus the target is negative seven. That is not in the hash map. So we'll add this to the hash map that the current sum was two at the index of zero. And then we move to here and current sum is five minus nine is negative four. Negative four is not in the hash map.

So we'll put the current sum of five in the hash map that is at the index of one. So then we move to here. And now current sum is nine and the target is nine and nine minus nine is zero. So you can see why we have to have a zero in the hash map. When you go to look for that it has to be there. And it says that the index for that is negative one. And the beginning of the range of our subarray will be the index after that, which is the index of zero.

And then the ending index is going to be whatever I is. So the array to be returned will contain zero and two. And that is how we do subarray sum.

----------------------------------------

# 5.2 — LL: Has Loop

> Section 5: <> LL: Interview / LeetCode Exercises

So our next coding exercise is called has loop. And it's going to have a lot of similarities to the last coding exercise. So I'm going to bring up a linked list. And we want to check to see if this linked list has a loop. And you can see by looking at this that this does not have a loop. So I'm going to first show you how the code works. If it does not have a loop just like we had in the last video. We're going to have slow and fast. And as we start traversing the linked list, if this has a loop, you will eventually get to the point where slow and fast are going to point at the same node.

So after the first iteration of the loop, fast moves two and slow moves one. And this will be the first time that we check to see if they're equal and they're not. So we're going to go until these two are equal or until we get to the end of the linked list. So we'll move fast forward two and slow forward one. And having fast point to the last node is one of the things that breaks us out of the while loop. And since fast and slow were never equal to each other, that means we do not have a loop.

So we will return false if we have an even number of nodes. We'll move fast forward two, slow forward one, and then we do that. Check to see if they're equal. We run the loop again and move fast forward two and slow forward one. And now we're going to break out of the loop. And slow and fast were never equal to each other. So we return false because it is not true that this has a loop. So now let's look at a situation where we do have a loop, and something would have had to have gone wrong with our code to have this situation happen.

So we're going to run the loop again. Now with this situation I'm going to show slow moving first and then fast moving second. It doesn't really matter the order that you do it in, because you're doing the comparison after you have moved both so slow and fast are not equal to each other. And we have not reached the end of the linked list. So we'll keep going. We'll move, slow up one and then fast up two and do the comparison again. And then we'll move slow to here and fast to here and do the comparison.

They are not equal to each other. And then we'll move slow up here and then fast up here. And now slow and fast are pointing to the same node. And that means that we have a loop. So if this situation happens, we will return. True. Because it's true that this linked list has a loop. So I want you to notice that in this video and in the previous video, I did not include any code. And that's going to be the case for all of the interview slash leetcode exercises.

So in these coding exercises I'll give you strategies, I'll give you the visuals, but it'll be up to you to figure out how to write the code. And the reason for that is we've already covered linked lists in detail. And once you have these strategies at this point you should be able to implement them. But that is our overview of has loop.

----------------------------------------

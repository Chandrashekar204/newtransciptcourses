# 10.7 — BST: Contains - Intro

> Section 10: Trees

So now we're going to build our contains method. So I'm going to bring up a tree like this. And with contains if we're looking for a number that's in the tree let's say the number 27, we want it to return true. If we're looking for a number that's not in the tree say the number 17. And in that case we want it to return false. So I'm going to walk through the steps of doing that in this video. This will be similar to what we did with insert, where we have a video, where we go through the steps, and then a separate video where we use those steps to write the code.

So if you're sitting down with a piece of paper and you're trying to come up with all the steps, probably the first step you're going to write down is what if we have an empty tree root is equal to null? Obviously, in this situation, whatever number you're looking for is not in the tree. So we'll say if root equals null, return false. So let's bring back our tree. So the next thing we'll do is create our temp variable. And let's say we're looking for the number 27.

Temp would go left and then right. And then temp dot value would be equal to the value that we're looking for. And we would return true. So let's put this up at the top. We'll create that temp variable like this. Temp equals root. So the next thing we need to do is create a while loop to move temp through the tree, and to explain how we're going to write that while loop. I'm going to show you what happens when we're looking for a number that is not in the tree.

So let's say we're looking for the number 17. Let's less than 47. So we're going to go left 17 is less than 21. So we go left again. 17 is less than 18. So we go left again. So now temp is equal to null. If we ever have this situation, then we don't want to continue running the while loop. This is what's going to break us out of the while loop. So our while loop will run so long as temp is not equal to null. So inside of this while loop we have three different scenarios.

Either the number we're looking for is less than the one we're comparing it to, in which case we go left. Else. If it is greater than we're going to go, right? Else is equal to, and then we will return true. There is a fourth scenario though. Temp could be equal to null. If temp is ever equal to null, that'll break us out of this while loop and then we return false. So those are all of the steps for the contains method. And we will pick up here in the next video where we code contains.

----------------------------------------

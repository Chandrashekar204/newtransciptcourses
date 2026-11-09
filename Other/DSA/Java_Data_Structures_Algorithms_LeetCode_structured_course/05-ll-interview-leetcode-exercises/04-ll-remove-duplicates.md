# 5.4 — LL: Remove Duplicates

> Section 5: <> LL: Interview / LeetCode Exercises

Our next coding exercise is called Remove Duplicates. So if you have this linked list you can see that we have two ones and two twos. And our job is to remove the duplicates. Now there are a couple of ways of solving this problem. There's the really efficient way which uses a set and then the inefficient way that uses nested loops. If you use a set, it's O of N, and if you use nested loops it's O of n squared. But at this point in the course I haven't covered sets.

So I'm just going to walk through how to do this with nested loops. We'll have one loop that has a variable called current, and then another nested loop that has a variable called runner. And current is the current node that we're comparing to the rest of the nodes. And runner is going to run the length of the linked list. So runner is always going to check the next node. So right now it's checking to see if that two node is equal to the one node.

And I'll show you why in a moment that we have to do it that way. But then it moves up and checks to see if the three node is equal to one and it's not. Now we're checking to see if that one node is equal to one. And it is. And the reason why you need to have runner here when you're checking the next node is because we need that next pointer of the node that runner is pointing to to point to the next node. And that removes the one from the linked list.

And then we go to the end looking for ones. And we don't find any. And then we move current up one. And we set runner to be equal to current. And then we do this again. And now that two is equal to current. And we'll have the next pointer of the node that runner is pointing to, point to that five node and we remove the two node. And of course there are no other twos, and we move current up and runner back to point at the same node as current. And now we go looking for threes and move current up and runner back.

And then we look for fours. And we do this until current is past the end of the linked list. And that breaks us out of the loop. And now we've removed all of the duplicates in the linked list. And as I mentioned at the beginning of the video, there is a more efficient way of solving this with a set. And I've included both of the solutions, the one with the set and the one with the nested loops under the solution explanation tab. And that is the overview of remove duplicates.

----------------------------------------

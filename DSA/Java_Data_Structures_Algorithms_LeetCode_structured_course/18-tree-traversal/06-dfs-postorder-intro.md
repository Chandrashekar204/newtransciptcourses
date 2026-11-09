# 18.6 — DFS: PostOrder - Intro

> Section 18: Tree Traversal

Now let's look at depth. First search post order. I'm going to bring up a tree here. In this video we'll just walk through the steps of it and then we'll code it in the next video. And just like with all the other tree traversals, we're going to start at the top. What's different here is that we're just going to visit that 47 node. We're not going to write that value to the results list yet. Then we're going to go to the left and then visit the 21, and we'll go to the left again to the 18.

Now, what the 18 is going to do is it's going to look to the left. There's no node there. It'll look to the right and there is no node there. And then finally it will write its value to the results list. So the order that we're doing this is we look left, we look right. And then we write the value from that node. So now we come up to the 21. It has gone left. Now it's going to go right to the 27. It's going to look to the left. It's going to look to the right.

And then finally we will write the value 27 to the results list. Now we come back up to the 21 again. Now it has gone left. It has gone right now we can write that value to the list. And that brings us back up to the 47. It has gone left now it will go right to the 76 node. And we always start with going left first. So it will go to the 52 node. It will look left and right and then write its value. We come back up to the 76. It has gone left. Now it will go write that 82 node will look left and then right, and then write its value.

That brings us back up to the 76. It has now gone left and right and it can write its value. And that brings us back up to the 47. It has gone left. It has gone right. And now its value can be written to the results list. So we'll code this in the next video. But that is our overview of depth. First search post order.

----------------------------------------

# 18.8 — DFS: InOrder - Intro

> Section 18: Tree Traversal

Okay. So now let's look at depth. First search in order. We'll bring up our tree like this. And what we're going to do is we're going to visit that first node. We're going to go to the left. Go to the left again the 18 will try to go to the left. There's nothing there. We'll write that 18 to our results list and then it'll go to the right. So at this point the tree looks exactly the same as it did at this point with depth. First search postorder.

But instead of going left, then right, and then writing its value, it's going left, writing its value, and then going right. So we're going to get this in a different order. So now we're going to come up to the 21. It has gone left. Now it's going to write its value and then go write. The 27 will go left write its value and then go right. That brings us up to the 47 node. It has gone left. Now we can write its value and go write. The 76 will start out by going left.

The 52 will go left, write its value and then go right. The 76 has already gone left. Now we can write its value to the results list and then go right. Then the 82 will go left and then write its value, and then try to go right. So at this point, what I'm going to do is turn the entire tree back to blue and look just at the order that the items get written to the list. We start out with the 18 being written to the list, and this is the lowest value in the tree.

Then it's the 21, the next lowest, and so on. Then the 47, the 52 and the 76 and the 82. So all of the numbers are written to the list in numerical order. So that is depth first search in order.

----------------------------------------

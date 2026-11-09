# 10.1 — Trees: Intro & Terminology

> Section 10: Trees

So now we're going to look at trees. And we've already seen a tree in this course. And that was a linked list. A linked list is just a tree that doesn't fork. And we said that this node was similar to a hash map that looked like this. So what I'm going to do is take this node and make changes to it and turn it into a binary tree node. So the first thing I'm going to do is change the color. Since we're moving to a new data structure, and instead of pointing to next, this points to left and right.

So if we're going to use the hash map analogy again you could say that it is something like this. So let's turn this back into the graphic. We'll shrink this down. That left and right pointer can point to new nodes like this. And this would be similar to a set of nested hash maps that look like this. So let's put this back. And the way we've built these because it can only point to left and right. It can only point to two other nodes. That's what makes it a binary tree.

But there is no rule that says that a tree has to be a binary tree. You can have each node point to three nodes or ten nodes or 100 nodes. It's just the way we're doing it here. Each node can only point to two nodes. And then of course, these new nodes that we've added can also point to two other nodes themselves. So now let's look at some terminology. This tree here is what is called full and a full tree. Every node either points to zero nodes or two nodes.

So if you do something like this. Now you have a node, the seven node that only points to one node, so it is no longer full. So let's remove that. Make it full again. And if we remove these two, it is still full, but it is also something else. It is perfect. With a perfect tree. Any level in the tree that has any nodes is completely filled all the way across, so this is also a perfect tree. But if we remove these two, it is no longer perfect. But it is still full.

So let's bring these two back. So a perfect tree is also something else. It is complete. So with a complete tree, you are filling the tree from left to right with no gaps. So if we add a node down here, it is still complete because we are filling the tree from left to right. But it is no longer full and it is no longer perfect. If we add one more node like this, filling this from left to right, it remains complete, but it is now also full. But it is not perfect because we haven't filled it all the way across.

So if we do this now, it is full and perfect and complete. Okay. So let's focus in on this tree and drop some of these off. So this node here is a parent. Of these two child nodes. These two child nodes, because they share the same parent, are also called siblings. And every node can only have one parent. So if you see something like this where a node has more than one parent, then it is not a tree. So let's put this back. And child nodes, of course, can also be parent nodes.

Now these nodes at the bottom, they don't have any children. And a node that doesn't have children is called a leaf. All right. That is our intro for trees.

----------------------------------------

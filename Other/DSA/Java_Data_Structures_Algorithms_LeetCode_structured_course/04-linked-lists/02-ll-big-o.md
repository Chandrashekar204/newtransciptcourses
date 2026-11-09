# 4.2 — LL: Big O

> Section 4: Linked Lists

So now we're going to talk about link lists big O. So what I'm going to talk about is the big O of each of the methods that we're going to create in this course. So for example we have a linked list. If we're going to add something to the end, the steps that we would do is we're going to have this arrow point to it, tail is going to point to it and it gets added into the linked list. Now from a big O perspective n is the number of nodes. So the steps that we just walked through are going to be the same.

If the linked list has ten items in it, or it has a thousand items in it, it's not going to change based on whatever n is. Which means that adding something to the end is O of one. Now this is different. When we remove the item, it looks like it would be pretty simple to pop that off, have tail point over to there and it would be an easy process. But in order to move tail over to point at that seven node. You have to have this pointer set equal to something else that is pointing at that seven node.

And there's only one thing that is pointing at that node. And it is this pointer here. And we can't move backwards to the list. We can only go the direction that the arrows are going. So let's move tail back and look what we need to do. We need to start at the head and iterate through the list like this. Until we get to this pointer. Then we can say set tail equal to that pointer. And then it moves back. But because we had to touch every node and iterate through the list.

This is O of N. So now let's look at adding an item to the other end. So we're going to have the four node point to the first node in the list. So in other words we're going to set the pointer on the four node to be equal to head like this. Then we're going to move head over to point at the new node. And that adds that into the list. And it doesn't matter how big the list is, it's going to be the same number of operations to add this item. So that is O of one.

Likewise, if we're going to remove that four node, that first one, we have a fixed number of steps to do this. We'll need to move that head pointer over one. So we'll set head to be equal to head dot next. And that moves that over. Then we'll remove this node from the list like that. And that since it's a fixed number of steps is O of one. Now let's look at inserting a node. Let's say we're going to insert this node after the 23 node. We're going to insert this at the index of three.

In order to do that we'll have to start at the head and iterate through this list and get to this node. We want the four node to point to the seven node. So this pointer points to the seven node. We'll set the new node pointer equal to that. Then we'll have the pointer from the 23 point to the new node. And that adds that into the list. But because we had to iterate through the list this is o of n. So now let's look at removing that node. So to get to that node we have to start at the head.

And we have to iterate through the entire list to get to this node. And let's just have that come down here. We want that 23 to point to the seven node and the four points there. So we'll set the pointer for the 23 to be equal to that. And then we'll set this pointer equal to null. And that removes that from the linked list. But once again we had to iterate through the list to do that. So that is o of n. The next thing is if we want to look for something by value, let's say we want to look for the value of 23.

In order to do that, we have to start at the head and iterate through and see if that's 23 and that's 23. And then finally we find it. Now the other way we can look for this is by index. And if we're looking for this as the index of two, we're going to start at the head and go 012. So it doesn't matter if we're looking for it by value or by index. It is O of n. So this is one of the places where an array list is better than a linked list. If you look for it by index and a linked list, you have to iterate through to get to that index.

So now I'm going to remove this, and I'm going to bring in a chart to compare linked lists to array lists. So everything that's in gray is the same for both. But there are a couple of these that are better for an array list, removing the last item and looking something up by index. But there are also a couple of things that are going to be better for a linked list prepending an item or removing the first item. So in other words, adding or removing something from the beginning, an array list is going to be O of n because you have to re-index everything, whereas a linked list because you don't have indexes in there, it is o of one.

So I will create a PDF of this table and attach it to this lesson. So you can download that. But that is linked list big O.

----------------------------------------

# 7.3 — DLL: Partition List

> Section 7: <> DLL: Interview / LeetCode Exercises

So in this video we're going to talk about partition list with a doubly linked list. This is going to be one of three leetcode challenges for doubly linked lists that we also had for linked lists. And those three are partition list reverse between and swap pairs. The last two reverse between and swap pairs. I'm not going to have a video for doubly linked lists. And the reason for that is you're going to already understand the logic of how to do all three of these from having done it with singly linked lists.

But when you do partition list with a doubly linked list, there's an edge case. And I want to show you that edge case. So if you remember from partition list with a singly linked list, if we want to have everything that's greater than or equal to five on one side and everything that is less than five on the other, we take all of the nodes that are less than five, and we're going to put them together like this. And then we're going to have dummy nodes and variables called previous one and previous two.

All of this is going to be the same, with a singly linked list and a doubly linked list, with the exception, of course, that we have previous pointers that we need to attach in addition to the next pointers. And then if you'll recall, we just take both of these and then combine them, but with a doubly linked list. When we go to combine these there's an edge case. And that is if the second list is empty, you're going to have to write code specifically to deal with this edge case.

And by this point in the course, you should be able to take out a piece of paper and draw this out and figure out why that's an edge case. So I'm not going to give you the details of why it's an edge case, but I am going to give you this hint that you're going to have to write code to specifically deal with this. And that is your hint to be able to solve doubly linked list. Partition list.


########################################

# 8.5 — Queue: Intro

> Section 8: Stacks & Queues

So now we're going to do our introduction to cues. So a cue is just like when you get in line people can get in line behind you. And then when you remove someone from the line, you take the first person in line out of the line. This is Fifo first in, first out as opposed to stacks which was last in first out. So a couple of pieces of terminology with a queue. When you add someone or something to a queue, you would say that you have in queued that person.

And then when you remove someone from a queue or a node from a queue, you would say that you have dequeued them. So now let's look at a couple of ways we can implement a queue, just like we did with stacks. We're going to first look at an array list. So the only rule with a queue is you have to enqueue and dequeue on opposite ends. So with an array list if we dequeue here or we enqueue on this end. Either way it would be o of one. But on the other end if we dequeue or enqueue on this end it's O of n.

So you could say, hey, I want to enqueue on this side and I want to dequeue on this side. You're still going to have one O of one and one O of n. Or it could be the other way. We're going to enqueue over here and dequeue over here. Either way you're going to have one side that's O of one and one side that is O of n. So let's compare this to a linked list with a linked list. To remove an item on this end is o of n, but to add an item is o of one.

Then on this end to remove an item is o of one, but also adding an item is O of one. So the one thing you don't want to do if you're going to use a linked list for a queue, is you do not want to dequeue on this end. You want to enqueue on this end and dequeue on this end. That way, enqueue and dequeue are both o of one. So with the linked list we also had head and tail. We'll rename these and call these first and last. And that is our introduction to cuz.

----------------------------------------

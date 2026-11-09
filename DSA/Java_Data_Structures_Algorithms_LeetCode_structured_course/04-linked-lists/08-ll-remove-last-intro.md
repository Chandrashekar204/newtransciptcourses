# 4.8 — LL: Remove Last (Intro)

> Section 4: Linked Lists

So now we're going to look at removing the last item from a linked list. This is a lot more complicated than adding an item to the end of a linked list. We talked about this in the big O section, that this is a more complicated method, and it is complicated enough that I've split this out into two videos. In this video, we'll talk conceptually about what happens when we remove that last item. So when we remove it, we'll also want to return it. This is what it looks like on a basic level when we have multiple items in the linked list.

We'll also have to code for when we have an empty linked list. And there is another edge case for when we only have one item in the linked list. So at a high level, this is what we'll need to do. If you want to try to code this, go ahead and pause it here. So let's look first at this situation where we have multiple items in the linked list and what we do when we remove this and we return this. I'm going to bring this back and turn our linked list into this.

And as we have discussed previously, a linked list acts pretty much like a set of nested hash maps. And what we want to do is have tail point at this node, and then we'll say tail dot next equals null. And then we can return this node. So let's put this back the way it was and look at what we need to do to make that happen. So we want tail to point to this node. So what we have to do because it is a pointer is set it equal to another pointer that is already pointing at that node.

In other words, something that is set equal to that node. And the only thing that's set equal to this node is the next value in this node. So that means we need to get to this node. And the only thing that is pointing at that node is the next value in this node, and so on until we get to the head. So we have to start at the head, and then we can iterate through the linked list until we get down to this node. And then we can set tail to be equal to this pointer.

Then we can say that tale dot next equals null and then return this node. So now let's put this back like this and look at what we need to do to make this happen. We'll need a couple of variables I'm going to call mine pre and temp. We'll set them equal to head and we can remove head and tail. I'm going to move pre underneath like this. And then we're going to have a loop that runs until temp dot. Next is NULL. And you can see on the end of the linked list that's where that's going to happen.

And what we'll do in each iteration of the loop is we will have pre be equal to temp, and the first iteration it is already equal to temp. And then we'll set temp to be equal to temp dot next. Then we'll see if temp next is null. It is not. We'll set pre equal to temp. And temp is equal to temp. Next. And then we'll keep going through the list like this. We'll move pre up and temp over. And this will be the last time we move these. This will move pre up and temp over on this iteration.

That is NULL. And we stop running the while loop and we stop right here. So let's look at these two variables one at a time. We'll look at pre. First I'm going to remove temp. For now I will be bringing this back. And there's only one reason that pre exists. And so we can say that tail is equal to pre. And that's what moves tail back. Now we're done with the pre variable I'm going to drop this out. And now we can say tail dot next equals null. That will break this node off.

And now I'm going to bring back that temp variable. And at the end of the method what we'll do is we'll say return temp. And that's going to return this node. So we will code this in the next video. But for now that is our introduction to remove last.

----------------------------------------

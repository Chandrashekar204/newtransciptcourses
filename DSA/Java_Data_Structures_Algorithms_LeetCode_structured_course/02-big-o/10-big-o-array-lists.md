# 2.10 — Big O: Array Lists

> Section 2: Big O

So now we're going to look at the big O of array lists. And I use an array list here instead of arrays. Because to show all of these concepts, I need a data structure that's going to be dynamic and allow us to add new items and not just be of fixed length, but a lot of the concepts that I'm going to show here will apply to arrays as well. Also, instead of showing our array list like this, I'm going to represent it like this so I can show the indexes.

Now we'll just walk through some of the methods for Arraylists and what the big O of those methods are. So we'll start out with my list for my array list. And say dot, add with the number 17 that's going to do this. When we add something to this end of the array list. It's a pretty simple process because we don't have any reindexing like all the way down. These indexes do not need to be changed. Likewise, when we remove this item with a dot, remove at the index of four and we remove that, there is nothing that needs to be re-indexed and the array list.

So it is one operation to add something. It is one operation to remove something. So this is O of one. This is different. If we do something on the other end of the array list. So if we say my list dot, remove the item at the index of zero. This one right here. When we remove this the problem that we have. Is this is no longer at the correct index. So we need to change this index of one here to be an index of zero. And then we need to do this all the way down and touch every item in the array list.

Also, if we add an item at the index of zero, we bring that 11 back. We need to change this index. And then we have to do this all the way down to make room. For that 11 to be at the index of zero. So in this case, n is the number of items in the array list. And because we had to touch each item, that means this is O of n. So it is o of one on this end when you're adding something or removing something. But it is O of N to do those things on this end.

So when we remove that item, we have to re-index everything here. If we bring it back, we have to do all the re-indexing again to bring it back. So it's o of one on one end, it's O of N on the other. So if we say my list dot add at the index of one, the number 99. That's going to be this index here. We're going to drop the number 99 in here. What we have to do here is reindex this item and make that a two. And this a three and that a four. So you have to touch all of the items that come after where the insert happened.

So that is O of N. So you might say that this should be O of one half n, because on average this insert is going to be somewhere in the middle and you'll only have to touch half the items. However, there are two problems with that logic. First, big O measures worst case, not average case. But even if O of one half N was our worst case, one half is a constant and we drop constants. So likewise, when we go to remove that item, we're going to have to re-index everything that comes after it again.

So it doesn't matter if it's an insert or a remove, it is O of n. So now let's look at finding something by value. Let's say we're looking for the value of seven. We'd start at the beginning of the array list or the array. And then we say is this the value of seven. This is 11. So we keep moving until we get to the value of seven. So looking for an item by value is o of n. But it's different if we're looking for this by index. If we are looking for the index of three, we do not have to iterate all the way through this.

We can go directly to this index and that is O of one. And that is our overview of big O of a Rayless.

----------------------------------------

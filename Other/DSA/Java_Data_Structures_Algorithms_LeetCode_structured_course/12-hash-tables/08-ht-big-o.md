# 12.8 — HT: Big O

> Section 12: Hash Tables

So now we're going to look at the big O of hash tables. And I'm also going to bring up our graphic for our hash method. And because this hash method has to be run every time we add an item or we get an item, we have to determine what is the big O of the hash method itself. Well, the hash method itself is O of one. And the reason for that is the hash method is going to go through the same number of operations to determine a hash, regardless of the number of items that are already in the hash table.

Now let's walk through setting an item. Say we're going to set washers. We would run it through our hash method. And we're going to say in this case that it gives us an index of zero. And then we'll add that item like that. It is a single step. So you can see where that would be considered O of one. Now how about getting an item? We'll get screws. We'll run this through our hash method. And that gives us an index of six. And we find screws in one step.

But what if our hash table doesn't look like this? What if our hash table looks like this? Now, when we say get screws, it's going to be at the index of two. And then we have to iterate through this entire linked list until we finally get to screws. So you might think that that makes this a within. But when you're dealing with a hash table, the assumption is going to be that that hash method is going to create very random addresses in your hash table is going to look something more like this.

You'll have a larger address space. You'll have a very good hash method that will randomize where these things are put. And because of that, we treat getting an item and setting an item and a hash table. As of one. And that is hash table big O.

----------------------------------------

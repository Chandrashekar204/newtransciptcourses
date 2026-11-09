# 12.5 — HT: Set

> Section 12: Hash Tables

So now let's create our set method for our hash table. I'll start off by bringing up our array called data map. That is our address space. And then we're also going to be using the hash method. So set will look something like this. We have set nails with a quantity of 100. And that key nails is going to be put through our hash method. We'll get an index of six in this case. But then the set method is also going to create this linked list node. And then we're going to put that at the index of six.

So I'm going to take that out for now. And then put our hash method graphic down here in the corner. And we'll start coding this. So we're going to call this set and we're going to pass this a key which will be a string and a value that is an integer. And the first thing we need to do is determine the index where the key value pair is going to go. Now we're going to do that like this. We're going to have a variable called index that is an integer.

And then we're going to set it equal to hash. And we're going to pass that the key. And then we're going to run the hash method on that key. And if we use nails we get an index of six. So that is where our node will eventually go. So now we need to create that node. We'll do that like this. We'll pass this a key and a value and that creates this node. So just like we saw in the linked list section of the course, inserting a node into an empty linked list is different than inserting a node into a linked list that has nodes in it.

So first we're going to write the code for inserting this into an empty linked list. And that's going to look like this. We'll say if data map at the particular index is equal to null. And that's what it is. Now we have an empty linked list. Then we're going to set data map at that index to be equal to new node. And remember data map is an array of pointers to nodes. So when we set that pointer equal to new node that does this. So otherwise we do have items in the linked list and I'll say else and I'm going to shrink this down.

So we have a little bit more room here. So to better show how we're going to loop through the nodes and then add a node to the end, I'm going to add an extra node to our linked list. And then we're going to show how we add that lumbar node to this linked list. So we're going to create a variable temp that we're going to use to iterate through this linked list. So we're going to say node temp that creates this. And we're going to set this equal to data map index.

So what is at data map index. It is this pointer. Here it is the pointer that points to the first node. So this line of code here is the equivalent of setting temp equal to head. So when we set temp to be equal to that pointer we're just pointing temp at that first node. So then we'll create this while loop to iterate through the linked list. So we'll say while temp dot next is not equal to null. So that is temp dot next. That is not equal to null because it's pointing to a node.

Then will set temp to be equal to temp. Next which moves that over. So now when we say while temp dot next is not equal to null temp dot next is null. And that breaks us out of this while loop. So this while loop is going to take temp to the last node and stop. And then we'll say temp dot next equals new node. That is temp dot next equals new node. And that adds that into our linked list. So that is our set method. So we'll look at this code in a moment in IntelliJ.

And when we do we will set these three key value pairs which will all be at the index of six. And then I'll throw in a couple more key value pairs that will be at different indexes. And then we will do a print table. So now let's flip over to IntelliJ and take a look at this. So there is our set method there. That's part of our hash table class. And then I will come up here to our main class that contains our main method. And then with this line here we're creating a new hash table called my hash table.

This is where we set nails, tile and lumber that we just saw in the graphic. And then I've added bolts and screws here. And then with this line here we will print out this hash table. And I'll run this. And you can see here that we have added all of these key value pairs to our hash table. And that is our method for set.

----------------------------------------

# 12.6 — HT: Get

> Section 12: Hash Tables

So now let's write our Get method. I'm going to bring up our address space here with a few key value pairs. And then I'll also bring in our hash method. So if we do something like get lumber and we run this through our hash method, the hash method will return a six. And we'll know that that is the index where we could find lumber. But once we get to this index, we'll have to iterate through the linked list like this until we get to lumber. And remember, lumber was the key.

What we want to return is the value. Of 80. But if we look for something like bolts and we run this through our hash method, we'll get a four. But when we come to the index of four, there aren't any bolts. So in this case, when we don't find the key that we're looking for, we want to return zero. So let's move our hash method down to the corner here and we'll start writing our code. We'll call our method get. We pass it a string, which is the key.

But we're going to return an integer which is the value associated with that key. So the first thing we need to do is determine the index where we would expect to find a particular key. So we take the key that we pass the get method. And we pass that to the hash method. And we run that. And if say we were looking for lumber we would get an index of six. And we know that is where we would need to go to look for lumber. So now that we have found the index, we need to be able to iterate through the linked list.

And in order to do that we'll need a variable. I'll call this temp. And we'll do that like this. Temp equals data map at that index. And that's going to point temp to that first node. So then we'll create this while loop to iterate through the linked list. While temp is not equal to null. And then this while loop is going to contain this if statement if temp dot key. And right now temp dot key is nails. That's the key of the node that temp is pointing to.

If it is equal to the key that we're looking for then we'll return temp dot value. So in this case temp dot value is 100. But let's say instead of looking for nails we're looking for lumber. We'll need to move temp through this linked list. So we'll say temp. Temp dot next. And that's going to move temp forward and forward again. And in this case temp dot key is equal to the key we're looking for. So then we'll return temp dot value which in this case is 80.

So now let's look at a couple of situations where we're looking for something. And it is not in the hash table. So first let's put this back the way it was. But one of the things we know, if it's not in the hash table, that we do not have any of that item and we're going to want to return zero. So situation number one is if you have a linked list at that index, we'll run this while loop while temp is not equal to null. And then we'll go through here until temp is equal to null.

That breaks us out of the while loop. And then we come down to this return zero. The other possibility is you're looking for something like bolts which would be at the index of four. In this case you don't have a linked list at all. So the code will run a little bit different here. What's going to happen is temp is going to be set equal to null right out of the gate. Because data map index at the index of four is equal to null. To put it another way, this is an array of pointers to nodes.

So the pointer that's at the index of four doesn't point to anything. There is no node for it to point to, which means it points to null. So in this line of code, temp would be set equal to null. So when we go to this line here, while temp is not equal to null, it's going to make it where we don't run the while loop at all. We'll just skip that and go straight down to return zero. So that is all of our code for the Get method. So now let's flip over to IntelliJ and take a look at this.

So there is our Get method there added to our hash table class. Then I'll come up here to our main class that contains our main method. And what we've done here is we've created a hash table called my hash table. And then we have added the three items we had in the diagram nails, tile and lumber. And then with this line here we'll do a print table to take a look at our hash table. So I'll run this. And you can see down here at the index of six, we have nails, tile and lumber.

So now what I'm going to do is I'm going to replace this print table. With these two lines, and all we're doing here is we're running the get method on lumber. And you can see over here that this should return 80. And then with this line we're going to get bolts. And obviously we don't have any bolts. And that one should return zero. So now I'll run this. And just as we expected, this returned 80 and zero. And that is our method. Forget.

----------------------------------------

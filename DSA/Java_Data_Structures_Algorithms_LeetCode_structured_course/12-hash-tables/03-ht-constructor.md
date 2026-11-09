# 12.3 — HT: Constructor

> Section 12: Hash Tables

So now we're going to build our constructor for our hash table. So I'm going to bring up our address space here. And I'm going to make a change to this address space to emphasize a particular point. I'm going to remove that last index on the bottom and then expand this out. But when we do it like this our address space has seven indexes. And the reason why we want to do this is we'll have fewer collisions if our address space has a prime number of addresses.

So now let's start coding this. The class is hash table. That I'm going to create an integer that I call size, that will be the size of the array that we're using for our address space. And then we'll create the data map array like this. So notice that the type is node. And remember when we set something to type node it is a pointer to a node. So this is an array of pointers to nodes. So now let's create the constructor. It's only going to have this one line here.

And we will create an array of this size here which will be size seven which creates the array on the left. And of course, instead of using a variable called size, you could directly put the seven in there. But I think this makes it easier for someone that comes back and looks at this code later to realize that you can just change the size by changing that variable at the top. So now that we have this built out, I want to emphasize that this is an array that contains pointers to nodes.

That's all this contains is these pointers. So the next thing we need to do is actually create the nodes that these pointers would point to. So these nodes are going to be a little different than the nodes that we created for linked lists previously. Now we've used the analogy that these nodes are similar to a hash map. I'll do the same thing here. It would look like this where key is a string, value is an integer. And then next points to a node.

So all of these will be class variables and our node class. So let's start building that out. So we have key as a string and value as an integer. And next points to a node. So now let's look at our constructor for the node. It's going to look like this. Previously with nodes we just pass it a value. But here we're going to pass it a key that is a string. And then the integer value. Then we'll do this. This dot key equals key. And this dot value equals value.

So that key and value are these variables here. And we're setting this dot key and this dot value to be equal to those. And this dot key and this dot value are these variables up here. So what we've done with the code that we've created in this video is we've made it where we can initialize our address space. And then we have a class that creates nodes. So now let's flip over and take a look at all of this code and IntelliJ. So now we're moving to a new data structure.

So we have the package hash table all lowercase. And then we'll write our code for our hash table. And the hash table class capitalized. And then we'll run the code in our main class that contains our main method. I'm going to come up here and close this side panel. And this is all of the code that we just created for the hash table class. And then we have an inner class for creating nodes. But I'm going to scroll up here and also show this method here print table.

And I created this just like we had print list or print queue or print stack to be able to see what is in our hash table. So now I'm going to come up to our main tab here for our main class. And this has our main method. And all we're going to do here is create a new hash table called my hash table. And then I'm going to run print table. And this is just going to be an empty table. But you'll be able to see that we have addresses zero through six.

So I'll run this. And you can see over here our empty hash table with indexes of zero through six. So it looks like we have a working hash table constructor.

----------------------------------------

# 3.2 — References

> Section 3: Classes & References

In Java. There are variables that hold values and there are variables that hold references. And I'm going to compare and contrast those in this video. I'm going to start out with variables that hold values. An example would be an int Num1 holds the value 11. It does not hold a reference, it holds a value. And if you set num2 to be equal to num one, of course num2 is going to be equal to 11 as well. So I'm going to represent this in a little bit different way here without code like this.

When you say you want num2 to be equal to the same thing that num1 is equal to, you are setting it equal to the same value. But these two variables at this point are independent If you later change num one to be equal to 22, it is not going to change num two to be equal to 22, it remains 11. They are independent. Now let's compare this to a variable that holds a reference. Let's say we have a variable map one and we set it to be equal to this hash map.

Map one does not hold a value that is equal to this hash map. That variable holds an address that points to the hash map. It holds a reference. And these types of variables work in a different way. So if we set a new variable of map two to be equal to map one, I'm going to show you what does not happen is you do not get another hash map. That map two points to it does not work like this. So I'm going to remove this. When you set Map2 to be equal to map one.

Map one is going to pass a reference the address. So map two is going to point to the exact same. HashMap in memory. So if you said that you want to change this 11 for map one to be equal to 22, it changes it for map two as well, because map two is pointing to the exact same HashMap. So now I'm going to bring up another HashMap that we'll call map three. And now if you say that you want map two to be equal to map three, you're going to have map two point to the same place in memory as map three.

So now they both point to the same HashMap. So once you assign this kind of variable, it can be reassigned to another HashMap. And now let's do this one more time. We'll say that map one is equal to map two. And now map one is going to point down here as well. And notice that nothing is pointing to this HashMap anymore. And you can only get to this HashMap through a variable. And there are no variables pointing to this. Which means this is taking up space in memory, but it is unusable.

And Java has a process that runs periodically looking for this type of situation. And when it finds something like this where there are no variables pointing at it, it will be removed in a process called garbage collection. So now all three of these variables are pointing at this new HashMap. And the reason that this is important is when we get to the next data structure linked lists, we're going to create what are called nodes. And all of these principles with references will apply to those nodes.

So instead of having map1, map2 and map3 pointing to a hash map, you could have node one, two and three pointing at a node. And if you said that you wanted to change the value of node one from 22 to 33, and then you printed out the values for node two and node three, well, those would be 33 as well because they're pointing to the same node. And when you create a linked list you're going to have a variable called head. And that is going to be a variable that holds a reference.

In other words, is going to point to a place in memory where that node resides. So if you create a new variable let's say we call it temp and we set it to be equal to head. When you do that, you are passing a reference and you're making it where temp points at the same node that head is pointing to. And notice the node itself has a pointer a reference. And if you have one of these that's not pointing at a node, that means that it is null which means it is pointing to nothing.

But in a linked list, we're going to create nodes that can point one to another to another. So if we added another node it would look like this. The last node in the linked list is always going to point to null. It is what is called a null terminated list. And all of the variables in the linked list section, or the doubly linked list section, or stacks or queues or binary search trees. All of those nodes. Any variable that refers to that node. You can think of as just pointing at the node.

So let's say we want to have head point at the 44 node. What you would have to do in that situation is set head to be equal to another reference that is pointing at the 44 node. And there's only one thing on the screen here that is pointing at the 44 node. And it is this arrow. So if you set head to be equal to the address that is stored there, it would cause head to point to this node. So it's very important to understand that these are all just references and how it works.

When you set one reference to be equal to another reference. And you might be wondering, why would you ever want head to point to the second node? Well, you would want to do that if you were removing the first node. And this will be one of the things that we do when we get to the linked list section is learn how to remove the first node. And of course we could also remove this node. So what happens to head if you remove all of the nodes from the linked list?

Because you could have an empty linked list. That would mean that head is equal to null, which just means that head is not pointing at a node. So it is important to understand with any of the data structures where we have a node class, that any variable that is set equal to a node is not holding a value, it is holding an address that points at a node. All of those types of variables are going to hold references.


########################################

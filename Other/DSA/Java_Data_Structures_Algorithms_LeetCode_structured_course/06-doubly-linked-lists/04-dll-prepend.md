# 6.4 — DLL: Prepend

> Section 6: Doubly Linked Lists

So now we're going to create our prepend method. I'll bring up our doubly linked list like this. So what we're going to do here is we'll have the next pointer from the new node point to the last node in the list. The previous pointer from that last node is going to point back to the new node. Head will point to the new node, and that will add that into our linked list. We also have to code for when the linked list is empty. In which case we'll just have head and tail point to the new node.

So if you're going to code this, go ahead and pause it here. Otherwise I will get into the code. So we'll call this method prepend. We'll pass it a value and the return type is void. When we prepend that value onto the doubly linked list, we don't need to return anything. And the first thing we'll do is create a node with that value like this. And then we'll start out by coding for when we have an empty linked list. So we have to test to see if the linked list is in fact empty.

So we'll say if length equals zero. Or we could say if head equals null then we'll have head and tail be set equal to the new node. Like this. So that is for if we don't have any items in our linked list. And if we do, we'll say else and we'll build out our else statement. So the first thing we'll do is have that next pointer from the new node point to the first node in our list. And to do that we'll set that equal to that head pointer. Since it is pointing at that node like this.

And we'll do it with this code here. Newnode.next equals head. So then we'll have that previous pointer from that first node point back to the new node. And we'll do that by saying head dot previous equals new node. And the code looks like this head dot previous equals new node. And then we'll move the head pointer over to the new node. We'll do that with this head equals new node. And that adds that into our doubly linked list. So let's add this code in with the rest of our code.

Now the only thing left to do is to increment the length by one. So we'll look at this code in a moment in IntelliJ. And when we do. Will create a linked list with the items two and three in it, and then we'll prepend the one node and it will be one, two, three. So now let's flip over to IntelliJ. So there is our prepend method there that has been added to our linked list class. And then I'll come up to this tab that contains our main class that also contains our main method.

And with these two lines of code here we'll create our linked list with the values of two and three. And then with this line here we'll print that out. So I'll run this. And you can see that we have a doubly linked list with nodes with the values of two and three. So I'll come up here and then I'll add this line of code. Which will prepend a node with the value of one, and then we'll print this out again. And I'll run this. And now we have a doubly linked list with nodes with the values of one, two and three.

And that is our method for prepend.

----------------------------------------

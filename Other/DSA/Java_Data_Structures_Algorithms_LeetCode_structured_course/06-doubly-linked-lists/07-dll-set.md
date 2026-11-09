# 6.7 — DLL: Set

> Section 6: Doubly Linked Lists

So now let's create our set method. So with set we're changing the value of a node at a particular index. If we were successful in doing that we'll return true. And if we're not we'll return false. So let's bring up our doubly linked list. Like this. If we're going to change this value here from a three to a four, we'll say temp dot value equals four and change that value. So I'm going to change this back to a three for now. And then we'll walk through our code.

So to get temp to the correct index, we'll set it equal to get and then pass it the index. So if you'll recall, our get method will return one of two things. If the index is out of range, it will return null. If it is not out of range, it will return the node at that particular index. So what we need to do is test to see if temp is pointing to a node. So we'll say if temp is not equal to null. In other words it is pointing to a node. We'll set temp dot value to be equal to the value that we pass the set method.

So in this case that value was four. So we'll change that to a four. And since we were able to successfully change that value. We will return true. So now the conditional on this if statement will equate to false. If temp has an index that is out of range because the JIT method will return null. So if this ends up happening, we'll skip the if statement and we will return false. So this is the one method in the doubly linked list class, where the code is exactly the same as it was in singly linked lists.

But there is a difference in how the code runs and the reason for that. Is the git method runs in a different way in a doubly linked list. So remember we had that efficiency where if the node was toward the end, we could start at the tail and go backwards. So the get method will run more efficiently. But the code itself is exactly the same. So we'll look at this code in a moment. And IntelliJ. And when we do. Will build this linked list, and then we'll change the item at the index of one to have a value of four.

So now let's flip over to IntelliJ and take a look at this. So there is our set method there. And then we'll come up to our tab here for our main class. And this is where we create our linked list with the values 11 three, 23 and seven. And then with this line here we'll print this and I'll run this. And there is our doubly linked list with values 11, three, 23 and seven. So I'll come over here. And I will add this line of code, and then we'll run the set method where at the index of one we're going to change that node's value to be equal to four.

And then we'll run printlist again. And I'll run this. And you can see that the item at the index of one has had its value changed to four. And that is our method for set.

----------------------------------------

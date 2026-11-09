# 8.4 — Stack: Pop

> Section 8: Stacks & Queues

So now let's create our pop method for our stack. We'll bring our stack up like this. Pop is going to look like this. That is if the stack is not empty. So our method starts out like this. Our return type is node, which is the node that we are popping. We will return that. So we'll start out by coding for this situation where we have an empty stack. We'll say if the height is equal to zero, return null. You could also say if top is equal to null, return null either way.

So now let's code for when we do have items in the stack. Since we are returning that top node, we'll need a variable that points to it. So we'll say temp equals top. That'll do this. And then we'll say top equals top dot. Next that is top equals top dot next. And that's going to move top down to this node. Then we'll say temp dot next equals null. That is temp dot next equals null. And that will break that off from our stack. And let's put these three lines of code in with the rest of our code like this.

And the only things left to do are to decrement the height by one. And to return temp, which is the pointer to that node that we just removed. So we'll look at this code in a moment in IntelliJ. And when we do we'll create this stack. And we'll pop that top item from the stack. And we should be left with a stack that has items three, 23 and seven. So let's flip over to intelligence and take a look at this. So there is our Pop method there that has been added to our stack class.

And then I'll come up here to this tab to bring up our main class that contains our main method. And these lines of code here are going to create that stack that we just saw in the diagram. And then we'll run this line here to print this out. So I'll run this. And you can see here that we have a stack with 11 323 and seven. So I'll come over here. And I'll paste in this line of code. And that will pop off that top item and I'll run this. And you can see that our stack now contains three, 23 and seven.

And that is our method for pop.

----------------------------------------

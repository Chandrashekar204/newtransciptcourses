# 10.8 — BST: Contains - Code

> Section 10: Trees

Now we're going to write the code for our contains method. We're going to pick up where we left off in the last video with all of our steps to do the contains method. I'm going to move all of these steps down to the bottom. So we have room for our code and we'll start this out like this. Our method is contains. It returns a boolean true if the item is in the tree, and then false if it is not. So the first thing we'll do is say if root is equal to null, return false.

That is this situation where we have an empty tree. And we'll do that with this line of code. If root equals null, return false. And we can remove that from our list. And then we'll create our temp variable temp equals root. We'll do that like this node temp equals root. We can remove that and then we'll create our while loop. While temp is not equal to null. We'll remove this. Now we're going to create our three scenarios that go inside of the while loop.

So if the number we're looking for is less than the one that we're comparing it to, we're going to go left. We'll do that like this. If the value that we're looking for is less than temp dot value. So let's say we're looking for the number 27. For example we're going to set temp to be equal to temp left which moves this down. So let's remove that and we can remove this from our list. Then we'll say else if it is greater than we'll go right. We'll do that like this.

If the value that we're looking for is greater than temp dot value, let's say we're looking for the number 82. Then we'll set temp to be equal to temp right. Which does this this. So we'll remove that and then take this off of our list. And then the other alternative is that if it is equal we'll return true. So we can just say else return true. So the only thing left on our list is if we break out of our while loop, we will return false. So let's look at a couple of scenarios from just the while loop down.

So let's just focus in on this and we'll bring a tree up like this. And then we'll walk through how the code will work. If we're looking for a node that is in the tree, and then we'll do it again for a node that is not in the tree. So first we're going to look for the number 27. So we'll say while temp is not equal to null and it's not equal to null. And the number we're looking for is less than 47. So this if statement will run. If value is less than temp dot value then we're going to move this to the left.

Then we come up and run this while loop again. And 27 is greater than 21. So we'll run this code here which is going to move this to the right. Then we'll run the while loop again. Then this code will run and we will return true. So let's move this temp variable back up to the top and look for the number 17. So we'll run the while loop 17 is less than 47. So we'll run this and that moves temp down. Then the while loop runs again. It is less than again.

So we're going to go to the left again, and then the while loop will run again. And 17 is less than 18. So we run this again and temp is now equal to null. So this time when we run the while loop. Temp is equal to null. That breaks us out of the while loop. And then we come down here and return false because that number is not. And our binary search tree. So let's drop this out and we'll bring back the rest of our code like this. And I wanted to point out one other thing.

You actually don't need this line of code. And I left it in there because if you're actually writing out the steps to see if your binary search tree contains a particular value and you're writing this out on paper, you probably are going to put this in as one of the steps. So let's remove this and look at how this code would work if we have an empty tree like this. The first line is going to be temp equals root, which is going to set temp to be equal to null.

Then when we try to run this while loop temp is equal to null. So the while loop never runs and we go straight down here to false. The code does run either way just fine. Now, if you do a search for how to write the contains method, you'll see that a lot of the versions online contain that if statement. And you can see why. Because if you're going through the steps, it just seems natural to put that in there. And when you put it in, the code works.

So you'll see a lot of versions where they have not taken that out. But I think this is a little bit cleaner to do it this way. So we'll look at this code in a moment in IntelliJ. And when we do we're going to create this tree. And we're going to run the contains method on the number 27. We'll expect that to return true. And then we will also run the contains method on the number 17. And we will expect that to return false. So now let's flip over to intelligence and take a look at this.

So there is our contains method there added to our binary search tree class. And then I'm going to come up here to our main class where we have our main method. And this line here creates our new binary search tree. And then with these lines we actually create that tree that we just saw in the diagram. And then down here we're running the contains method twice. First on the number 27 and then on the number 17. So we would expect this to return true for the first one and false for the second one.

So I'll run this. And you can see that we got true for the first one and false for the second one. So it looks like we have a working method for contains.


########################################

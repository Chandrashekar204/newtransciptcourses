# 15.4 — Heap: Insert (Code)

> Section 15: Heaps

So in this video we're going to write the code for insert. So we'll pick up where we left off in the last video with our helper methods. And insert is going to go in right below these. So I'm going to remove these. And then I'm going to bring insert in like this. And then I'm going to focus in just on the insert method. So I'll bring in this tree to start with. This will be represented with this array list. And we're going to insert the value of 100.

Which is to say that we're going to add 100 to the array list here. And we'll do that with this line of code where we say heap dot add and then just pass it the value. And then we're going to have a variable called current. And current is going to be set equal to the index of this new node, which in this case is going to be four. So that effectively points current here. And we'll do that with this line of code. Current equals the heap size minus one.

So the size of the heap is five. And the last index in the heap is four. And that's going to bring us to our while loop. And the insert intro video I mentioned that there are two different conditionals that can break us out of the while loop. But for now I'm going to say while true, now this true is going to get replaced with those two conditionals, but I'll add those conditionals when we get to the point that they apply. So now I'm going to focus in on this while loop.

Now the next thing we want to do is compare that new node's value of 100 to its parent's value. And because it is greater than we want to swap these, which is to say in the array list, we're going to take these two values here and swap them. So we'll do that with this line of code that uses that swap helper method. And it swaps the value at current with the value at the parent of current. So now that those have been swapped, the next thing we want to do is move current up here to continue pointing to this new value.

That is to say, we want to update this to be equal to the index of one. So I'm going to move this back over here. We'll move that with this line of code that sets current to be equal to the parent of current, which is going to move this up. Then we're going to run the while loop again. The first thing we'll do is swap current with the parent of current. That's going to do this in the array list. What that's going to look like is just swapping these two values.

Then we're going to have current be set equal to the parent of current, which is going to move it up here. And because this node has bubbled up all the way to the top, this is the first conditional that we want to break us out of our while loop. We only want to run this while current is greater than zero. If current is ever equal to zero, that means this value has bubbled up all the way to the top and we want to stop. So now let's bring in the rest of our code like this.

And now let's look at adding the value of 75. We're going to add that to the array list with this line that adds the 75 like this. And then we're going to set current to be equal to the size of the heap minus one which points current here. So now I'm going to focus in on our while loop again and move that up to the top. And we're going to run this line of code that swaps that 75 and the 61 in the tree. It's going to look like this. And in the array list we're going to take these two values and swap them like this.

And then we're going to set current to be equal to the parent of current which moves current up here. And this brings us to the next conditional in the while loop because 75 is not greater than 100. So with that other conditional we're going to say we're only going to run this when current is greater than the parent of current. And because that is not the case here, we're going to stop running the while loop and we have a valid heap. So now let's bring back the rest of our code again.

And this is all of the code for insert. We'll look at this code in a moment in IntelliJ. And when we do we'll build a heap that looks like this. And we'll print this out. And then we'll add the value of 100. I'll just put this in its final spot like this. And in the array list, the final version of that is going to look like this. And then we'll print out this array list. And then we're going to add the value of 75 in the array list. The final version of that is going to look like this.

And then we'll print this out. Again. So now let's flip over to IntelliJ and take a look at this. So this is our heap class here that creates the heap and initializes it as an array list. And then with this this is where we have get heap. And I'll scroll up. And these are the helper methods that we created. And then I'll scroll up again. And this is the insert method that we just wrote in this video. So now I'm going to come up to the main tab that has our main method.

So these lines here will create that initial heap and print it out. And then these lines here will add the value of 100. And then print the heap out again. And then with these lines we'll add the value of 75 and print the heap out again. So I'm going to scroll up again. And this is the expected output. So I'll run this. And you can see that our output matches our expected output. So it looks like we have a working method for insert.

----------------------------------------

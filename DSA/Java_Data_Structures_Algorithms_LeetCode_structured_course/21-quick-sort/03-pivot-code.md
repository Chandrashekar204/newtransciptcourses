# 21.3 — Pivot: Code

> Section 21: Quick Sort

So now we're going to write the code for our pivot method. We're going to run that on this array which I'll represent like this. And shrink this down into the corner to make room for our code. So before we get into the code for the pivot method itself, one of the things that you saw when we did the intro video is that we're swapping items a couple of different times in the method, and we've seen code similar to this a couple of times in the course for swapping two values in an array.

But since we're doing it twice, I'm going to create a separate helper method, and I'm just going to call this swap. And we'll pass this the array and the two items that we want to have swapped. And that'll clean our code up a little bit. And now that we have this let's get into the pivot method. So we pass this the array and that we pass it a pivot index and an end index. So in this case the pivot index is going to be zero. And I'm going to put an arrow on the diagram down here for that I'll call it pivot on the arrow.

But I like to call it pivot index in the variable to emphasize that this is the index and not the value at that index. And the end index will be the last item in the array. So we'll create another variable called swap index. We'll set it equal to pivot index. I'll just call that swap on the arrow. But once again I like to leave the index in the variable name to emphasize that it's an index. And now we'll create the for loop so we can do all of the comparisons moving through the array.

So our variable I is going to start out being equal to pivot index plus one. And then we're going to go to the end of the array. So I'll bring I in like that. So inside the for loop we'll start doing comparisons. We'll say if the item at array at the index of I is less than array pivotindex. And in this case that is not the case because six is greater than four. So I will color that in gray since it's greater than. And we'll run through the for loop again, which is going to move the I over.

And now when we run this if statement, the conditional is true because one is less than four. So we need to move swap up. So we'll say swap index plus plus that moves that over to the six. And now we're going to swap the values at swap index and I. And this is where we use that helper function that we just wrote. We'll say swap pass it the array and give it swap index and I and it will swap those two values. So if you continue running through this for loop, you will eventually end up with an array that looks like this.

And now what we need to do is swap the items at pivot index and swap index. So we'll use that swap helper function again, pass it the array and pivotindex and swap index and that will swap those two items. And that item at the swap index is now sorted. So I colored that in green and then we want to return. The swap index. And that index in this case is going to be three. I want to emphasize that this is the index not the value for that is at that index we're actually returning the index.

And that is all of our code for the pivot method. So we'll look at this code in a moment in IntelliJ. And when we do we'll start out with an array that looks like this. So now let's flip over and take a look at this. So this is all inside of our quicksort class. And we start out with our swap helper method that we created. And here is our pivot method. And then I'll scroll up again so we can focus on our main method. So we'll create an array called Myarray.

That's the array that we just saw. And then we'll run pivot on my array and pass it the indexes of zero and six. So we have the entire range of the array. And that index that it returns will store that in an integer called returned index. So with these next two lines I want to emphasize that the pivot method does two different things. First it returns an index. So we'll print that out. But the other thing it does is it rearranges your array. It does both things.

So with this line down here we're going to show what the array looks like after we run pivot. And I'll run this. And you can see up here that it's returned an index of three, but it's also changed the array. We now have four in the middle. All the items that are less than four are on the left, and all the items that are greater than four are on the right. And that is our method for pivot.

----------------------------------------

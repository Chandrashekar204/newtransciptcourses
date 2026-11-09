# 12.9 — HT: Interview Question

> Section 12: Hash Tables

In this video, we're going to go over a very common interview question that involves arrays and hash tables. And there are different variations on this question, but I'll show you one version. So I'm going to bring up a couple of arrays like this. And the objective is to see if the two arrays have an item in common. And obviously they both contain five. But how do you write the code to do that. So this is pretty simple to do with some nested for loops.

But the problem is if you have nested for loops it's very inefficient. So that is not the answer they're looking for. But so we can compare the two solutions. Let's start out with the inefficient solution and look at how that works. So first you would create a for loop to go through the first array. So you get this first item. Then you have a second nested for loop that compares that value to all of the values in the second array. Then you move that first array over to the next one and compare it to every single value in the second array.

And then we do it again until we finally find our match. So in this situation the arrays are three items long and we had nine operations. So that is O of n squared. So let's go quickly through the code to do this. I'm going to shrink this down. And we're going to call this method item in common. We're going to pass it the two arrays. We'll call them array one and array two. And then we'll return a boolean true if there is a match and then false if there is not.

So we'll start out with this for loop here. So if you haven't seen a for loop like this before this just is going to loop through array one. And then I is going to be equal to the value at each index. So it'll first be equal to one and then three and then five. And then we'll have another for loop that does the same thing on array two. And if these are ever equal we'll return true if we go through the for loops and we don't find any matches then we'll return false.

Now let's flip over and take a look at this code in IntelliJ. So that is the code that we just wrote right there. And then I put our main method inside of the same class. So down here we have our two arrays. Array one and array two with the values that we just saw. And then down here we're going to run item in common with array one and array two. And in this case we should get true. So I'll run this. And you can see up here we get true. And then I'm going to come down here to array two.

And I'm going to replace this five with a six. And now when we run this we should get false because we don't have any matches. So I'll run this again. And you can see that we get false. So this code does work. It's just really inefficient because it has the nested for loops. So now let's flip back. So now let's look at how we can do this much more efficiently with a hash table. So we'll bring our hash table in like this. So now what we're going to do is we're going to loop through that first array.

And what we're going to do is add these values as keys. Remember these are key value pairs. And the value. Is going to be true. And then we'll do the same thing for the three. We'll have that value be true. And then we'll have the same thing for the five. So then we'll have a separate for loop. But this will not be a nested for loop to go through the second array. So we'll check to see if that value of two is on our hash table. And that is an O of one operation to do that comparison.

And then we'll do the same thing for the for and the same thing for the five. And of course that is in the hash table. And in that case, we'll have our method return true. But if you look what we did here, we ran through each array. One time. We looped through the first one straight through and then the second one straight through. So we've said before that N was three. So this would be O of two n. But remember we drop constants. So now this is O of n.

So doing it this way is much more efficient. O of n is much more efficient than O of n squared. So now let's look at how we would code this. Now the way this starts out, this line of code looks exactly the same. But we'll start this out by creating a hash table. Technically, this is going to be a hash map, but a hash map is a hash table. And we'll call this my hash map. That will create a for loop, just like we did before, to loop through array one.

But inside of this for loop, we're going to put the value from each item in the array. That will be the key, and then the value will be true in the key value pair. That will have a second for loop, where we just check to see if J is in our HashMap as a key. If there is ever a match, we'll return true. If we go through this loop and we don't find a match, we'll return false. So now let's flip over and take a look at this code in IntelliJ. So there is our new item and common method there.

So one of the things I wanted to point out down here in our main method, this is all the same down here. So when we call the item in common method and pass it array one and array two, you're calling this method exactly the same way the method is written in a different way. But to the end user that might use this method, they are calling it exactly the same way as they did before. So you can see here that array one and array two do have an item in common.

They both have a five. So we would expect this to return true. So I'll run this. And you can see that it returns true. And then I'll come down here and change this five in array, two to a six. And now when we run this. It returns false. So the key takeaway here is that either way that you write this, it will work. But can you get this done and make it O of N is the real interview question.


########################################

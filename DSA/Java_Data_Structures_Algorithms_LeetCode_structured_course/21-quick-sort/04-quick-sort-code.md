# 21.4 — Quick Sort: Code

> Section 21: Quick Sort

So now we're going to write our code for quicksort. I'm going to bring up the array like this. And previously we had written the code for pivot where we had a pivot point like this. And then we ran the method and ended up with an array that looked like this. And we returned the index for this item. So in the quicksort method we're going to run pivot get it to here. And we'll run quicksort again on these items. And then we'll also run it on these items.

So let's put this array back the way it was. And we'll shrink this down to make room for our code. And we'll start it out like this. We'll call it quicksort. We're going to pass it the array, but we're also going to pass it the left and right index. So in this case we have an array with seven items in it. So we're going to pass it the indexes of zero and six. And then our return type is void which means this is going to be sorted in place. So now we're going to run our pivot method.

We'll do it like this. And we're going to pass these three variables to the pivot method. And when we do that pivot is going to do two things. It's going to rearrange that array to look like this. But it's also going to return this index. And we'll store that in that variable called pivot index. Now that we have that index, we'll run quicksort on everything to the left of that index. And then on the right. So starting with the left it'll look like this.

Quicksort we pass it the array and then the indexes in that range. So left is this left from up here. And then pivot index minus one. Is this index down here. So I'll bracket this. It's this range here. And then we'll do the same thing on the right where we pass it the array. And then the index of pivot index plus one which is going to be that six there. And then right, which is right from up here, which is this index over here. So I'll bracket that.

And now let's enlarge this and walk through the rest of the steps. So we'll start with the left, since that will be the first one to run. Our pivot index is going to be two. And then the one is less than and the three is greater than. So we'll just do this. And now that two is sorted. And when we do this we're going to run quicksort on the left and the right. And there's only one item in each of these. So we know those are sorted and we're done.

That is our base case. And then we do the same thing over here where our pivot index is going to be six. Seven is greater, five is less than we swap these two. And then we swap these two. And the six is sorted. And that we do quicksort on the left and the right again. And those two are sorted. So let's shrink this down and bring our code back. The one thing that we don't have in our code here is some type of base case. So we're going to say if left is less than right.

If that is the case then we will run this. So for example when we started the left index was zero and the right index was six. So left was less than right. And we were able to run these next three lines of code. So if left is ever greater than or equal to right we won't run this. So that is all of our code for quicksort. We'll look at this in a moment in IntelliJ. And when we do we'll start with an array that looks like this. And then we'll run our quicksort method and sort that array.

So now let's flip over and take a look at this. So there's our quicksort method there. And then down here we create the array that we just saw. And then we'll run quicksort on that array and we'll pass it the left and right index. The array has seven items so the indexes are zero and six. And then down here we'll print out that array. And I'll run this. And you can see that we have a sorted array one through seven. So now that we have this, I'm actually going to make a change to our quicksort method.

And the reason why is I don't want to have to pass these indexes or have an end user that's going to use this method have to pass these indexes. I want to be able to just pass the array called my array. So I'm going to come up here and change the name of this from quicksort to quicksort helper. You'll see that temporarily. Some of the stuff is in red, but I'll change this. And then finally change this one. So now what I'm going to do is I'm going to add a new method called quicksort.

That looks like this. So now quicksort is just going to call quicksort helper. It'll pass it the array a left index of zero. And then the right index will be the length minus one. So now when I come down here, I can remove these indexes of zero and six. And I can just pass it the array. So now I'll run this. And you can see it outputs the same sorted array. The difference being that we can call this method down here with just the array. And that is our method for quicksort.

----------------------------------------

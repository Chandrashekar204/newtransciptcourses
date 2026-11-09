# 19.2 — Bubble Sort: Code

> Section 19: Basic Sorts

So now we're going to code bubble sort. We'll pick up where we left off in the last video, except I'll take this and shrink it down into the corner to make room for our code. So we'll call this bubble sort and we'll pass this an array of integers. So one of the things we talked about in the last video is our first pass through this array that has six items. There will be five comparisons. And then the second time there's four and then three and so on.

So in our first for loop, we're going to say that I is equal to the length of the array minus one. So the length is six. So the first time we're going to go through five times. And then you can see here that we are decrementing this each time. In the second for loop. We're going to run this I times. So that'll be five times. The first time we do it and then four and three, etc.. So inside of this for loop is where we will check to see if two items need to be switched.

So we'll say array at the index of J. That's this item here. If it's greater than j plus one which is the next item, then we'll switch these. So we'll switch these with three lines of code. I'm just going to bring them in. And then we'll walk through how this works. So we're creating a new integer temp. And we're setting it equal to the value of the item that's at the index of J. So to show this graphically temp equals this value here. Then we'll set the item at the index of J to be equal to the value of j plus one.

So that's going to do this. This moves that value over there. And then we say at the index of J plus one we're going to set that equal to temp. And that copies that in there. And that's how we're going to swap our items. So if we keep running these for loops it'll cause the entire array to look like this. It will sort the entire array. So notice that we don't have a return statement. So what we're doing with this type of sorting algorithm is we are sorting the existing array in place.

We're not making a copy and then sorting it and then returning it. We are actually sorting the original array in place without making a copy of it. So that's why the return type is void. And this will be the case for most of our sorting algorithms, but not all. When we get to merge sort, merge sort is actually making copies and then putting them together and then returning a copy of the array. But because we don't have to make a copy of the array and we are sorting it in place.

The space complexity of bubble sort is O of one, which basically means we don't have to make a copy. So this is all of our code for bubble sort. We'll look at this code in a moment in IntelliJ. And when we do we'll start with an array that looks like this. And we'll run bubble sort on that array and sort it. So now let's flip over and take a look at this. So before we get started here, I want to zoom up and look at the side panel and show that we're in the algorithms package, and that it has a source package that includes all of our sorting algorithms.

And then we are starting with a package called Bubble Sort. And it also contains a class called Bubble Sort. So I'm going to close this side panel. So you can see here that we have our class bubble sort. And this is the method that we just created. And I'm going to scroll up just a little bit here. And down here we have our main method. In this case, I put our main method inside of our class where we have the method that we're testing. So this is the array that we're going to pass bubble sort to be sorted.

And then with this line here we'll run bubble sort on my array. And then down here we're going to print that array out and show that it's sorted. So I do want to come down here and explain this I'm highlighting this. So we have to use arrays dot to string and then pass it my array to print this out. In other words, the array has to be converted to a string before you can print it. So I'm going to delete this and just type in my array. If you do it this way, you're going to get this wavy underline with this.

And if you come up here and just hover over this, you're going to get this box. And it asks you if you want to wrap with Java util arrays to string. So you can just click on this and it will do the rest for you. So that's not something you actually have to memorize if you just type in my array. In this case, it will prompt you and allow you to just add that. Okay, so now I will run this. And you can see up here that we have a sorted array one through six.

So it looks like we have a working method for bubble sort.

----------------------------------------

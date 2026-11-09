# 8.8 — Adding Arrays to Arrays with concat()

> Section 8: More on Arrays & Iterables

There also is a useful method for adding elements to an array and returning a brand new array which again can be useful in situations where you want to create a copy of an array, maybe after adding new elements to it, let me show what I mean. I'll comment this out and instead create stored results here by using my test results and now here, there is the concat method which we can call. The concat method allows you to concatenate, so to add elements at the end of an array.

Now therefore it's of course a bit like push, with push you can also add items to an array, by the way also more than one item, they will be added at the end but concat actually here takes an array or multiple arrays but not individual numbers or items in general but arrays, one or more arrays and combines these arrays with this array. So it does not add these arrays as new nested arrays, that is what would happen if you pushed an array, that would add this as a single element in the existing array hence creating a nested array, concat on the other hand will pull out all elements of the array you are passing here and add them as new elements to the existing array and it will then also return a brand new array. So it will create a copy of the array, add these items and return that copied brand new array, hence creating a new place in memory and a new address.

So here for example, if we have 3.99 and 2 and I concatenate this here, what you'll see is if I reload, here we get the array with 3.99 and 2 at the end which are the two values I just added. And of course please also note that when I push 5.91 to test results, this does not end up in my stored result which is the first array I output here because concat returned a brand new array. So you see no 5.91 here in the first array, only in the second one.

So that's also useful, concat can be really useful if you have array data and you want to combine it with an existing array and the fact that you get a brand new array is also quite convenient because that often avoids problems where you manipulate an existing array when you actually didn't want to do that.

----------------------------------------

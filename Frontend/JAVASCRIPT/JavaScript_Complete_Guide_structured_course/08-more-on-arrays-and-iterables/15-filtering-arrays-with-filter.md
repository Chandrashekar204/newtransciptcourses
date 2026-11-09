# 8.15 — Filtering Arrays with filter()

> Section 8: More on Arrays & Iterables

Now slowly we're coming to an end of interesting array methods but we're not there yet. Another very useful array method is one that allows us to filter the elements in an array. Now we had a look at find and find index which was really nice for finding single elements but what if you want to basically reduce the amount of elements in your array based on some filter, let's say here we only want to have prices that are greater than 6, so that only 6.59 and 10.99 are included.

Well for that, we can create a new constant for example filtered array and then use the prices array and call the filter method on it. Now just like all these other array methods, filter will return a brand new array, so it will not touch the original array but instead return a new one which we then store here and which I therefore want to output down there and the filter method also takes a function and this function here works just like the function you pass to find and to map and so on. You get the value it's currently looking at because this function which you pass to filter is again executed for every item in the array on which you call filter, so on every price in this example. You get the index here and you get the original array if you're interested, though you will rarely use that last argument as you already saw here.

Well and then here again you need to return something, so the filter method is a method that expects the function which you pass to it to return a value, to be precise it wants true or false. It wants true if the item on which this function is currently executed should be kept in the newly created array and false if it should be dropped. So here I want to keep everything where the price is greater than 6, so I will return price greater 6. This boolean comparison here will return true for any item where the price is greater than 6 and therefore any item where the price is greater than 6 will be kept, other items will be dropped from that newly created array, the old array is not touched, so the prices array itself is not touched.

So if we save that and reload, filtered prices here indeed only has two values which are my two values greater than six. So filter is also really useful for filtering an array as you can guess and therefore this also is an operation you'll find yourself do quite frequently.

----------------------------------------

# 8.13 — Transforming Data with map()

> Section 8: More on Arrays & Iterables

Now in the end what we did here in the last lecture with ForEach is we transformed the array, right? We in the end transformed it from an array of prices into an array of objects, where of course also each price changed. We can do that with ForEach here but there is an easier way because what we have to do with ForEach or with for loops is we have to manage our new separate array onto which we push these transformed items, we can do that but there's a shorter alternative.

So if I copy that and then comment it out and repeat this example, let's get rid of the tax adjusted prices array like this, let's get rid of this common here also to save some space and now instead of ForEach, we can use map, another special method available on arrays. Now map has the job of taking an array, running a function which has this form on every item in that array and then and that's important, that function should now return a new element for every element in that array, a possibly transformed element.

So ForEach, this function which you pass to ForEach doesn't have to return anything, you can do whatever you want in ForEach. For map, this function which you pass to it has to do something, has to return something, it has to return the map that transformed the new element for that array. So here I would return price object for example and that means that now this will replace every element in the array on which we call map with this adjusted element. However that's not totally true, it doesn't really replace it, the original array stays untouched, instead it returns a brand new array with a brand new address in memory where every element has been changed.

So now here, we can get our tax adjusted prices, store it in a constant and prices themselves will be untouched as I can prove by logging them here, tax adjusted prices however will be the transformed prices with the help of map. So if we save that and reload here, we see that is the original array, nothing changed there and here we have the transformed array with our object in there, so that did indeed change. So map is a really nice method if you want to transform an array because it makes changing elements and getting a brand new array based on these changed elements super easy.

----------------------------------------

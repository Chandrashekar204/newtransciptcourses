# 8.9 — Retrieving Indexes with indexOf() /& lastIndexOf()

> Section 8: More on Arrays & Iterables

Thus far when we worked with arrays, we always talked about adding items or selecting single items or a range of items. Now you also encounter use cases or scenarios where you have an array of data and now you want to find out at which index in that array a certain item sits, so that you can use that index to replace the item or for whatever reason you might have. Let's say we want to find out where in this array this item with the value of 1.5 lives.

You can do this with another method that is available in Javascript on every array, let's run it on test results here and that's the indexof method. Now as the name suggests, this returns the index of the value you're passing as an argument here. So for example here we could search for 1.5, you also have an optional second argument that would allow you to specify a starting index so that you for example only start searching on elements with index 2 or higher.

Now I will search the entire array here and hopefully, get a result of 2 which is the index of this 1.5 value here. So if we reload this, indeed I see 2 here. Now there are a couple of important things to understand, for one if you have the same value more than once, like I do here now that I added 1.5, then this will stop after it found the first matching value, so it will return you two, it will not return you all indexes of all items that have that value.

So if I repeat that code with that new item added, you'll see I still get to here even though I have another item of the same value at index four. So that's one thing, indexof stopped once it found the first element that fits this description. Now if you want to start searching from the right, there is last indexof, you can use that to search from the right and therefore it will now stop at this index, so it does the same as index of, just starting from the right.

So if I now reload, we see an index four here because it started from the right. Another important gotcha regarding index of and last index of is that it works fine for primitive values but not for reference values. Let's say we had our person data array here and there we have an object with name Max in there and another object with name Manuel, so it's an array of two objects. If I want to find out where Manuel is, then of course we could try person data index of and pass in that object, right?

We could try that. If we do this and I reload my page, we'll get -1 though, -1 is the return value of index of and last index of if it couldn't find any entry, then it always returns -1. So it doesn't throw an error, it doesn't return false or anything like that, it returns -1 if it didn't find anything. Now the reason for this behavior of course is this reference value thing. Objects are reference values and therefore in the end here, I'm creating a brand new object and I'm passing this to index of and behind the scenes, index of is of course comparing all values to the value I passed to index of and because two objects even if they look similar are never similar, it doesn't find any match and therefore it returns -1.

So index of won't work if you have objects in there but no worries, we'll have a different method that does work if you do have objects in there.

----------------------------------------

# 9.7 — Property Types & Property Order

> Section 9: More on Objects

Now besides string property names, there are two other kinds of values you can use for your property names and that would be numbers and also symbols. Now again let's ignore that symbol thing but let's have a look at a number. Now actually it's not too surprising that we can use numbers because that's in the end what an array does, it assigns indexes to our values, well in the end as you know, an array is an object, so in the end it's just an object which automatically assigns number keys to the values you added.

So here, we could also add a number key and for a person, it doesn't make too much sense, what would be a number here but we could enter 1.5 here as a key and assign a value of hello or any other value. So now we have this here as a number, again behind the scenes it will still be coerced to a string but you can use it as a number here and access it as a number. So for example here if I store hello in 1.5 or in any other number of your choice, not including negative numbers though, so negative numbers are not allowed, must be a positive number, zero or higher but if we store that here, we can access this here with console log person and now again not with the dot notation though because this here will not work.

You see I'm getting an error here, this is simply not syntax Javascript understands. So therefore here, you also have to use square brackets but now important, you don't have to wrap this in quotes here, now here Javascript clearly detects that this should be a number, so now since it's in the same pair of square brackets, this is evaluated as one thing and therefore as one number and hence if I save this, we see if I reload here hello down there.

Now you can also wrap this in quotes if you want, so you can do that and then reload and it will work as well because as I mentioned, Javascript automatically coerces values to strings, so it kind of translates it to a string anyways behind the scenes but you can also access it like this. Now storing numbers in normal objects is probably not something you'll do too often but it works and you see, this is how you can then access this. Now one word about the order of properties, a common question is, how are these properties ordered in a Javascript object?

Now let's have a look and let's console log the entire person here and if we do so, if we reload this, we now see the object here and now here's something important. If you expand it here, you automatically get a sorted view of that, so here you always have that sorted. Now if we have a look at that unexpanded thing however, we see that we have the order in which we added our properties, so that's how our properties, our key-value pairs are ordered, they keep the order in which we add things.

So we have first name, hobbies, greet, 1.5 and isAdmin and indeed we have first name, hobbies, age is deleted but then hobbies, greet, 1.5 and then isAdmin is added last and that's exactly what we see here. Now there is one important exception which I quickly want to show you here, if we have an object which only consists of number keys, let's say you have five with a value of hi and then one with a value of true, a string but can be any value, then if you output numbers, you see indeed here already that changed, so here that is sorted. If you have an object with only numbers, then the numbers will be sorted and that's important to keep in mind, numbers will be sorted, otherwise if you have string keys, the insertion order will be kept.

That's how Javascript object properties are ordered by Javascript.

----------------------------------------

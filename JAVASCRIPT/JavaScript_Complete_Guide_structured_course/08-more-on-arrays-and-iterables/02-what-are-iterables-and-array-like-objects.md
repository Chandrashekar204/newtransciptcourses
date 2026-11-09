# 8.2 — What are "Iterables" and "Array-like Objects"?

> Section 8: More on Arrays & Iterables

So what's an iterable in Javascript? An iterable can be defined technically, there it's basically an object or any objects that implement the iterable protocol and have to is @@iterator method with the symbol iterator property. Now symbols are a special type of values in Javascript, we'll dive into them way later since they're really niche and specific and therefore the human readable definition of an iterable in the end is that we can use a for/of loop on it.

Yes, it's indeed as simple as that, we can loop through it with for/of. Now the important thing is that not every iterable in Javascript is an array. We work with arrays thus far but there also are other iterable objects, like a node list for example which we saw in the last course module but also strings and also maps and sets which we'll have a look at later. Now there also is another term which I already used and that's array-like and that's actually not the same as an iterable, both iterable and array-like are official terms in the Javascript language.

Now what are array-like objects therefore? Again, the technical definition is here, much more readable, that an array-like object are in the end any objects that have a length property and use indexes to access items, it's as simple as that and I'd say it is also pretty clear to us humans. Now just as with iterables, not every array-like object is an array, that's why it's called array-like. We have array-like objects, like node list and string. Node lists and strings are objects that have a length, that have indexes and where we can use for/of and still, they're not real arrays because as you will learn in this module, real arrays have a couple of interesting behaviors and also a bunch of important methods available to them which do not exist on these array-like or iterable objects.

Now with these definitions out of the way, let's dive a bit deeper into arrays before we then also have a look at other array-like objects and iterables.

----------------------------------------

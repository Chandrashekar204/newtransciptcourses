# 8.22 — Maps & Sets - Overview

> Section 8: More on Arrays & Iterables

That is it for arrays, lot of information about arrays, lots of things you will of course see throughout this course and in many of the projects you will work on as a Javascript developer. Now definitely of course take the time to go through these things again, have a look at some of these important array methods, get acquainted to them, practice with them, get a feeling for them. For now I will move on to two totally different constructs or iterables though or not totally different but quite different which also exist besides arrays and that are maps and sets.

So in Javascript, we got three major iterable data structures you could say. We got arrays but we also got sets and we got maps. Now one important thing right away, arrays are the most important one, the one you work with most often and objects of course but objects also are a bit more than just a data container, something you'll especially see once we dive deeper into objects in the objects deep dive module. So when we talk about lists of data or storing kind of connected data, arrays are the main storage for storing that data and there you can have nested data of any kind, of any length, you can mix data types.

It's an iterable as you learned with many special array methods available, all these great methods which we used and a couple of key characteristics of arrays are that the order of elements is guaranteed, so the order doesn't magically change. Duplicates are allowed, you can have the same number twice in an array for example and you have a zero based index to access elements, these are things you of course learned throughout this course and especially throughout this module.

Now what are sets then? Sets are also data structures which store nested data of any kind in length, so you can have sets of arrays, sets of numbers, anything goes and it's an iterable with some special set methods but not with all these array methods. So these array methods are not supported on sets, instead there are standalone set methods which are mostly there to manage the data in the set though, not for transforming it and so on, though you can always, what you already learned, convert any iterable to an array with the array.from method.

Now what are the key characteristics of a set and how does it differ from an array then other than that it misses some methods? Well in a set, the order of elements is not guaranteed which might sound bad but that isn't necessarily a problem, you don't always need a specific order and also important, duplicates are not allowed. This makes sets a great choice to store data where you don't want duplicates, for unique IDs or anything like that. You also have no index based access, instead you just have an access that allows you to get a specific value if you looking for it and then you can see whether it's in the set or not.

Now maps are yet another data container where you store key-value data of any kind in length and that's a bit like an object where you also have key-value data, one important difference is that in an object, you may only have strings or numbers as keys or symbols but we haven't learned about those yet, in maps you can use anything as a key. You can have an array as a key, you can have another object as a key and that offers you more flexibility.

It's an iterable with some special map methods but not with the array methods, again just as with the set, the methods which you have here are mostly there to help you manage the items in the map and here, the order is guaranteed, that's by the way not the case for objects, there the order of the key-value pair is not guaranteed, often that doesn't matter because you retrieve values by key anyways and you don't care where it's stored, well nonetheless here it is guaranteed. Duplicate keys are not allowed but values can be duplicated throughout this map and you access values by key.

So let's now work a bit with these data structures and then get a feeling for when we use them and how we use them.

----------------------------------------

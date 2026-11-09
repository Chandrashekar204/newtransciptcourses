# 12.1 — Hash Table: Intro

> Section 12: Hash Tables

So now we're going to do our introduction to hash tables. I'm going to bring up an address space here. And we're going to create this address space by just creating an array. And then in this array we're going to store key value pairs. So what I'm going to do here is I'm just going to do the inventory for a hardware store. So one of the things that we would have in inventory would be nails. So this is what's referred to as a key value pair. So nails is the key.

And then a thousand would be the value. So when a couple of videos we will be writing the code for a hash method. I'm just going to represent that graphically here. Like this. And what we're going to do is we're going to run the hash on the key and the key value pair. So every letter has an Ascii text numerical value. So what we're going to do is run a calculation on all the numbers that are associated with these letters. So we'll run this through the hash.

So first we are going to get our key value pair back. The hash is only run on the key and gives us an address. That address is going to be one of the indexes in the array. And that's where we store our key value pair. So now let's look at a couple of characteristics of this hash method. First it is one way. So when you have a key like nails, and you run this through the hash method and you get an address, the thing that you cannot do is do it the other way and run two through this and get nails.

It is only one way. The other thing is that the hash method is deterministic, and what that means is every single time we run nails through this, we will always get the same address. So this hash method is both of these things one way and deterministic. So let's bring back our address space here and just look high level how we would write methods to use this hash method. So we will create a set method where it takes a key and a value. And let's say we pass this nails and 1000.

When we run this through here we're going to get our key value pair. But the hash method is also going to give us an address where we're going to store this. So we'll put that up there. And now let's do a few more of these. We'll say set screws. We run this through here. We get an address and a key value pair. And that goes at six. And then we'll say nuts. And we'll run that through the hash and we get the address of two. So in this situation you get what is called a collision because you already have something at the index of two.

So what you don't want to do is just overwrite this. You want to be able to keep both. So there are multiple ways of storing multiple items at a particular address. And we'll talk about that in some more detail in an upcoming video. So let's just add one more. So we have a more filled out hash table like this. So now that we've set a bunch of these, let's look at an example of our Get method. So if we say get bolts we can run bolts through this same hash method.

And get the address. Remember that hash method is deterministic, which means if you put bolts in there, you will always get the index of four. And then we'll write our get method to return the value that's associated with that key value pair. It'll be a little bit more complex if we have something like this. Get nails. We run this through here, we get that. Number two, we have multiple items here. So we have to have a way of going through all of the keys that are going to be at a particular index, and then returning the value associated with that particular key.

And that is our quick overview of hash tables.

----------------------------------------

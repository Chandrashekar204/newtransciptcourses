# 6.5 — Functions are Objects!

> Section 6: More on Functions

So functions in objects is a thing, what if I would tell you that functions themselves also are objects? I can prove this, if I console log typeof start game, you might remember this typeof operator, we used that earlier in the course to find out what the type of an array and of a number and so on is. Now if I log the typeof my start game function, so I'm not executing it because that would call the function and I would get the typeof whatever this function returns, which is nothing which therefore would be undefined, as you see if you reload, you see undefined here, so that's not what I'm interested in.

If I log it like this, I am basically doing the same as with the event listener, I'm just passing the name here and therefore the typeof operator will have a look at the thing behind the name, so it will have a look at that thing which is stored in start game, which is our function and if we do that if I log the typeof my function here, then if I reload you see function here. Okay, that's not an object right, that's a function. Well actually, function is a separate type which is being logged here but it's based on object. It becomes a bit easier to see if I don't log the type but the function like this, so I'm not calling the function, I'm just passing the name here, so therefore I log the thing behind the function.

Now let's also switch console log to console dir which gives us a different insight into objects and if we then go back and reload here, you see here we get this strange thing here, looks like a function but I can expand it and what you see here is actually, there's a bunch of strange stuff in it, we got a name for example, we got an arguments thing and these are all key-value pairs in there, so these are all properties of this function in the end.

Now it also has a scopes thing and that's interesting, this basically tells Javascript where to manage the variables of these functions, so what the scope and on is and we don't need to worry too much about the stuff that's in there, some of the things like prototype will become clearer later in the course once we dive way deeper into objects and how they work internally, not something we have to worry about right now. The only key takeaway right now is that a function in the end whilst having its own type is an object.

It's basically also an object, a special type of object if you will with special pre-configured properties but still an object and the implication of that is for example that it's typically stored in the heap as you learned and basically anything that applies to objects, for example that they are reference types also applies to functions. Often that might not really matter to you, it's still important to be aware of that, so functions are objects.

----------------------------------------

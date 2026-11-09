# 9.15 — Understanding Object.assign()

> Section 9: More on Objects

Now if we talk about copying, we also have to talk about another way of copying values and for that, I reloaded the page and I'll again start with my name, Max object here and now if I want to create person2, of course we can use that spread operator which actually would be my recommendation because it's a really short syntax but there also is another approach which simply has been around for longer and has a bit of better browser support, though as you will learn in the browser support module, that might not matter for you and that other approach is to use object.assign. Now object is a globally available object actually in Javascript and it has an assign method where you pass in a target which is for example a new object you create and then the object where you want to copy over your values, like person.

Now you can add multiple sources where you want to copy over key-value pairs and in the end, object.assign will spit out a new object here then and merge all the key-value pairs of the other arguments into that new object and you by the way don't have to use it to create a new object, you could have an existing other object which has its own properties already and merge in properties of other objects into that, that would work as well but a common use case which you'll see is also exactly this use case where you assign properties of an existing object to a new object with object.assign. By the way when I say properties, the same for the spread operator, I also always mean methods as well, so both is copied over.

So here if I hit enter, you will see person2 now also is a copy of person and it's actually a copy where we have a real new object as I can prove by changing the name to Maximilian for example, person2 still has Max here because here, we created a real new object and just merge the two key-value pairs into it just as we did with the spread operator. Now again, the spread operator would be my recommendation simply because it's a bit shorter.

----------------------------------------

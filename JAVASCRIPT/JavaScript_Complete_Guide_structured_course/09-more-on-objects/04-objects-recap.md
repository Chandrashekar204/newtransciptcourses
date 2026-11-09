# 9.4 — Objects - Recap

> Section 9: More on Objects

So before we work on the actual application here with all the logic we need, let's quickly make sure we all understand what an object is. Well I guess we already did that but let's create one. So we can create an object and store it in a constant or in a variable, both works, it's a normal value in the end, now for example create that good old person object with which we worked multiple times already. Now we create it here with the curly braces and that's the object literal notation as it's called and in there, you can have these key-value pairs.

Now as I said, properties are key-value pairs which store some static values or some values and not functions basically and if you store a function as a value on a certain key, then this is called a method. Now both properties and methods are created here by entering some name of your choice, for example name and then a colon and then the value. Important, in here you don't have any const or let or anything like that, you just have name or whatever name you want to use for your key, colon and then the value, for example Max.

Now we can also add an age here for example and store 30, we could add hobbies and have an array in there, an array is an object and therefore this of course proves that we can have an object inside of an object, that is absolutely okay. There there we could have sports and cooking as hobbies and we could also add a method, for example greet which simply is a function assigned to a property here where we can then for example use the console here for the moment or also alert of course to show an alert box where we say hi there, something like that.

Now with that we created a person, an object and we can interact with that with that dot notation, we did this multiple times and this is probably not new. You can enter a dot and now you have access to all the properties and methods that are stored on this object, for example .age, .greet which is a function in which we therefore can call as such and so on and hence if I for example save that code and we go to our site, this is by the way what's getting rendered with that HTML and CSS which is part of the project and we reload this, we see hi there before this renders.

So this is what happens here with this basic object and thus far that's nothing too new. Now let me dive into some new things regarding the properties, how you can add them dynamically after an object was created, how you can delete them and which restrictions but also flexibility you have when it comes to picking a name and to accessing a property.

----------------------------------------

# 11.10 — Built-in Prototypes in JavaScript

> Section 11: Deep Dive: Constructor Functions & Prototypes

Now one important additional word about prototypes in Javascript. They're essentially everywhere and we have also taken advantage of them in the course already without knowing that we did so, for example with all the array methods I explained to you. If you dive into the MDN docs, you see that the array methods - concat or filter are actually part of array.prototype, so they're defined on the fallback object, on the prototype every array is connected to.

So when you create an array with the square brackets for example, you automatically get an array object which itself does not know these methods but it knows its prototype which in turn is an object that holds these methods and here of course you also find all available methods on that prototype including some methods which I didn't have a closer look at in this arrays module. And it's not just arrays, it's also the case for strings for example.

Now strings are kind of a special type because they're primitive values but as I explained, they still kind of behave like objects when you do call a method on them, some Javascript internal and therefore here, we also got a string prototype which is then utilized in the end which holds methods that help us with strings, something like slice for example which we also know from arrays but also string exclusive methods like replace or split which we saw in the array course section and that's in general a pattern you'll see throughout Javascript.

There are a bunch of built-in objects which are used as prototypes, so as fallback objects for other built-in objects. I'll sporadically come back to that and dive into this when we need to know it, for now just be aware of that and be aware that this is a core part of Javascript and that it's important for how fallback methods and dependencies and shared code is managed in Javascript.

----------------------------------------

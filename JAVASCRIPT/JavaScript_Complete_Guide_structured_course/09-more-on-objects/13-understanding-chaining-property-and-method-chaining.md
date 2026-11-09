# 9.13 — Understanding "Chaining" (Property & Method Chaining)

> Section 9: More on Objects

With this example finished, there are more exciting things we can dive into when it comes to Javascript and object syntax or Javascript features that help us work with objects. One important thing which I again want to emphasize is the concept of chaining, here we're doing something which is called chaining. We're having multiple dots in one and the same line or to be precise, in one and the same expression because we just prefer multiple operations on objects or on values returned by prior operations, for example movie.info returns an object and therefore we can access .title on that object.

We don't have to split this across multiple lines and store the result of movie.info in a variable and then use .title on that variable, we can all do it in one line. This concept of chaining is not only available on properties but also on methods, for example here with the ID. Math.random uses this built-in math object to generate a random number. Now it turns out that numbers in Javascript also have a method you can use which is called toString, actually everything in Javascript has this toString method.

Now what I'm doing here is I'm chaining the toString method on the result of math.random, so random is called on math and gives me a random number and toString is then called on that number. So this concept of chaining and this term, this special word, chaining, that is something you should memorize because you'll see it a lot in most programming languages and especially in Javascript, it is a common thing to do, it simply saves you the hassle of splitting code unnecessarily across multiple lines with helper variables in between.

----------------------------------------

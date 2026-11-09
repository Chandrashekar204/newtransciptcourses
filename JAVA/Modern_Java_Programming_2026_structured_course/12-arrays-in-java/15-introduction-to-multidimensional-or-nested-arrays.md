# 12.15 — Introduction to multidimensional or nested arrays

> Section 12: Arrays in Java

[00:00] As of now, we discussed about simple arrays.
[00:03] Using these simple arrays, we can store a group of elements which belongs to a same data type.
[00:10] For example, by using a simple array, I can store a group of into values or a group of String object
[00:17] or a Person object.
[00:19] Apart from these simple arrays, Java also supports multi-dimensional or nested arrays.
[00:25] So what is this multi-dimensional or nested array?
[00:28] In simple words, we can call them as array of arrays, which means each element of an array can be
[00:36] also be an array.
[00:38] So that's why anytime if someone asks you what is a multi-dimensional or a nested array, you can simply
[00:44] answer them
[00:45] it is an array of arrays.
[00:47] The most common multi-dimensional array that we are going to use in real projects is two dimensional
[00:54] array.
[00:54] If needed, we can build a three dimensional array, four dimensional array, five dimensional.
[00:59] We can build any multi-dimensional arrays or nested arrays based upon our business requirements and
[01:06] complexity of the data that we are trying to store inside arrays.
[01:11] So these are simple definition about the nested arrays and multi-dimensional arrays.
[01:15] Let's try to understand what is the syntax that we need to follow whenever we want to simply declare
[01:22] an nested array or multi-dimensional array. Like you can see here
[01:26] first, as usual, we need to mention what is the data type which is going to be supported by your array,
[01:33] followed by
[01:34] you can mention the square brackets, usually as part of simple arrays
[01:39] we will only mention a single square bracket, but here we can mention any number of square brackets.
[01:46] For example, if I want to create a simple array, then we are going to mention a single square bracket.
[01:52] Whereas if you have a requirement to store the data using the two dimensional array, then I need to
[01:59] mention two square brackets.
[02:01] Like the same way we can mention any number of square brackets based upon how many number of dimensions
[02:07] that we want to consider while building the nested array.
[02:11] And at last you can mention, as usual, what is your array variable name followed by semicolon.
[02:17] So here we are just declaring the nested array.
[02:21] We are not initializing it, or we are not assigning any size or length to my multi-dimensional array.
[02:28] As an excerpt, let's try to understand how to initialize and multi-dimensional or nested array.
[02:35] In the very first syntax
[02:36] you can see
[02:37] first, I am trying to use the same variable name that we have created in the above step.
[02:41] After the variable name
[02:42] as usual, we need to mention is equal to followed by new operator, followed by data type, and after
[02:48] the data type, you need to mention the same number of square brackets that you have defined during
[02:54] the declaration.
[02:55] Inside these square brackets, you can define the length values like length one, length two.
[03:01] If you want to combine both these declaration and initialization into a single statement, then you
[03:07] can look at these last syntax that I have mentioned.
[03:10] Like I said before, using these multi-dimensional array we can build a 2D array 3D array 4d array.
[03:17] So based upon our business requirements we can go to any nesting level.
[03:21] But most of the times in real projects people will end up using only 2D or at a max
[03:28] they will use 3D arrays.
[03:30] The higher number of dimensions you are trying to consider for your nested array, the more difficult
[03:36] you are going to face.
[03:37] To access and store elements inside a multi-dimensional array, you're going to understand the same
[03:43] when we are going to discuss few examples around the two dimensional array and the three dimensional
[03:48] array.
[03:48] Whenever we are using simple arrays to store the data, it is going to be super simple to access an
[03:54] element or to store an element at a particular index, because we just have to provide what is the position
[04:00] number or the index number.
[04:02] And providing such information with simple arrays is going to be super easy.
[04:07] But like I said, if you try to create two dimensional or three dimensional arrays, then you need to
[04:12] mention multiple index values along with their correct combinations.
[04:18] Otherwise you will end up accessing an invalid element.
[04:22] When we see examples around multi dimensional array, it is going to make more sense to you.
[04:26] The last point that I want to highlight here is, whenever we want to convert a nested array into a String
[04:33] representation, so that we can print the nested array onto our console.
[04:37] In this kind of scenarios, we need to use the deep toString() method available inside arrays.
[04:43] Whereas for simple arrays we used toString() method which is available inside arrays.
[04:49] The same toString() method is not going to work for multi-dimensional or nested arrays.
[04:54] That's why whenever you want to convert your multi-dimensional or nested array into a
[04:59] String object, please use the deepToString() static method available inside the Arrays class.
[05:06] I'm also going to show you a demo around this method in the coming lectures.
[05:10] I hope you are clear about what are multidimensional and nested arrays in Java.
[05:15] If something is not clear, don't worry, I'm there for you.
[05:18] From the next lecture, we are going to start discussion around the 2D arrays and the 3D arrays.
[05:23] And in the same process I'm going to show you many examples.
[05:27] And with that you're going to have a clear understanding around the nested arrays inside Java.
[05:33] Thank you
[05:33] and I'll catch you in the next lecture bye.

----------------------------------------

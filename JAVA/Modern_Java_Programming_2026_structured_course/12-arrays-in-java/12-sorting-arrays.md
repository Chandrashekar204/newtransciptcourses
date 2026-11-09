# 12.12 — Sorting Arrays

> Section 12: Arrays in Java

[00:00] The next common operation that you may want to perform on your arrays is sorting.
[00:06] So how to perform this sorting?
[00:08] To help you on the sorting operation, we have two different types of methods inside arrays class.
[00:14] The very first static method is sort to the sort method.
[00:18] You can simply pass what is your array and the output from this method is going to be.
[00:24] Your array is going to be sorted in an ascending format.
[00:29] Very similarly we also have parallel sort method.
[00:33] This method you can use if your array holds a large number of elements, like if your array size is
[00:41] more than 1000.
[00:42] In such scenarios, you can use the parallel sort method.
[00:46] Behind the scenes, this parallel sort method will apply some parallel logic, and it will try to leverage
[00:53] all the core processors available inside your laptop and try to perform the sorting operation parallelly
[01:00] in a more efficient manner.
[01:02] So let's try to see that demo of these methods as well.
[01:06] By building a Java program here I'm going to create a new class.
[01:10] The class name is going to be Short Demo inside this class.
[01:15] First, as usual we need to create the main method, followed by I'm going to create an array.
[01:21] The array name is going to be small array.
[01:25] And inside this I'm going to randomly store some into values like let me mention 5 to 8, one and six.
[01:36] So you can see as of now my numbers are arranged in a random order.
[01:41] If I want to sort the elements of my array, I can simply invoke arrays dot sort.
[01:48] And when we try to invoke the sort method, you can see we have many overloaded methods.
[01:53] Since we are trying to pass the integer type array, I'm going to invoke the very first method, and
[02:00] to this sort method I'm going to pass small array as an input.
[02:04] Now I'm going to print out these small array content with the help of arrays dot to string and to this
[02:13] two string method.
[02:14] I'm going to pass small array as an input.
[02:18] So this statement, it is going to print all the content of my small array onto my console.
[02:24] And you can see all my elements inside my array.
[02:27] They are sorted in an ascending order.
[02:31] Now let me show you that demo of parallel sort method to show you the demo of parallel sort method.
[02:37] First I want to create an array of type int with a variable name larger array to this array.
[02:45] I want to assign the size 10,000.
[02:49] That means I want to store 10,000 different int values inside this array, but populating 10,000 into
[02:58] values inside this array is going to be super heavy task for me.
[03:02] If I start doing this manually by using the syntax like larger array and with the index.
[03:10] If I start typing like this, it is going to take few years.
[03:14] That's why I'm going to show you a better way.
[03:17] The logic that I'm going to write is I'm going to iterate my entire array.
[03:21] During each iteration, I'm going to generate a random number and the same random number I'm going to
[03:29] store inside the current index value.
[03:32] So to generate the random number inside Java we have a random class.
[03:37] So this is available inside the Java dot util package.
[03:41] So let me try to create the object of this random class or start using the same object.
[03:46] I'm going to create the random values.
[03:49] So here I'm going to write the traditional for loop.
[03:53] That's why I'm going to first mention int I is equal to zero followed by I less than larger array dot
[04:01] length followed by I plus plus.
[04:04] So during the each iteration, I want to update the content of the larger array at a given current index
[04:12] value with a some random number.
[04:15] So how to generate a random int number using the random object, we can try to invoke the next int method.
[04:23] So there are three overloaded methods of next int method.
[04:27] I want to invoke the second method to this next int method.
[04:31] I'm going to pass an a maximum our upper bound value.
[04:35] So let me mention a upper bound number.
[04:39] So here I'm trying to mention 1 million or 10 lakhs as the upper bound number.
[04:45] So whenever a random int number value is trying to be generated using this random class, I'm trying
[04:51] to mention a maximum cap value.
[04:54] So this number is exclusive.
[04:56] So if I try to see the documentation of this method you'll be able to see the purpose of this param
[05:03] bound.
[05:04] So bound is used to mention the upper bound must be positive and it is exclusive.
[05:10] I hope you are clear.
[05:12] After this for loop is completed, our larger array will have 10,000 int values.
[05:18] I can also confirm you by using the System.out.println and with the help of arrays dot to string and
[05:26] to this two string method, I'm going to pass larger array as an input.
[05:31] So let's see first how the input is going to look like.
[05:34] You can see I have a larger array with 10,000 different values with some random numbers that are generated.
[05:42] If you can scroll right, you'll be able to see a bigger array with some random numbers generated.
[05:49] So now I want to do the sorting of these array.
[05:53] So let's try to understand how to do the same.
[05:55] It is going to be super quick.
[05:57] We just have to invoke the arrays dot parallel sort method to this parallel sort method.
[06:05] We need to pass the same larger array.
[06:08] This time I'm going to move the System.out.println just after these parallel sort operation.
[06:14] When we run this program we'll be able to see the content of the larger array in an ascending order.
[06:21] Let me confirm the same by executing this program.
[06:23] You can see the content of my larger array.
[06:26] Right now they are following the ascending order because all the content is sorted by my parallel sort
[06:33] method.
[06:34] So this is the maximum number that we have inside our array.
[06:37] I hope you are clear on how to do the sorting.
[06:40] As of now I'm only showing the demo with the help of primitive data types, but in real projects we
[06:47] may have requirements to sort the objects as well.
[06:50] Maybe if I have 100 different person object, I want to sort them based upon a name or based upon the
[06:56] age.
[06:57] So for these kind of complex requirements, first we need to complete advanced concepts like collections
[07:03] and lambda expressions and do functional programming.
[07:06] Once we complete all those advanced discussions, I'm going to show you some examples on how to sort
[07:12] objects inside an array as well.
[07:15] For now, please hold your thought around this.
[07:17] Thank you and I'll catch you in the next lecture.
[07:19] Bye.

----------------------------------------

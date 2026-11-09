# 12.4 — Declaring & initializing Arrays - Part 2

> Section 12: Arrays in Java

[00:00] There is one more approach as well, to create an variable and initialize at the same time with the
[00:07] given elements.
[00:08] So let's try to understand the same.
[00:10] For the same, I'm trying to create an int[] int and to this array I'm going to give the name
[00:16] as numm's.
[00:17] Inside this array I want to store five different int numbers.
[00:22] So how to do that?
[00:23] Once you declare the array variable on the left hand side, you can mention the curly braces and the
[00:30] right hand side.
[00:31] After the curly braces, please mention the semicolon.
[00:34] Now inside the curly braces I can mention all my int numbers.
[00:38] Like for example, I can try to store some numbers like one, two, three, four, five.
[00:46] So all the numbers has to be separated with a comma value.
[00:49] So with this I have created an array which is capable of storing five numbers of type int instead of
[00:58] int.
[00:58] If I try to assign a double or a float, I'm going to get a compilation error, because on the left
[01:05] hand side we said this array is only capable of storing the int primitive data types.
[01:11] But on the right hand side, if you try to violate that rule, you're going to get a compilation error.
[01:17] That's why always make sure you are storing the same data type elements inside your array.
[01:24] So with this syntax, we are trying to perform three different operations at the same time.
[01:29] The very first operation is I'm trying to declare a variable for my array.
[01:34] And the second operation is I'm trying to initialize my array with a predefined set of values.
[01:40] And the third operation is,
[01:42] since we have assigned five different numbers to this array, the length or
[01:46] the size of these num's array is going to be five.
[01:50] So this is another style of creating arrays in Java.
[01:54] Now with this you may have a question which is you have created an array of mobile numbers with a size
[02:01] of five, how you are going to store the mobile numbers of your friend inside this array.
[02:08] Because I have not followed this approach where we are trying to initialize the values during the declaration
[02:14] itself.
[02:15] So it is going to be very simple using the array variable name, which is mobile numbers, you can store
[02:21] the data.
[02:22] For example, if I want to store a mobile number inside this array, I need to mention at which position
[02:28] I want to store.
[02:29] So how to mention that just after the variable name, you need to mention square brackets, and inside
[02:34] this square brackets you need to mention the index number or the position where I want to store a given
[02:41] mobile number.
[02:41] For example, if I want to store at the very first position, then I need to mention zero, because
[02:48] inside arrays, the very first element position or index is always going to start from zero.
[02:55] After mentioning this on the right hand side, with the help of is equal to operator, you can try to
[03:01] assign a mobile number like ten digit mobile number I'm trying to assign.
[03:05] You can see I'm getting a compilation error saying that this number is too large for into primitive
[03:11] data type.
[03:11] So to resolve this I can either change this array variable named declaration to long primitive type
[03:18] or
[03:19] I can also try to make this number as a nine digit number.
[03:23] for now let me go with a nine digit mobile number.
[03:26] Very similarly, I can try to store different mobile numbers at a different positions.
[03:31] Like for example, at the very first position I will try to store some other number.
[03:36] Let me do the same for third position.
[03:39] For the third position I will type some random number followed by fourth position
[03:45] I'm going to again mention some random number.
[03:48] Now at last, at the fifth position, I'm going to store a number which is a random number again.
[03:57] So you can see I have five different mobile numbers stored inside this array.
[04:02] Now, if I try to execute my program in a debug mode and click on this step over, you will be able
[04:08] to see
[04:09] initially my mobile numbers is holding all zero values, but after executing this line, the value at
[04:16] the very first position is going to be changed.
[04:18] So let me click on this step over.
[04:21] You can see it is getting changed at each position.
[04:24] So this gives a confirmation to us that we are able to store the five different mobile numbers with
[04:31] the given array.
[04:32] Similarly, if I try to debug this line related to the num's array, you will be able to see a new
[04:37] num array.
[04:38] And inside this you can see I have 1, 2, 3, 4, 5 values stored.
[04:44] I hope this is clear.
[04:46] Let me release this breakpoint.
[04:47] As of now you can see we have declared the array size or array length as five.
[04:53] But if I try to be oversmart and try to store an element at the sixth position, then I'm going
[05:00] to get an exception which is ArrayIndexOutOfBoundException.
[05:04] Let me show you that as well.
[05:06] So I'm going to take the same line.
[05:08] And this time instead of four I'm going to mention five.
[05:12] So when I say five at what position we're going to store, we are going to store at the sixth position
[05:17] because we started the index from zero.
[05:20] Let me try to give a different mobile number here
[05:22] now, if I try to execute this program in a run mode, you'll be able to see I'm getting a RuntimeException
[05:29] which is ArrayIndexOutOfBoundsException.
[05:33] That means we're trying to access an index file which is out of bounds for the length of five.
[05:40] We have declared the length as five for the array, but we are trying to access the sixth element with
[05:45] the help of the index five.
[05:47] So that's why we are getting ArrayIndexOutOfBoundsException.
[05:51] Let me comment this line which is going to result into RuntimeException.
[05:55] I'm just commenting this and keeping it for your reference instead of hard coding this length value
[06:00] directly inside the array, you can also use an expression.
[06:04] For example, let me try to create an array of persons which is capable of storing 100 Person object.
[06:13] So let's try to achieve the same.
[06:15] First, let me try to create an length variable and inside this length variable I'm trying to store
[06:21] 100.
[06:22] So now using this length variable I can try to create an array of persons which is capable of storing
[06:29] 100 Person objects.
[06:31] So how to do that after persons?
[06:33] First let's remove the semicolon followed by
[06:36] you can mention is equal to followed by new operator, followed by persons with a square bracket.
[06:43] And inside the square bracket we can either hard code the value 100, or we can give an a variable or
[06:51] an expression.
[06:51] For example, if I give this length variable as an input to my array, then my array size is going to
[06:58] be 100.
[06:59] Otherwise, you can also use an expression as well.
[07:02] If I mention length asterisk two, that means my Person array object is going to have the length of
[07:10] 200.
[07:11] This way it is up to us whether we want to hard code the size or length value directly inside the array
[07:17] declaration, or we can also refer the length or size values from an expression or from a variable.
[07:24] I hope you are clear with all the basics on how to declare an array and how to initialize an array,
[07:29] and how to assign a size or length to an array, and how to store that data inside an array.
[07:36] Please make sure you are clear with all these basics. For your reference,
[07:40] I have mentioned all the points that we have discussed inside this slides, so please refer them if
[07:46] you have any questions.
[07:47] I have mentioned all the syntaxes that we need to follow.
[07:50] The only important point that I want to emphasize one more time is, inside array
[07:55] always the index at the position is going to start with zero.
[08:00] Here you can see we are trying to create an array of size five that is storing 1, 2, 3, 4, 5.
[08:07] So all these values they are going to be stored at the position 0, 1, 2, 3, 4.
[08:13] So whenever we want to access an element inside an array we need to use this syntax which is what is
[08:20] your array variable name followed by square brackets.
[08:23] And inside the square brackets we need to mention the index value.
[08:27] The same syntax we can also use to assign a value at a particular array index value.
[08:34] So I would request you to read all the slides one more time very quickly, so that you will be clear
[08:40] with all the points that we have discussed.
[08:42] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

# 7.41 — Details of Java operators Precedence & Associativity

> Section 7: Operators in Java

[00:00] I have total five slides where I have mentioned table with this format to explain you about the Java
[00:07] operators, precedence and associativity.
[00:10] First, let's try to understand the columns of this table.
[00:14] The very first column that we have here is what is the precedence of an operator, and what is the associativity
[00:21] of the operator and post that the second column indicates what is the operator itself, and the third
[00:27] column indicates what kind of operand types we can give as an input to a given operator.
[00:34] And at last I have operation type where I am going to provide a brief description about the type of
[00:40] operation that is going to be performed by a given operator.
[00:44] If you see here, and at the very first row, I have mentioned the precedence as 16.
[00:50] This is the highest priority that we have in Java.
[00:53] So all the operators like dot operator, array element , access operator [], method arguments(), list
[01:01] operator, post increment and post decrement operators.
[01:05] All these operators, they have the same precedence which is 16 anytime inside your Java expression
[01:11] if you have these kind of operators, they are going to be evaluated first until unless you override
[01:18] the precedence by using parentheses and the associativity for these operators are left to right.
[01:25] Most of the operators in Java they follow left to two right
[01:29] Associativity.
[01:30] Very few operators they follow right to left.
[01:33] So here you may see a new type of operators like dot operator.
[01:37] So we have been using these dot operator a lot to invoke the methods with the help of an object.
[01:43] So for all such scenarios we are using these dot operator.
[01:46] That's why I have not discussed about these separately and very similarly
[01:50] we also have an operator which we are going to use as part of arrays.
[01:55] We are ready to discuss about arrays.
[01:57] When we start discussing about the arrays, then it is going to make more sense to you.
[02:01] For now, please note that that these operator also has highest precedence And after that we have
[02:07] method of list operator.
[02:09] Whenever you want to invoke any method, you're going to send the arguments to the method by using these
[02:15] parentheses.
[02:16] So this operator we are going to use in the scenarios of method invocation.
[02:20] And we discussed about what is post increment and post decrement.
[02:24] So this operator has highest precedence as well.
[02:27] Moving on to the next row
[02:29] here you can see all these operators
[02:32] they have precedence which is 15.
[02:35] And they follow the associativity which is right to left.
[02:39] So this plus plus, minus minus you are able to see here as well.
[02:42] But this indicates pre-increment and pre decrement operators.
[02:47] And we also have unary place and unary minus operators,
[02:51] Bitwise complement operator, boolean not operator.
[02:55] So you don't have to remember all these precedence and associativity
[02:59] and you don't have to buy heart them.
[03:01] Just keep this information handy whenever you're going for an interview or whenever you are trying to
[03:07] address a scenario around operator precedence and associativity, you can quickly brush up all the information
[03:15] that I have provided in these slides.
[03:17] Now let me go to the next slide.
[03:19] Inside the next slide you can see we have the new operator, which we are going to use whenever we want
[03:25] to create an object of a class.
[03:27] And we also have casting operator.
[03:30] So these operators, they have the precedence 14 and they are going to follow the associativity right
[03:37] to left and post that we have arithmetic operators like multiplication, division, modulus, all of
[03:43] them.
[03:44] They have 13 precedence with the associativity as left to right.
[03:49] After that we have subtraction, addition and the string concatenation, so they have less precedence
[03:55] compared to the multiplication, division and modulus.
[03:59] So the precedence value for them is 12 with the left to right associativity.
[04:04] After these Arithmetic operators, we have left shift operator Signed right shift operator, Unsigned
[04:11] the right shift operator.
[04:13] So all these operators, they have precedence 11 with the left to right associativity.
[04:19] Moving on to the next slide
[04:21] less than, less than or equal to, greater than, greater than or equal to and the instance of.
[04:26] So all these relational operators, they have a precedence 10.
[04:30] We are ready to discuss about instance of operators in the coming sections
[04:35] we are going to talk in detail about them.
[04:37] So the associativity for these operators is left to right.
[04:40] After that we have operators with nine precedence and left to right associativity.
[04:46] So these equal and not equal, they repeated multiple times.
[04:50] The reason why I have mentioned these equal operator and not equal operator two times is, though their
[04:56] precedence and associativity is same, we can use
[05:00] these operators with various kinds of operands.
[05:03] For example, you can use these equality operator on top of primitive data types to compare if the content
[05:09] of the values is same or not.
[05:10] Whereas if you use on top of the object references, you're going to check if both the objects are referring
[05:16] to the same object or same memory location.
[05:19] So to differentiate that, I have repeated the same operators again.
[05:23] But please note that they all have same precedence and associativity.
[05:28] Moving on to the next slide,
[05:30] here, under the eight precedence, we have Bitwise AND operator and boolean AND operator.
[05:38] Coming to the Bitwise XOR operator and Boolean XOR operator, they have a precedence seven.
[05:45] Similarly, Bitwise OR and Boolean OR
[05:47] they have precedence which is six, followed by conditional AND operator
[05:53] it has a precedence as five, and at last we have conditional OR operator, which has an precedence
[05:59] four so all these operators you can see they have same associativity which is left to right.
[06:05] Now let's go to the last slide
[06:08] and here you can see the third precedence operator is ternary operator or Conditional operator.
[06:15] It is going to work with an associativity which is right to left.
[06:20] And after the ternary operator we have operators like Assignment operator and all Compound Assignment
[06:27] operators.
[06:28] So these operators they have precedence to with the associativity as right to left.
[06:34] And at last we have an lambda operator.
[06:37] We have not discussed about these
[06:38] operator we are going to discuss about these
[06:41] operator.
[06:41] When we start discussing about the lambda expressions inside Java, with the help of lambda expressions,
[06:47] we can follow functional style of programming in Java.
[06:51] So this is a very complex and advanced topic.
[06:53] We are going to discuss about that in the coming sections.
[06:56] So these lambda operator it has the very lowest priority inside Java.
[07:02] That means this lambda operator is always going to execute at the end.
[07:07] So always remember the operators with the highest precedence
[07:11] they are always going to be executed first, whereas the operators with the lowest precedence, they
[07:17] will be executed at a later point of time.
[07:20] With this, I'm assuming your million dollar question is answered.
[07:24] Like I said, you don't have to remember all those details, but have this information handy so that
[07:30] if someone tries to trick you, you can refer to these information and you can answer to them.
[07:34] At least you should have some basic knowledge about what is a precedence and what is an associativity
[07:40] around the Java operators.
[07:42] Hooray!
[07:43] With this we have completed all the discussion around the Java operators.
[07:49] I am super happy with the progress that we have made in this section, so please take a break and try
[07:55] to digest all the information that we have discussed around the Java operators.
[08:00] If needed
[08:01] please try to revise the slides that I have given multiple times so that all these information is going
[08:08] to enter into your subconscious memory.
[08:11] Take a break, come back and I'm going to catch you in the next section.
[08:15] Bye.


########################################

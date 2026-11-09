# 7.38 — Compound assignment bitwise operators in Java

> Section 7: Operators in Java

[00:00] Just like how we have Compound Assignment operators for Arithmetic operators and Logical operators.
[00:07] Very similarly we have Compound Assignment operators for Bitwise operators as well.
[00:13] The syntax of these Compound Assignment Bitwise operators is going to be very similar to the other type
[00:19] of Compound Assignment operators that we have discussed previously.
[00:22] So let's try to discuss very quickly about them.
[00:25] And we can also see a demo very quickly.
[00:27] So the syntax as usual first we need to mention what is your operand one followed by what is your Bitwise
[00:34] operator symbol.
[00:36] After the operator symbol you can mention is equal to symbol followed by what is your operand2
[00:41] When we use this short syntax behind the scenes, the JVM and the Java compiler, it is going to
[00:48] convert your expression into the format, which is operand1 is equal to type of your operand1,
[00:56] like the casting is going to happen, followed by an expression which is operand1, op operand2.
[01:02] So op means we can use various bit type operator symbols such as ampersand, pipe, carrot, two less
[01:09] than symbols, two greater than symbols, three greater than symbols.
[01:13] I also have an table explaining about how to use these Combined Assignment Bitwise operators, and what
[01:20] will be the equivalent expression that is going to be executed by your JVM or Java.
[01:26] For example, the very first operator that I'm trying to use is Bitwise AND operator.
[01:32] So the syntax that I need to follow is x, x is my operand1.
[01:36] ampersand is equal to y.
[01:39] So y is my operand2.
[01:41] So this expression is going to be evaluated behind the scenes as x is equal to type of x, which means
[01:48] the casting is going to happen once the x ampersand to y expression is calculated.
[01:54] The same applies for remaining operators as well.
[01:57] Can we see the demo of these very quickly?
[02:00] Inside my intelliJ, I'm going to create first an inter variable with the name x4, and inside this
[02:06] I'm going to store a value ten, followed by I'm going to create another inter variable which is y four
[02:13] and inside this I'm going to store a value six.
[02:16] Now I want to use Compound Assignment Bitwise operator by using Bitwise AND symbol.
[02:22] So how to do that we need to mention what is your left operand followed by,
[02:27] you need to mention what is your Bitwise operator symbol which is ampersand
[02:31] post that is equal to and followed by what is your second operand or right hand side operand.
[02:37] I can mention y4 as an right hand side upper end.
[02:41] After this, if I try to print out the value of x4, I'm going to get an output which is two.
[02:48] So let's try to validate the same by executing this program.
[02:51] And at the end you can see we have an output value which is two.
[02:55] Very similarly you can always use any Bitwise operator,
[02:58] for example if I want to use Bitwise OR operator I can simply replace ampersand with pipe symbol.
[03:05] I hope you are clear with this
[03:07] always use them wherever possible.
[03:09] With this we discuss all the bitwise operators.
[03:12] I'm assuming you're liking the progress that we are making throughout the course.
[03:16] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

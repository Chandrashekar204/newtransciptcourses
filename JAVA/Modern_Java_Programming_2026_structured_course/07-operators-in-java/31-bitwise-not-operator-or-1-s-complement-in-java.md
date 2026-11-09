# 7.31 — Bitwise NOT operator or 1’s complement in Java

> Section 7: Operators in Java

[00:00] We decided to learn about the Bitwise operators so they are complex to learn, but we are jumping into
[00:07] them without any fear.
[00:09] So brace yourself.
[00:10] First I'm going to start the discussion with Bitwise NOT operator.
[00:14] In other words, we can also call this operator as once complement operator.
[00:19] So what is the symbol
[00:20] to use this operator, we can use that tilde symbol just above the tab key.
[00:25] You'll be able to see a button which is going to hold that tilda and the backtick.
[00:30] So if you want to type this tilda you need to press shift and type backtick button.
[00:35] Then you're going to get this symbol.
[00:37] We know Bitwise NOT operator is an unary operator.
[00:41] It is always going to take one operand as an input.
[00:45] And for all Bitwise operators we need to provide upper end of type int only.
[00:50] If you try to provide other operand like String, boolean or any object, we are going to get a compilation
[00:56] error.
[00:57] So what is operation that these Bitwise Not operator is going to perform.
[01:01] So that's a question that we have right now when we use these operator each bit of your operand is going
[01:07] to be converted to its opposite value.
[01:10] That means first your normal
[01:12] decimal number will be converted into a binary number.
[01:16] And inside your binary number you will have bits like 1010.
[01:21] So each of your bit is going to be converted to its opposite value.
[01:26] That means if you have zero, then it is going to become one and vice versa.
[01:30] So here you can see I have given a table as well.
[01:33] If the input bit to the Bitwise NOT operator is one, then the output is going to be zero.
[01:39] Otherwise if the input is zero, the output is going to be one.
[01:42] I know you might be scratching your heads like why this fellow is continuously talking about bits.
[01:48] What are these bits,
[01:49] how can I convert my normal decimal number to bits?
[01:52] So you may have all such questions.
[01:54] No more
[01:54] wait.
[01:55] I'm going to give an example
[01:56] and with that you will be super clear.
[01:58] You can see here I'm trying to create an integer variable with the name x.
[02:04] And inside this variable I'm trying to store a int value which is nine for my Bitwise NOT operator.
[02:10] If I give this x operand as an input, I'm going to get the output as -10.
[02:16] That's what you can see.
[02:17] Whatever output that I am going to get from this Bitwise NOT operator the same I'm going to catch inside
[02:22] the int variable with the name y.
[02:25] And in this scenario the y is going to hold -10.
[02:29] So how we are going to get 10.
[02:31] Let's try to understand the same.
[02:32] In the very first step you need to convert your number nine to a binary number.
[02:38] So to convert that number to a binary number, first you need to write down the two to the power of
[02:43] zero two to the power of 1234567.
[02:48] Like this
[02:49] you need to write,
[02:50] if your number is larger, you can write two
[02:52] power of eight, two power of nine, two power of ten
[02:55] it's up to you.
[02:56] But with this number we should be good
[02:58] up to two to the power of seven.
[03:00] Once you have written these numbers, you need to mention either 1 or 0 against to each of these number.
[03:07] For example nine I can write as eight plus one.
[03:10] So where I'm going to get the eight two to the power of three, it is going to be eight.
[03:14] That's why at this position I need to put the value as one.
[03:18] And very similarly I need to look for a position where the value is one.
[03:22] So two to the power of zero is going to be one.
[03:25] That's why at this position I'm going to put the bit one remaining
[03:29] all places I need to put zero.
[03:31] How the calculation is going to happen is, when your computer look at this, it is going to perform two
[03:37] to the power of zero into one, which is one and two to the power of one into zero, which will be zero.
[03:43] Like this
[03:44] it will keep on multiplying at each position,
[03:47] after calculating all your positions, it is going to add the number like here we have eight and here
[03:53] we are going to have one.
[03:54] So eight plus one
[03:55] we are going to get the nine.
[03:56] So this is the way how we need to represent our decimal numbers in a binary format.
[04:01] Once you have represented your input in a binary format, we need to invert each bit value to its opposite
[04:08] value.
[04:09] So since I am trying to apply Bitwise NOT operator to the x at each position, I'm going to apply not
[04:16] operator, so zero will become one here also one here also one one, whereas here I have one.
[04:22] So the output is going to be zero
[04:24] and here 110.
[04:26] So whatever number you are going to get here this is the representation of -10.
[04:33] And here you may have a question like how I'm telling this is the representation of -10.
[04:39] On what basis I'm telling this is the representation of -10.
[04:42] So you may have some questions for the same
[04:45] I want you to show you the steps that we need to follow whenever we want to calculate the binary format
[04:51] for a given negative number.
[04:52] So let's try to understand the same before I move on to the next slide,
[04:56] like you can see here, I have mentioned all the steps that we have discussed
[05:00] here as well for your reference.
[05:01] Now let me go to the next slide.
[05:03] Think like I have a scenario where I want to represent a negative number -10 in an binary format.
[05:09] For the same we need to follow certain steps.
[05:11] The very first step is first you need to write down what is the binary representation of your positive
[05:18] number.
[05:19] If you have taken -10, then for plus ten
[05:21] first we need to write down what is the binary representation followed by.
[05:26] In the second step, you need to invert all the bits like 0 to 1, 1 to 0.
[05:32] Once you have inverted all the bits inside the third step, you need to add one to the inverted binary
[05:38] number that you received inside the step number two.
[05:41] So these are the three steps that we need to follow.
[05:43] So this process or this format we can also call it as two's complement format.
[05:49] Let me try to show you all these steps visually.
[05:51] Like you can see here,
[05:53] in the very first step I'm going to represent my positive number 10 in an binary format.
[05:58] So two to the power of three is going to be eight and two to the power of one is going to be two.
[06:04] That's why I have kept one only in these two positions.
[06:07] So eight plus two is going to be ten in all the remaining positions.
[06:11] I have mentioned the value as zero and inside the
[06:14] step two, we need to mention the inverted values like zero with one and one with zero.
[06:20] So once you have done all these inversion of the bits inside the
[06:24] step three, we need to add the bit one at the position of two to the power of zero.
[06:30] That's what I'm trying to do once we mention these one at the position of two to the power of zero,
[06:35] we need to add one plus one.
[06:37] So one plus one will give two.
[06:39] Where can we represent these two value.
[06:41] So to represent the two value we need to make first two to the power of zero as zero.
[06:46] Whereas at the position of two to the power of one, I need to mention the value as one, because two
[06:52] into one is going to be two.
[06:54] That's why I need to mention one here, and at the very first position I need to mention zero.
[06:59] Apart from these two bits, you can mention the same bits that you have received inside the step two.
[07:04] That's what I have done here.
[07:06] So these are the same number that we have received
[07:08] when we applied that tilda symbol to the positive number nine.
[07:12] I hope you are clear with this.
[07:14] Now let me go to the intelliJ and let me show you very quickly the demo about these Bitwise NOT operator.
[07:21] Inside my intelliJ
[07:22] first I need to create a new Java class.
[07:25] So let me create that.
[07:26] The class name is going to be BitwiseOperatorsDemo.
[07:31] Inside this class
[07:32] first I need to create main() method followed by
[07:35] I'm going to create an integer variable with the name x, and to this I'm going to assign the value
[07:41] nine.
[07:41] Later on I'm going to create one more variable y, and to this I'm going to assign an expression which
[07:47] is tilda of x.
[07:50] So with this I'm trying to apply Bitwise NOT operator on top of x operand.
[07:55] So what is the output that we can expect here.
[07:57] We can expect the output as -10.
[08:00] I can also try to print out the y variable onto the console.
[08:04] So let me try to execute this program
[08:07] and you can see we are getting the output as -10.
[08:10] So when we saw the demo inside IntelliJ Nowhere we are converting our decimal number into binary
[08:15] bits.
[08:16] And nowhere we are seeing the bits as well.
[08:18] Everything is going to be taken care by the Java behind the scenes.
[08:21] And here you may have a question which is what is a use case?
[08:25] Or what is a scenario where we need to use this bitwise operators in the real projects for the same
[08:31] the answer is most of the real projects where you are going to build a business logic related to your
[08:37] web applications, mobile applications, web services, or APIs.
[08:41] In all such scenarios, you're not going to use Bitwise NOT operators.
[08:46] 99% of the projects they don't need the Bitwise Not operators.
[08:51] You may need these Bitwise operators only if you are working on some networking programming related
[08:58] logic.
[08:58] Maybe you want to give some instructions to an hardware.
[09:02] In all such scenarios, you may end up writing the low level programming.
[09:07] So for the low level programming only, we need these bitwise operators behind the scenes
[09:12] when we use any of the bitwise operators, all these kind of conversion of your decimal number to the
[09:18] binary number and manipulating each bit by bit.
[09:21] So all these complex process is going to happen behind the scenes.
[09:25] So Java made our life very easy by abstracting all these complexity from us.
[09:30] We just have to simply learn how to use these bitwise operators.
[09:35] I hope you are clear.
[09:36] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

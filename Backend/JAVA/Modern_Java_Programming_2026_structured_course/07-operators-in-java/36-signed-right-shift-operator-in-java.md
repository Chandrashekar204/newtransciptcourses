# 7.36 — Signed Right Shift operator in Java

> Section 7: Operators in Java

[00:00] Inside this lecture
[00:01] let's talk about Signed right shift operator.
[00:04] The symbol to use this operator is we can mention greater than symbol two times continuously without
[00:11] any space.
[00:12] This operator also is going to shift to the bits just like Left shift operator.
[00:17] But this is going to work in an opposite direction.
[00:21] The name itself is conveying the same.
[00:23] The shifting operation is going to happen onto the right hand side.
[00:27] But what is this Signed word inside this operator name.
[00:30] So let's try to understand all these details.
[00:32] Signed
[00:33] right shift operator is a binary operator that performs a Bitwise right shift operation on the binary
[00:40] representation of the left hand operand by the number of bits specified by its right hand operand.
[00:47] Just like how we have Signed right shift operator, we also have Unsigned right shift operator, which
[00:53] we are going to discuss in the next lecture.
[00:55] The only difference between Signed right shift operator and the Unsigned right shift operator is this
[01:01] Signed the right shift operator
[01:03] it is going to preserve the sign of the left operand when shifting.
[01:08] When I say sign, what is that?
[01:09] It is the indication whether my number is a positive number or a negative number.
[01:14] So if you give the positive number as an input to this operator, it is going to retain that positive
[01:21] sign.
[01:21] And similarly if you give a negative number it is also going to retain the negative sign.
[01:26] So let's try to understand how it is going to retain.
[01:29] You can see we have an example here where first I have created an int variable with the value 50
[01:36] and using this int variable I'm trying to perform Signed right shift operator by using the greater than
[01:43] symbol two times.
[01:45] So whenever I want to use this operator as a first operand I should give the int variable
[01:50] and here I have provided the x.
[01:52] Whereas on the right hand side you need to give the number indicating the how many number of times you
[01:58] want to right
[01:59] shift your bits.
[02:00] So let's try to understand in detail about this by taking an example.
[02:04] So here you can see we are trying to apply the Signed right shift operator to a positive number.
[02:10] Because 50 is a positive number.
[02:12] I have not mentioned any hyphen or minus before this number.
[02:15] So the steps that we need to follow is first we need to build a binary representation of your positive
[02:21] number.
[02:21] So for the 50 the binary representation is going to be 32 plus 16 plus 2.
[02:28] That's why at the two to the power five and two to the power of four and two to the power of one
[02:33] I have mentioned the bit as one, whereas in all the remaining places I have mentioned the bit as zero.
[02:39] So once you have derived the binary representation of your input positive number, since you are going
[02:45] to right shift your bits by three positions, you need to simply ignore the last three bits.
[02:51] From the fourth bit onwards, you need to perform the right shift operation.
[02:56] Right now you can see this bit is present at the fourth position.
[02:59] That's why I'm trying to move it to the very first position.
[03:03] The same I have to do for all the remaining bits except for the last bit.
[03:08] So this last bit indicates me whether a given number is a positive number or a negative number.
[03:13] So always remember for positive numbers the last bit is going to hold the value as zero.
[03:19] Whereas for the negative numbers the last bit is going to have the value one.
[03:24] So this last bit you have to retain at the same position with the same value.
[03:29] So that's why first we need to mention this zero as it is at the position two to the power of seven.
[03:36] After that you will have some empty space between these three positions, like two to the power of six,
[03:42] two to the power of five, and two to the power of four into these three positions
[03:47] also, you need to mention the same bit that is available at the left most of your number, which is
[03:53] at the two to the power of seven.
[03:54] So the same zero
[03:55] you can see I'm trying to copy into this positions under two to the power of six, two to the power
[04:01] of five, and two to the power of four.
[04:02] So once this shifting operation is completed, you can calculate what is the decimal number of your
[04:09] binary representation.
[04:10] So here we have four plus two,
[04:13] so that's why we are getting the output as six.
[04:15] So there is also a shortcut that you can use whenever you are trying to apply these Signed right shift
[04:21] operator on a positive number.
[04:23] Please note I'm telling one more time that this shortcut is only applicable for the positive number,
[04:29] whereas for a negative number, there is a different process that we need to follow.
[04:33] And for the negative number there is no shortcut.
[04:36] So the shortcut for the positive number sign, the right shift operator is you can perform the integer
[04:42] division by two to the power of n.
[04:44] So what is the number that I have mentioned on the left side of my Signed
[04:48] right shift operator I have mentioned the value as 50, so the same 50
[04:53] I have to perform integer division by taking two to the power of three as an denominator.
[04:59] So with that the
[05:00] division is going to be 50 / 8.
[05:04] So what will be the output.
[05:05] We are going to get the output as six.
[05:07] So the same we are getting even if we follow the lengthy process that we have discussed.
[05:11] So this is the process that we need to follow for the positive number.
[05:15] Let's try to understand what is the process that we need to follow when we take an negative number as
[05:21] an left operand for the same, let me go to the next slide.
[05:25] Inside this slide you can see I'm trying to perform the same signed right shift operator by taking the
[05:31] negative number, which is -50.
[05:34] So since here we have a negative number, we need to follow the two's complement to calculate the binary
[05:40] representation of this negative number.
[05:42] In the very first step I'm trying to calculate the binary representation of the 50.
[05:46] So this is the binary representation post that I'm trying to apply the ones complement which is inverting
[05:52] each bit.
[05:53] So zero will be inverted to one and similarly one will be inverted to zero.
[05:58] After that I need to add one to the right most bit, since we already have one here with one plus one,
[06:05] we'll get zero here and in the left bit we need to mention one, and after performing this plus one,
[06:12] you can simply copy all the remaining bits that you have under the step two.
[06:16] So whatever you see at the step three, this indicates the binary representation of your negative number
[06:22] which is -50.
[06:24] So on top of this binary representation we need to apply the Signed right shift operator.
[06:29] So whenever we are performing the Signed right shift operator, we need to simply ignore all the last
[06:35] three bits, because on the right hand side, we have mentioned the operand value as three and post
[06:40] that we need to perform the right shifting of all the bits by three positions, and at last, once you
[06:47] reach to the last position, you need to retain the same value at the position two to the power of seven
[06:52] and you should also mention the same bit value in the blank positions, like at the two, to the power
[06:58] of six, two to the power of five, and two to the power of four.
[07:01] So this output indicates the binary representation of minus seven.
[07:06] I hope you are clear with this theory discussion.
[07:08] Let's try to quickly see the demo of this Signed right shift operator inside InteliJ.
[07:14] Here I'm going to create a variable which is x2
[07:17] and to this I'm going to assign a value 50.
[07:20] And very similarly I'm also going to create one more variable which is x3
[07:25] and to this I'm going to store a value -50.
[07:28] So using these two variables I'm going to perform the Signed right shift operator.
[07:33] So let me create a variable with the name z5.
[07:37] And to this z5 I'm going to assign an expression which I'm going to build with the help of Signed
[07:43] right shift operator.
[07:44] So first let me mention the positive number operand which is x2, and post that I'll mention greater
[07:51] than symbol two times followed by three.
[07:54] With this we are going to get the output as six.
[07:57] We can also confirm the same by trying to print out the variable z5.
[08:03] Very similarly, I can also try to perform the signed right shift operator on top of a negative number.
[08:09] So negative number means x3.
[08:11] We need to mention here and I'll rename this z5 to z6.
[08:15] And with that we are going to get the output as minus seven.
[08:18] So let me try to print this z6 variable.
[08:21] And if I try to execute this program you can see we are getting the output as six minus seven.
[08:28] So this is working like we expect.
[08:30] One important point that we need to identify here is you are Signed right
[08:34] shift operator
[08:35] always it is going to retain the sign of your number.
[08:39] That means if you give positive number as an input to your Signed the right shift operator, the output
[08:45] is always going to be the positive number.
[08:48] Whereas if you provide a negative number as an input, the output also is going to be always a negative
[08:54] number.
[08:54] I hope you are clear.
[08:56] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

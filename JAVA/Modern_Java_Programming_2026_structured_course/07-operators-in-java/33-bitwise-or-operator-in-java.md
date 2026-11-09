# 7.33 — Bitwise OR operator in Java

> Section 7: Operators in Java

[00:00] Bitwise operator is also a binary operator that performs a Bitwise OR operation on the binary representation
[00:09] of its operands.
[00:10] So what are the rules that we need to follow to perform the Bitwise OR operation?
[00:14] Here you can see I have given a table, and this table follows the same rules that we have discussed
[00:20] during the Logical OR operator or Logical Short-circuit OR operator.
[00:26] So think like one as and true and zero as false.
[00:29] With that assumption, if you see your Bitwise operator is always going to give you the output as one.
[00:36] If any of one of the operand bit is one if both operand bits are zero.
[00:41] In such scenario, only the output from the Bitwise OR operator is going to be zero.
[00:46] That's why we have the output as zero only for the fourth combination, where I have both operand1
[00:53] bit and operand2 bit as zeros.
[00:55] Now let's try to apply this Bitwise operator on top of an int operands.
[01:01] Here you can see I have created the same operands x and y and they are holding the same values ten and
[01:07] six.
[01:07] If I apply the Bitwise operator on top of these two int operands, I am going to get the output as 14
[01:14] the same.
[01:15] I am going to store inside the z variable.
[01:18] Since you are already familiar on how these Bitwise operators are going to work, I would request you
[01:23] to pause the video, take a pen and paper, and convert these decimal numbers to the binary numbers
[01:29] and post that perform the Bitwise OR operator on each of the bit based upon the table that you see,
[01:35] and at last you can convert the final binary number into its corresponding decimal number.
[01:41] So your output should match with the 14.
[01:44] So accept it as a challenge and try to do this.
[01:47] You can pause the video and you can take five minutes, 10 minutes, 15 minutes, whatever time.
[01:51] But I want you to be successful at this challenge.
[01:54] I hope you are successful at the challenge.
[01:56] If not, don't worry
[01:58] I'm going to explain you the steps one more time and at the very first step, we need to convert the
[02:03] given decimal numbers to the binary representation.
[02:06] So how I can write the ten I can write as eight plus two.
[02:10] That's why I have mentioned one and one at the positions, two to the power of three, and two to the
[02:15] power of one, and similarly six
[02:17] I can represent as four plus two.
[02:19] That's why I have mentioned the one bit at the positions two to the power of two, and two to the power
[02:24] of one in all the remaining positions.
[02:26] I have mentioned the bits as zero.
[02:28] Now for these two input operands, if you try to apply these Bitwise OR operator logic, we are going
[02:34] to get the binary number which is 00001110.
[02:40] In all the positions where we have at least one of the binary bit number as one for all such positions,
[02:46] you can see we have an output as 111.
[02:50] So if you try to convert this number into the decimal number, you're going to get the output as eight
[02:56] plus four plus two which is 14.
[03:00] Can we validate this very quickly using Java code?
[03:03] Inside my intelliJ I'm going to copy these two lines of code and paste it here.
[03:09] Post that I'm going to rename this variable to z2.
[03:13] And I can provide the same input x1 and y1.
[03:16] And the output like you know we are going to get 14.
[03:19] The same I can confirm by printing z2 onto the console.
[03:23] So here we're getting two
[03:25] the reason is I made a very silly mistake instead of ampersand.
[03:29] This time we should use the pipe symbol.
[03:31] So with that we should be getting the output as 14.
[03:35] Did you see?
[03:36] Even if you mess up with one single operator, the output is going to change drastically.
[03:42] That's why
[03:43] please be very careful.
[03:44] You need to perform enough testing before you try to push your code into the GitHub repository.
[03:49] I hope you are clear about the Logical OR operator.
[03:53] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

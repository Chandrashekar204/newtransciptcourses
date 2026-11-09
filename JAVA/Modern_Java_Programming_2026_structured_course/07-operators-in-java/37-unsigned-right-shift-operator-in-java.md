# 7.37 — Unsigned Right Shift operator in Java

> Section 7: Operators in Java

[00:00] Unsigned right shift operator is a sibling of Signed right shift operator.
[00:05] Whenever you want to use this Unsigned right shift operator, we need to mention greater than symbol
[00:11] three times continuously.
[00:13] This is going to work very similar to the Signed right shift operator, except with one difference.
[00:19] The difference is this operator always is going to fills the leftmost bits with zeros.
[00:26] Let's try to understand these by taking an example.
[00:29] You can see I have an x int variable with the value ten.
[00:32] If I try to perform Unsigned right shift operator on top of this x by mentioning the right hand operand
[00:39] as two, I'm going to get the output as two.
[00:42] Let's deep dive into the details and understand how we are going to get the output as two in this scenario.
[00:47] As usual, first we need to mention binary representation of your left operand.
[00:53] So the binary representation of the number ten is 00001010.
[00:59] So eight plus two will be ten.
[01:01] And when we want to perform the Unsigned right shift operator, we need to ignore the last two bits
[01:08] post that we can shift to all the remaining bits by two positions, because we have mentioned the right
[01:14] operand as two, and this shifting includes your left most bit, which is present at that two to the
[01:21] power of seven.
[01:22] You can see I'm trying to shift it as well to the position of two to the power of five, and with that
[01:27] you will left with blank values at the left most two positions.
[01:32] In these two positions you're always going to fill zeros.
[01:36] That's why this approach sometimes call it as zero extension.
[01:40] And this operator commonly used with the positive numbers.
[01:44] So once you have final binary representation as an output, you can try to convert that into a decimal
[01:50] number.
[01:50] Since we have only one bit at the position two to the power of one, the output we are going to get
[01:55] is two.
[01:56] Let's validate the same inside IntelliJ as well.
[01:59] Here we already have an integer variable with the value ten, which is x1.
[02:04] Using the same, I can try to perform the Unsigned right shift operation.
[02:09] So let me create an variable with the name z7.
[02:12] And to this I'm going to assign an expression which is x1 and Unsigned right shift operator by mentioning
[02:19] three greater than symbols continuously followed by two.
[02:23] So I want to shift to my bits to the right hand side by two positions.
[02:27] That's why I have mentioned the right operand as two.
[02:30] So to this the output we are going to get is two.
[02:33] I can also confirm that by printing these z7 variable.
[02:36] So let me try to execute this program
[02:38] and you can expect an output as two.
[02:41] With this I'm assuming you are super clear about the Unsigned right shift operator as well.
[02:46] So always please make a note
[02:48] that Signed right shift operator is going to retain the sign of the number in the output, whereas
[02:54] Unsigned right shift operator is always going to ignore your sign, which means you will always end
[03:00] up with positive number.
[03:01] That's why most commonly these unsigned right shift operator is going to be applied on top of the positive
[03:08] numbers only.
[03:09] Thank you
[03:09] and I'll catch you in the next lecture bye.

----------------------------------------

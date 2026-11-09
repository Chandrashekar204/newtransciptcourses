# 7.35 — Left Shift operator in Java

> Section 7: Operators in Java

[00:00] Inside this lecture, let's try to understand about the Left shift bitwise operator.
[00:05] So what is the symbol that we need to use to use this operator we need to mention less than symbol two
[00:11] times continuously.
[00:13] With that quick introduction, let's try to understand how this left shift operator is going to work.
[00:18] Whenever you are using these Bitwise operator you need to provide two operands because it is a binary
[00:24] operator.
[00:25] On the left hand side of this operator, you need to provide your into operand value whatever in number
[00:32] to which you want to apply this Left shift operation.
[00:35] You you need to mention that on the left hand side, whereas on the right hand side you need to mention
[00:41] a number based upon how many times you want to shift a bit onto the left hand side.
[00:47] Because whenever we use this Left shift operator, it is going to move all the binary bits off your
[00:52] left operand based upon the number that you have mentioned on the right hand side.
[00:57] I know it might be super confusing.
[00:59] Let's take an example and try to understand these left shift operator visually.
[01:04] Like you can see here I have an int variable which is x.
[01:08] And inside this int variable I stored an int number which is ten.
[01:12] Now I want to apply this left shift operator on this x variable.
[01:17] That's why I am going to mention x as an left operand and post that once I have mentioned the symbol
[01:23] of left shift operator, which is less than symbol continuously two times.
[01:28] After mentioning this symbol, I am going to give a number which is two.
[01:31] So when I give a number two on the right hand side, my left shift operator is going to shift to all
[01:37] the binary bits of my x variable by two positions, and with that, the output that we are going to
[01:44] get is 40.
[01:45] So let's try to understand how we are going to get the output as 40 as usual.
[01:49] First we need to write down binary representation of your int number which is x
[01:55] here, inside the x we stored a number called ten.
[01:58] That's why for these the binary representation is going to be 00001010.
[02:05] I have mentioned one bit at the position two to the power of three, and at the position two to the
[02:10] power of one as well.
[02:11] So eight plus two is going to be ten.
[02:13] Now how the result is going to be calculated is first on the right hand side
[02:18] the Left shift operator simply is going to mention zero values.
[02:22] Since I have mentioned the right hand side operand as two, it is going to mention zero at the last
[02:28] two two bits post that you can see each bit is shifted by two numbers, like it was there at the position
[02:34] two to the power of zero.
[02:35] Now it is going to move to the position which is two to the power of two.
[02:40] The same is going to happen for all the bits once it reaches to the end
[02:44] obviously, whatever bits that are left out, they will be simply ignored.
[02:49] So whenever we use this Left shift operator, the higher order bits, they always will be lost, whereas
[02:55] the lower order bits they are going to be replaced by zero like you can see here.
[03:00] So once this shifting operation is completed you can calculate that decimal number.
[03:06] So if you see here we have one at the position two to the power of five which is 32.
[03:10] So 32 + 8 is equal to 40.
[03:14] So this is how we need to apply Left shift operator.
[03:17] But I'm going to tell you a secret or a shortcut which you can use to quickly identify what is the output
[03:25] from a given Left shift operator.
[03:27] So the secret is simply multiply two to the power of n to your left operand.
[03:33] So n is the value that you have mentioned inside the right operand.
[03:36] So previously I have mentioned on the left hand side ten and on the right hand side I have mentioned
[03:41] the operand as two.
[03:42] So ten into two to the power of two, which is ten into four will become 40.
[03:47] So that's a shortcut or a secret.
[03:49] So keep this secret and you can use this secret to give the answer very quickly whenever the left shift
[03:56] operator is involved.
[03:57] I hope you like the secret.
[03:59] Let's validate the secret inside the intellige as well.
[04:02] Inside my IntelliJ, I'm going to copy these two lines of code, and I'm going to create a int variable
[04:08] z4 and post that after this x1 variable, I'm going to mention the Left shift operator which
[04:16] is less than symbol two times, and followed by I'm going to mention a number which is two.
[04:22] So with this what is output?
[04:24] We are going to get 40.
[04:25] So how 40, first take what is a value which is ten and post that
[04:30] you can multiply that ten with the two to the power of n and n is your right hand operand value.
[04:36] So two to the power of two is going to be four.
[04:39] And we are going to get the output as 40.
[04:41] So let's quickly validate the same inside the console as well.
[04:45] And this time you can see we are going to get the output as 40.
[04:48] Can we also validate this by taking another number.
[04:52] Maybe instead of x1 I'll try to mention 11
[04:55] you can expect here the output as 44.
[04:58] So if I try to execute
[04:59] this
[05:00] you can see we are getting the output as 44.
[05:02] I hope this is clear.
[05:04] And you like the secret that I have told
[05:06] keep it with you so that it is going to be super handy in your interviews or inside your Java exams.
[05:12] But few people, they may not like you
[05:14] if you try to answer very quickly, they'll ask you tell me how you got this answer.
[05:18] In such scenarios, you can mention all the steps that we have discussed visually, and with that,
[05:24] you're going to get full marks for your question.
[05:26] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

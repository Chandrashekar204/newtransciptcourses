# 2.26 — Demo of implicit and explicit casting - Part 2

> Section 2: Primitive data types in Java

[00:00] Now let me show you that demo of a few scenarios which are very tricky in nature, are twisted in nature,
[00:06] for the same
[00:07] first, I'm going to create an inter variable with the name num1, to this num1 variable, I'm going
[00:14] to assign a value which is 13, so there is no issue.
[00:17] I created an inter variable and I assigned an integer value.
[00:22] As a next step I'm going to create a long variable with the name num2.
[00:26] To this long variable, I'm going to assign a number which is just outside the range of integer.
[00:33] So until 647 my integer can save
[00:36] but here I'm trying to use 648 which is one number outside the range of into values.
[00:42] So let me mention the suffix here and post that I'm going to execute this command.
[00:47] So now I have num1 and num2.
[00:49] Now let's see what is going to happen if I try to assign num2 to the num1.
[00:54] So what I'm trying to do here, I'm trying to downgrade my long to int value.
[01:00] So this is what casting this is explicit casting or manual casting.
[01:04] If I try to press enter I'll get an error because this is not completely acceptable by the compiler.
[01:10] But here the developer can do the manual casting by just to mention int here.
[01:16] So do you think we are going to get an expected output?
[01:19] Off course we're not going to get an expected output.
[01:21] You can see the overflow scenario is coming into picture.
[01:25] Since this number is outside the range of integer, the overflow is happening.
[01:30] And that's why we are seeing this number as an output under num1.
[01:35] So please be very cautious.
[01:36] Whenever you are trying to do manual casting,
[01:39] you should also consider the range of values.
[01:42] Otherwise you will end up with overflow or underflow scenarios.
[01:46] For example, I can show you the same demo by taking a smaller number.
[01:50] In such scenarios, we're not going to lose any data.
[01:53] So let me create the first variable int num1, this time with the value six.
[01:58] And very similarly, I'm also going to create num2 with the value as 36L,
[02:04] you can see here both num1 and num2 are within the range of int data type.
[02:09] But still, if I try to do the casting of long to int, my compiler is not going to accept because I'm
[02:15] trying to downgrade.
[02:16] Let me show you that by running this command, which is num1 = num2, so 36 is within
[02:21] the range of int.
[02:23] But still my compiler is not accepting because num2 is an long value.
[02:28] So how to fix this by simply doing the manual casting.
[02:33] So now the casting is going to be allowed and my num1 is going to hold the value which is 36.
[02:40] Here there is no loss of data because my long value is within the range of integer values.
[02:46] As a next step, let me show you the conversion of char data type to the other primitive data types.
[02:52] For the same,
[02:52] let me clean my jshell console.
[02:55] Here first, I'm going to create a char variable for the same
[02:57] let me type char and the variable name is going to be myChar.
[03:02] And to this I'll try to assign some random character.
[03:06] Maybe I'll just assign M.
[03:08] So there is no issue here.
[03:09] Now, whenever you're trying to assign my char to other data types like int, float, double, byte, short,
[03:18] you need to be aware of few things.
[03:20] If you see this line where I have mentioned the primitive data type details based upon the order in
[03:26] an ascending manner, you can see the char comes only after byte and short.
[03:31] So if you try to assign this char variable to byte or short, we're going to call that as downgrade.
[03:38] So explicit casting or manual casting has to be done where if you try to upgrade from char to int, long,
[03:45] float, double, then in such scenarios the widening casting or automatic casting will happen.
[03:51] This is because char range is more than 65,000, whereas byte and short they cannot accommodate such
[03:58] a higher numbers only into long, float, double are capable of handling such higher numbers like 65,000.
[04:06] That's why anytime you try to cast a char to the int, long float and double, then that is an widening
[04:13] casting or implicit casting.
[04:15] And in the scenarios where you're trying to assign char to the short or byte, then we are going to call
[04:21] it as narrowing casting or manual casting.
[04:24] So let me show you this in the demo.
[04:26] So first I'll try to cast this my char byte.
[04:30] So for the same let me type byte myByteNum.
[04:34] And to this I'm going to assign the char variable which is myChar.
[04:38] So here, since I'm trying to downgrade character to a byte, I'm going to get an compilation error.
[04:44] The same you can observe for short as well.
[04:47] So let me mention data type as short and change this variable name to myShortNum.
[04:55] So here also we're getting an error.
[04:56] So how to fix this issue.
[04:58] We need to perform the manual
[05:00] casting.
[05:00] So let me try to perform the manual casting for short.
[05:04] So to do the manual casting, I need to mention short inside the brackets.
[05:09] After mentioning these, the casting will happen without any issues.
[05:14] So why we are getting 77 in the output
[05:17] because the character value M inside the Unicode has a decimal value, which is 77.
[05:23] That's why we are getting the output as 77.
[05:26] Now, if I try to cast my character to the int, float, double or long, then the compiler is not going
[05:33] to complain anything because I'm trying to upgrade my character to the higher data types.
[05:40] So let's see that in the demo. For the same, I'm going to create a variable int, and the variable name
[05:45] is going to be myIntNum.
[05:48] To this I'm going to assign myChar.
[05:51] So here without any error the casting is going to happen automatically.
[05:56] I assume you are clear about this concept.
[05:59] Please try all these examples with your own hands inside your jshell.
[06:02] So these are all easy examples where to discuss complex topics in Java.
[06:08] But before that, please, please make sure you are clear about all the basic concepts that we are discussing
[06:13] throughout this course.
[06:14] Now, as a last example, let me show you a very tricky scenario that you may face whenever you are
[06:20] trying to convert into to float or long to double for the same,
[06:24] let me clean my console.
[06:27] Here first I'm going to create an integer variable and the variable name I'll just mention as num1.
[06:32] To this, I'll simply assign a value 16.
[06:35] So there is no issue here.
[06:37] So now what I'm going to do is I'm going to assign this num1 to the float variable which is num2.
[06:44] Since this is an upgrade there is no issue,
[06:47] so my compiler is going to accept this casting.
[06:50] and I'm going to get an output which is 16.0.
[06:52] Now think like I want to cast this float number back to the int.
[06:56] So let me do the same for the same using int I'm going to create a variable num3.
[07:01] To this num3 I'm going to assign num2 which is of type float.
[07:05] So do you think this is going to work.
[07:07] This is not going to work because this is an downgrade.
[07:10] That's why I need to do the manual casting.
[07:12] So let me do the same.
[07:14] So if I try to execute this you can see
[07:16] so here I made a mistake I should mention into data type here.
[07:19] So now you can see under num3 we have a value as 16 which is exactly same as num1.
[07:26] So this will work perfectly up to certain range maybe for smaller numbers.
[07:32] But if you try to execute the same logic for larger numbers, then you are going to see a surprise.
[07:37] So let me show you that.
[07:39] So first I'll create a same num1.
[07:41] But this time I will try to consider a larger number.
[07:45] So the larger number is going to be this 1438764585.
[07:50] So there is no issue,
[07:51] my int variable can store this value.
[07:53] Now I'll try to assign these int value to the float by using float num2 is equal to num1.
[08:01] So here also there won't be any issues because this is an implicit casting.
[08:05] So this is my float representation value of these int value.
[08:10] As a next step I want to use this float value and assign this back to the int variable.
[08:16] So let's see by executing the command which is int num3 is equal to int of num2.
[08:22] So here I'm trying to do manual casting.
[08:25] And here you may expect this num1 and num3 is going to be same.
[08:29] But that is not going to be the scenario.
[08:31] So you can see there is some deviation,
[08:34] so here it is 585 whereas it is 544.
[08:38] Why
[08:38] this is because the way floats and doubles are stored is going to be different compared to the whole
[08:44] numbers like integer and long.
[08:47] That's why whenever you are dealing with the larger numbers, you will see this difference very clearly.
[08:52] Whereas for the smaller numbers, the num1 and num3 variables are going to hold the same value.
[08:58] So this is one of the tricky scenario that I want you to be aware.
[09:02] So when you're dealing with larger number of float values, please try to avoid the manual casting into
[09:09] int or long because you're going to lose some data
[09:12] and we saw that here very clearly. With this I have explained all the scenarios
[09:17] i will mentioned these scenarios inside the slide as well.
[09:20] So this is the slide where I have mentioned all the examples that we have discussed inside this lecture.
[09:25] I hope you are clear about typecasting in Java.
[09:28] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

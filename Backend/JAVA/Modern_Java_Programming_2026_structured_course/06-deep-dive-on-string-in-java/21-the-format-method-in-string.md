# 6.21 — The format() method in String

> Section 6: Deep dive on String in Java

[00:00] Inside this lecture, I'm going to explain about the format() method available inside the String class.
[00:07] So format is a static method.
[00:09] Let's try to understand what is the purpose of this format()
[00:12] method.
[00:12] Before that I want to show you a problem that I'm facing and how we can solve this problem with the
[00:18] help of format() method.
[00:19] Here you can see I have a class with the name StringFormatDemo, and inside the main() method I have
[00:24] a string variable with the name message.
[00:27] And inside this string I'm trying to store the data, which is,
[00:30] Hello Madan, you have three messages.
[00:33] If I want to show the same kind of message to different person with different number of messages, then
[00:40] the option that I have is I need to create one more string variable with the name message one and the
[00:47] post that I need to change the name, which is like Hello Saanvi, you have six messages.
[00:54] This way, if I want to send the same kind of message to many other people, I need to create lot many
[01:00] String objects and every time the sentence is going to be the same, the only changing data inside my
[01:07] string is the name and the number of messages.
[01:10] So to handle these kind of scenarios, we can build a String data that is going to hold the placeholder
[01:17] values here.
[01:19] Instead of hard coding the name, I can give a placeholder, and in the upcoming logic, I can replace
[01:25] the placeholder with the dynamic value that I want to provide.
[01:28] So to show you the demo of format() method, first I need to build a String data which has some placeholder
[01:35] inside it for the same
[01:37] first, let me delete this second line of code.
[01:39] And now instead of this Madan, I'm going to mention a placeholder by using
[01:46] %s indicates that in the upcoming logic, I want to replace this placeholder with a string
[01:53] value.
[01:54] Now as a next step, I want to replace this 3 with a placeholder value.
[01:58] So what should we type here?
[02:00] First we need to type percentage and post that
[02:03] since we want to replace a digit or a real number, we need to mention small d.
[02:09] Very similarly, if you want to replace a decimal number, then you should use f,
[02:14] indicates float and if you want to replace a char value inside a placeholder, then you should usef
[02:20] small c.
[02:21] If you want to replace a boolean value, then you should use the %b as a placeholder value.
[02:27] So now I have a string ready with the placeholders as a next step,
[02:32] with the help of format() method, we can replace this placeholders with the dynamic data that we are
[02:38] providing.
[02:39] Let me show you how to do that for the same
[02:41] first, I'm going to create a variable with the name messageForMadan.
[02:47] For message, I have used a shortcut which is msg and post that I have mentioned ForMadan.
[02:53] Now I want to invoke the format() method.
[02:55] Since format() method is a static method, we need to use the class name post that we need to invoke the
[03:01] format() method to this format() method
[03:04] first, I want to share the String object where I am mentioning the placeholder values.
[03:08] So what is a String object where we are maintaining the placeholder values?
[03:12] It is the message object, the same you can see here.
[03:15] After the message object, we can provide any number of input arguments based upon the placeholders
[03:22] that we have defined.
[03:23] So here inside this sentence I have defined two placeholders.
[03:27] If you define three or 4 or 5 placeholders accordingly, you can pass all of them as a input arguments
[03:35] to the format() method after the message object.
[03:38] In the very first placeholder, I want to replace with the value, which is Madan followed by
[03:44] in the second placeholder, I want to replace it with the value 3.
[03:48] Now, very similarly, I can build a message for Saanvi as well.
[03:52] This time the name I want to pass it here is Saanvi, and the number of messages I want to provide here
[03:58] is 6.
[03:59] So here you can see I'm trying to build our dynamic message data for various users data.
[04:06] So in future if I want to change something inside the message, I can simply change the message content
[04:11] in a single place.
[04:13] For example, here I have
[04:14] hello.
[04:15] If I want to change this hello to hi, I can simply change the same here and the same is going to reflect
[04:20] it back in all the objects like msgForMadan and
[04:24] msgForSaanvi.
[04:25] Let me show you the demo here so that it is going to clear for you.
[04:28] If I run this program you can see under the variable msgForMadan I am able to see the string
[04:35] which is Hi Madan you have three messages, whereas for the msgForDSaanvi I am able to see a message
[04:41] which is
[04:42] hi Saanvi, you have 6 messages.
[04:44] Suppose in future, like I said, if I want to change the content of the message, the change is going
[04:50] to be in the single place.
[04:52] So now I have changed this to hello.
[04:54] If I execute this program, the same is going to be reflected in all the String object.
[05:00] That we are trying to create with the help of format() method.
[05:03] So from this format() method, the return type is going to be the new String object.
[05:08] By replacingAll() the placeholders with the value that you have provided.
[05:12] Now, as a next step, let me show you one more example on how to replace a decimal value.
[05:18] For the same
[05:19] I'm going to create a new message.
[05:21] This time the message is going to be I want to display the price of a product.
[05:26] So for the same I'm going to type
[05:28] the price is $19.99.
[05:33] So here you can see I'm trying to hardcode the price.
[05:36] If I want to use the same message to display the price of various products, then I can't use this because
[05:43] the price value here is static.
[05:45] The other option that I have here is to create multiple String objects with a different, different
[05:50] price values.
[05:51] Instead of that, we can convert the content of this String object to have a placeholder value.
[05:56] I want to replace this 19.99 with a placeholder value.
[06:00] So to define a placeholder first we need to type percentage.
[06:04] And since here I want to replace a floating number or a decimal number, I should use f.
[06:10] So regardless you are trying to replace a double number or a floating number.
[06:14] Always
[06:15] you should use f.
[06:16] Now using this String object and format() method, I can try to build a multiple String objects by providing
[06:24] the price information at runtime.
[06:27] Let me show you a demo here.
[06:28] For the same,
[06:29] let me copy this line of code and mention here.
[06:32] Here I'm going to replace the variable name as price1 and post that
[06:37] I'm going to send this message1 as an input parameter to the format() method, this time inside the
[06:43] message1.
[06:44] Since we have a single placeholder, we don't have to pass these two arguments.
[06:48] Instead, we can pass a single argument that is going to send the price value using a decimal format.
[06:55] So here I'm going to mention 19.99.
[06:59] Very similarly, I can copy this line of code and change this variable to price2.
[07:04] And this time I'll change this to 9.99.
[07:07] If I try to run this program, you can see we are getting the output as the price is 19.99000.
[07:16] So here my format() method is trying to provide more precise value, but I want to restrict only for the
[07:24] two decimal numbers only.
[07:26] So how to achieve that?
[07:27] For that there is a technique.
[07:28] Let me show you that.
[07:29] Before that let me release this breakpoint.
[07:31] The technique is just between your % f,
[07:36] you need to type .2.
[07:39] With this dot two I'm telling to my String format() method.
[07:43] Whenever you are trying to display the decimal number, please have the precision value up to two decimal
[07:49] points.
[07:50] So if I try to execute this program this time, you can see the price is 19.99.
[07:55] And here the price is 9.99.
[07:59] I hope you are clear how to build a placeholders inside the String, and how to use the format() method
[08:05] to replace the placeholder with the dynamic values if needed.
[08:08] We can also introduce some padding space or alignment space with the help of the format() method.
[08:15] Let me show you how to do that.
[08:16] For the same, I'm going to create a new String object.
[08:20] The String object is going to be message2.
[08:24] Here the message that I want to mention is the number is and post that I want to mention %d.
[08:32] That means at runtime, I want to replace this placeholder with a real number value.
[08:38] In the next line, I can change the variable name to number1 and to this format method I can send
[08:45] this message to as an input, and the number I want to pass here is,
[08:49] maybe I can pass 5.
[08:51] And very similarly, I can pass one more number to the variable number2.
[08:56] And the number here I want to send is 15.
[08:59] So if I try to execute this obviously you know the output we are going to get the output as the number
[09:04] is five and the number is 15.
[09:06] But think like you want to give some more space between the is and the number.
[09:12] For such scenarios, there is a technique just before your d, you can mention some number like 5.
[09:18] With this the String format is going to apply five blank spaces between your is and the number that
[09:26] it is going to apply.
[09:27] So let me show you that demo this time
[09:30] you can see after the is there are some spaces the same you can see here as well.
[09:35] So how these spaces are coming because just before the d we have mentioned a number and with the help
[09:41] of this number, we are trying to apply some padding space.
[09:45] I hope you are clear with all these concepts.
[09:47] As of now you can see for our format() method we are passing the input parameters like Madan, 3.
[09:54] So the way it is going to work is whatever first parameter that you are trying to pass
[09:59] here, it is going to be replaced in the very first placeholder that you have defined.
[10:05] After the first argument is applied, then the format() method is going to take the second argument and
[10:11] apply the same inside the second placeholder.
[10:14] What if you don't want to give this control to the format, and you want to control it with your own
[10:19] hands?
[10:19] What I mean here is suppose think like the developer want to have a control.
[10:24] Which argument needs to be replaced at which placeholder for such scenarios
[10:30] also, we can use the format() method with a few tweaks.
[10:33] Let me show you that example very quickly.
[10:36] For the same, I'm going to create a String object, the String object variable name
[10:41] this time it is going to be message3.
[10:43] and inside this String object I want to type a String data, which is
[10:48] my name is post that
[10:50] I'll mention %s.
[10:52] That means I'm going to replace this placeholder with a dynamic value.
[10:56] Post that I'm going to mention comma followed by I am %d years old, followed by and I leave
[11:06] in %s at runtime I'm going to replace these three placeholders like %s, I'm going
[11:14] to replace with the name of the user, and %d I'm going to replace with the age of the user
[11:19] and the %s here, I'm going to replace with the name of the city where the user is staying.
[11:25] Now, as a next step, I want to replace all these placeholder values with the dynamic arguments with
[11:31] the help of format() method.
[11:33] For the same, I'm going to create a variable with the name String result, and after this I'm going
[11:39] to invoke the String format method.
[11:42] For this format() method I'm going to pass the input as message3, which is the object where my string
[11:49] data, along with the placeholders I'm maintaining. Here, I need to maintain the order
[11:54] first I need to pass the name, which is like
[11:57] I'll type Nithin and post that I need to mention the age like 25 and at last I'll mention the city as
[12:05] New York.
[12:06] So you can see here,
[12:08] if I want my format to work perfectly, I need to take care of the order of the placeholders by making
[12:13] sure that my method input arguments are matching with my placeholders.
[12:18] If I screw up these placeholders, like in the place of Nithin, if I mention New York, and here if
[12:24] I mention Nithin, let's see how the output is going to look like.
[12:28] If I execute this method, you can see the result is
[12:31] My name is New York and I am 25 years old and I live in Nithin.
[12:36] Here sometimes we want to avoid these kind of mistakes.
[12:39] Instead of giving the control to the format() method to apply all these dynamic values in the place of
[12:45] placeholders based upon the order of the method arguments, I can define my own order off method input
[12:53] arguments.
[12:53] For example, I want this nithin to be applied at the very first placeholder, and this New York should
[13:00] be applied at the last placeholder, and this 25 should be applied in the second placeholder.
[13:06] So how to achieve this for the same,
[13:08] the change
[13:09] it is going to be very easy just between your %s mention
[13:14] what is the number of the argument that you want to apply here if you ignore this message3 method
[13:19] argument.
[13:20] So this is going to be one.
[13:21] This is going to be second and this is going to be three.
[13:24] So if I want the third argument to be available here I need to mention 3$.
[13:32] And very similarly I want the %d to be replaced with the second argument.
[13:37] So that's why I need to mention 2$.
[13:41] And here I'm going to mention $1.
[13:45] So let's see how this is going to work I'm going to run this method
[13:49] you can see this time the output is
[13:51] My name is Nithin.
[13:53] I'm 25 years old and I live in New York.
[13:56] So the control right now is completely in our hands.
[14:00] How did we achieve that?
[14:01] Just by mentioning these number followed by dollar.
[14:05] So this is one flavor of placeholders that you can feed to your format() method.
[14:09] So I hope you are clear with all the concepts of format() why we should use the format() method.
[14:15] For your quick reference, I have mentioned all the details that we discussed about the format() method
[14:20] in these three slides.
[14:22] Like I mentioned here, %s mean String, %p means integer, f means floating point
[14:28] numbers, c means character and b means boolean.
[14:31] So whenever you want to replace a placeholder with a boolean value, then please mention
[14:37] %b.
[14:37] The other examples also I have provided for your reference, so please refer them for any questions
[14:42] and run the examples that I have provided inside your Java program as well.
[14:47] I hope you are clear with the format() method.
[14:49] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

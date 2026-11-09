# 15.9 — Deep dive on toString() in Object class

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Now let's try to discuss the next method available inside Object class, which is toString() method.
[00:07] Before I try to explain you about the purpose of toString() method and why we should override it, first,
[00:13] let me show you a small demo with the default behavior of the toString() method.
[00:18] For the same, I'm going to open the HashCodeEqualsDemo class.
[00:22] Here I'm going to write a System.out.println() and using the System.out.println(), I'm
[00:29] trying to print the p1, and similarly I also want to print out p2.
[00:34] This means I'm trying to print out my Person objects.
[00:38] If I try to execute this program, you can see the output
[00:41] it is not going to make any sense to me.
[00:44] So these are the two statements that is logged by my two System.out.println() that I have added
[00:50] just now.
[00:51] Let's try to see why we are getting this output by opening the toString() method available inside the
[00:58] Object class.
[00:59] So I'm trying to open toString() method.
[01:02] So the default implementation is,
[01:04] first it is going to print out the complete qualified name of your class.
[01:09] So the object belongs to the Person class.
[01:11] So that's why we are getting the complete qualified name of the class along with the package name.
[01:18] After that we have @ symbol.
[01:20] The same is being mentioned here.
[01:22] And after this at symbol, the hashCode() method is being invoked.
[01:27] The hash code value is converted into the hexadecimal representation with the help of this
[01:34] Integer.toHexString().
[01:35] So these toHexString() method, which is available inside the Integer wrapper class.
[01:40] It is going to convert an integer value into an hexadecimal representation number.
[01:46] That means whatever we are seeing here
[01:48] after this at symbol, it is the hexadecimal representation of your hash code value.
[01:54] So this is the default behavior.
[01:56] But is this useful to us
[01:57] off course not, because most of the times the reason why a developer want to print out his object is
[02:03] you want to see the content of the objects.
[02:06] Either it can be in the console or it can be in the logs.
[02:10] If the developer prints his object onto the console or onto the logs, it is going to help in some debugging
[02:16] scenarios or to fix some defect.
[02:18] So that's why we should always consider to override the toString() method.
[02:22] Whenever you want to print the content of your object onto the console or onto the logs in a String
[02:30] format.
[02:31] That's why inside the person class I will try to override that toString() method.
[02:35] Overriding the toString() method is very simple.
[02:38] You can right click and select the generate, and here you have an option to generate the toStrings().
[02:43] So let me select this and it is going to ask you which fields you want to consider to generate the
[02:49] toString() method logic and the template.
[02:51] You can select String concat.
[02:53] So this is the default one.
[02:54] You should be fine with this default option.
[02:57] Now let me click on this okay button.
[02:59] And you can see inside my toString() method.
[03:02] First I'm going to have the class name followed by curly braces followed by instance field names like
[03:07] name, age, gender and ssn and post that we are trying to append the content of the instance fields
[03:15] to the corresponding field names.
[03:17] After making this change, if I try to execute this program, you will be able to see my Person object
[03:24] details in an easily understandable format.
[03:28] So the p1 object has this data and the p2 object has this data.
[03:33] So this kind of information is going to be helpful to the developer during that debugging process.
[03:39] So always override and use the toString() method whenever you want to convert your object to data into
[03:46] an easily understandable String data.
[03:49] Now let me go to the program.
[03:50] Here
[03:51] you may have a question which is I'm not invoking the toString() method.
[03:54] Then how come the content of the p1 object and p2 object are being printed with the help of two
[04:01] string method?
[04:02] So that can be your question.
[04:03] It's a great question.
[04:05] Let me clarify you that whenever you are trying to print out a given object behind the scenes, your
[04:11] JVM is going to rely on your logic that you have written inside that toString() method.
[04:17] For example, here, if I try to invoke the toString() method, you can see I'm getting a warning saying
[04:22] that unnecessary toString() call.
[04:24] Why are you calling toString() unnecessarily?
[04:27] There is no need because behind the scenes, if you try to print out an object JVM anyway, it is going
[04:33] to invoke your toString() method.
[04:34] That's why IntelliJ also is trying to help us by giving a warning.
[04:38] As soon as I remove the invocation of toString(), the warning is resolved.
[04:41] Before I try to close this lecture, I want to share an important note about the toString() method.
[04:48] As of now, we relied on the shortcut approach to generate the toString() data implementation
[04:54] with the help of IntelliJ. You should be fine with the toString() logic generated by the
[05:00] IntellIJ if you have your own custom requirements that you want to print your own format, then you are free
[05:06] to override these methods based upon your requirements.
[05:09] For example, instead of curly braces, if you want square brackets, you can mention the same, and
[05:14] the same is going to be reflected whenever you try to print your object.
[05:19] Like you can see I'm trying to execute this program this time
[05:21] you can see I have the square bracket this way it's up to you.
[05:26] Whatever format you are comfortable you can follow
[05:29] the same.
[05:29] For now I'm going to that default generated curly braces.
[05:33] And whenever you're trying to generate these toString() implementation logic, please make a note of
[05:39] the sensitive information.
[05:41] For example, think like you're trying to print an User object.
[05:46] And this User object has user name and password.
[05:49] Password is a sensitive information.
[05:51] If you try to print that onto the console or onto the log, if someone sees those logs or console statements,
[05:57] they will be able to easily steal the password of an user.
[06:01] The same applies for the ssn
[06:03] also here SSN is a secret number are considered as a sensitive.
[06:07] So if you have these kind of sensitive information, please make sure you are not including those instance
[06:13] fields as part of the toString() logic.
[06:16] Otherwise, you will be in trouble on some day whenever some security screenings are happening inside
[06:22] your project.
[06:23] I hope you are clear with all the discussion that we have done around the toString() method.
[06:27] Whatever we have discussed around the toString() method, I have mentioned them in these two slides
[06:32] for your reference.
[06:33] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

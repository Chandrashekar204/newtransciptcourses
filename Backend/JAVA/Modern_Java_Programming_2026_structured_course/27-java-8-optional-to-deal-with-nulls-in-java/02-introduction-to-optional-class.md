# 27.2 — Introduction to Optional class

> Section 27: [JAVA 8] Optional to deal with nulls in Java

[00:00] While we are discussing about the streams API at many places we saw these optional class, so you can
[00:07] see the output from these reduce() method
[00:10] it is wrapped inside th Optional class.
[00:13] If you try to search for these kind of optional inside the same class, you will be able to see at many
[00:19] places like min() method, it is doing the same max() and findFirst().
[00:23] So these kind of code you will be able to see throughout the Java and even inside your real projects
[00:29] as well, where the return type from the method is going to be wrapped inside the Optional.
[00:34] So what is this Optional indicates here the developer who coded this method, he can simply return the
[00:40] T, but why
[00:41] he is trying to wrap that t inside the Optional.
[00:44] So what is the developer is trying to convey here?
[00:47] It's very easy to understand the purpose of Optional.
[00:50] Whenever a developer is building a business logic, which may return a object as an output, the developer
[00:57] is going to have two kinds of scenarios.
[00:59] The very first scenario is happy path scenario, where the developer is going to send a proper object
[01:05] as an output, and the second scenario is around the negative scenario.
[01:09] Whenever these negative scenario occurs inside the developer business logic, the developer may send
[01:15] a null value as an output from the method.
[01:18] So to represent to other developers saying that that my method may send a null object or a normal proper
[01:26] object, the developer is going to use these Optional.
[01:29] Whereas if the developer is very confident that his method always going to return a normal object,
[01:36] and there is no scenario where his or her method is going to return a null object, then he can happily
[01:42] return the T as an output instead of optional T, you'll be able to see at some places you will not
[01:48] have Optional T, so here you can see there is a of() method which is going to return the Stream of T.
[01:55] So here we are not using any Optional T.
[01:57] Similarly, if you can scroll down scroll down, maybe we can go to the filter() method.
[02:03] So here you can see the filter() method also is giving a Stream of T but not Optional of T.
[02:08] So optional concept is not only applicable to the stream API, the usage of optional.
[02:14] You will be able to see throughout the Java.
[02:16] So the feature of optional is introduced inside Java 8.
[02:19] So let's try to understand why this feature is introduced and how to use this optional, and how to
[02:25] operate the objects that are wrapped inside a Optional.
[02:29] The primary purpose of introducing optional inside Java is to deal with the null values.
[02:35] Why we have to deal with the null values?
[02:37] Because there is a reason.
[02:38] If I ask all the Java developers across the world to raise their hand if they have ever seen the
[02:45] NullPointerException inside their code, then there won't be no single developer who will not raise their
[02:51] hand.
[02:52] We will have all developers raising hands like this here.
[02:55] The baby is trying to raise his hands.
[02:57] So similarly some developers may raise their hand like this.
[03:01] The same question you can ask your Java developers.
[03:03] Majority of them, I would say 99% of them
[03:07] they will raise their hand saying that they encountered NullPointerException at least once inside
[03:13] their program.
[03:14] So that's how common it is to see that NullPointerExceptions inside Java code.
[03:19] That's why to deal with the NullPointerExceptions more efficiently, this optional has been introduced.
[03:26] Please note that the purpose of optional is not to eradicate all the NullPointerExceptions.
[03:31] Instead, it is going to give more proper approaches to handle the NullPointerException gracefully.
[03:38] First, let me show you the code which developer used to write before the introduction of Optional.
[03:43] So here you can see I have a method with the name get userOrderedDetails().
[03:49] To this method
[03:49] I'm passing an user object as an input.
[03:53] So inside user we have various embedded objects like inside user I have an order object.
[03:59] Inside this Order object we'll have item object, and inside the item object we'll have the name of
[04:04] the item.
[04:05] So if I try to execute this business logic to return the item name which the user has been ordered,
[04:11] there is a very good chance that a NullPointerException can happen at any point of time.
[04:16] For example, if the input to this method, which is user itself is null, then with the null object
[04:23] if I try to invoke getOrder() method, then obviously I'm going to get a NullPointerException.
[04:28] Maybe think like someone sent a proper User object and using the same proper User object, you are able
[04:34] to invoke that getOrder() method.
[04:35] So these getOrder() method.
[04:37] It is going to return the Order object, and the Order object can be a null or it can be a proper object.
[04:43] So if it is a null and using null, if you try to invoke the getItem(), you're going to get a NullPointerException
[04:48] NullPointerException again, in the similar lines, this getItem() method.
[04:51] Also, it is going to return you the Item object.
[04:55] If the received item object is a proper object, there is no problem you can
[04:59] safely invoke this getName() method.
[05:02] Otherwise, if the item object is null.
[05:04] If you try to invoke this getName() method by using the null object, you're going to get
[05:09] NullPointerException.
[05:10] In this single line of code, you can see there are multiple places where a NullPointerException may
[05:16] occur.
[05:16] That's why to avoid these kind of NullPointerExceptions before Java 8 developers they used to
[05:22] use lot of if conditions to validate if a given object is a null or not.
[05:27] So here just to make sure this method getUser() ordered details is not throwing any NullPointerException.
[05:34] Some experienced developer has written these code.
[05:37] You can see first, the developer is trying to check if the User object is not null.
[05:42] If it is null, the developer simply going to return a item name as not available, whereas if the User
[05:50] object is not null, then the developer is going to invoke the getOrder() method using the User object.
[05:56] Pose that the developer is going to get order as an output.
[05:59] Again, the developer is trying to check if the order is not null.
[06:03] If the order is not null, then only the developer is going to invoke the getItem() again
[06:08] for the Item object, the developer is trying to check if the Item object is not null.
[06:13] If it is not null
[06:14] at last, the developer is trying to invoke the getName() method, which is going to return as an output
[06:20] from this method.
[06:21] Do you see
[06:22] just to handle NullPointerException, the developer has to write such a lengthy code using if and
[06:28] sometimes else and else if blocks are also going to be used.
[06:32] So just to make developers life easy to handle, the NullPointerExceptions gracefully with very less
[06:38] amount of code.
[06:39] And just to inform other developers that a particular method may potentially give a .
[06:45] NullPointerExceptions.
[06:46] To handle all these kind of scenarios
[06:48] the optional isIntroduced() as part of Java 8.
[06:52] So let me search for Optional
[06:54] inside my interface.
[06:56] You can see it is present inside that java.util package.
[07:00] It is introduced as part of 1.8, which is the Java 8 version.
[07:04] If you see the documentation here, they clearly highlighted.
[07:08] Optional is primarily intended for use as a method return type, where there is a clear need to represent
[07:15] no result, and where using null is likely to cause errors.
[07:19] I hope you are clear with all these introduction around the Optional.
[07:23] Throughout this section, we are going to deep dive into the Optional and try to understand how to use
[07:28] this Optional to handle the NullPointerExceptions in a more graceful and efficient manner.
[07:34] I hope you are clear with the agenda of the course.
[07:36] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

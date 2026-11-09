# 27.4 — Demo of Optional - Part 2

> Section 27: [JAVA 8] Optional to deal with nulls in Java

[00:00] Inside this lecture, let's try to leverage Optional to overcome the challenges that we have with the
[00:06] code that we have written in the previous lecture.
[00:09] What I'm going to do is, I'm going to keep this ugly code for your reference.
[00:13] Instead of modifying these existing code, I'm going to create a similar kind of method with the name
[00:20] say hi.
[00:21] So this is also a static method.
[00:23] And inside this also I'm going to have this random logic to return a statement
[00:28] Hi World
[00:29] in the scenario of even number.
[00:31] Otherwise it is going to return the null as an output.
[00:34] So let's try to enhance this method further by leveraging the Optional.
[00:38] The very first enhancement that a developer has to do to the return type of a method is based upon the
[00:45] developer business domain knowledge.
[00:47] The developer knows whether the method is always going to give a proper output, or it may send null
[00:53] values in some negative scenarios.
[00:56] So based upon his or her knowledge on the business logic, the developer has to decide whether to keep
[01:02] only String, which conveys always his or her method is going to return a proper String object if the
[01:09] developer is not confident, and if there will be some scenarios where a null object can be returned,
[01:14] then the very first step that he need to do is he need to wrap the return type inside
[01:18] Optional.
[01:19] So after typing Optional inside angle brackets, we can mention String.
[01:24] So if you open these Optional you can see this is built with the help of generics.
[01:28] So the T indicates that it can hold or deal or wrap any kind of data type object.
[01:34] So here I'm just trying to mention String because we're trying to return a String object.
[01:39] After making this change, you can see we are getting a compilation error because we're trying to return
[01:44] a normal String object.
[01:46] But the return type of this method is Optional string.
[01:49] So to resolve this error, what you have to do is you need to use the Optional class.
[01:55] And inside this Optional class we have of() method.
[01:59] So to this of() method you can pass a String object which you want to wrap.
[02:04] So here I'll type
[02:05] Hi World.
[02:07] So this is the String object I want to wrap inside my Optional.
[02:11] And similarly in the case off negative scenario you should not pass the null object directly.
[02:17] Instead you need to pass Optional.empty().
[02:21] So whenever you are invoking the empty() method of optional, it is going to simply give an optional which
[02:27] is not going to hold anything.
[02:29] So here it is also highlighted.
[02:31] It is going to return an empty optional instance.
[02:34] No value is present for this
[02:36] Optional.
[02:37] So this is how you need to either send a empty optional instance or if you have a valid object, you
[02:44] can wrap it with the help of of()method.
[02:46] We also have other method which is ofNullable(), so there is a difference between of() and ofNullable().
[02:54] So let's try to read the documentation ofNullable().
[02:57] So when we use this ofNullable() what is going to happen is if you try to read this documentation,
[03:02] it clearly conveys if the given input object, which is t, is a non null object, it is going to wrap
[03:09] the same into the optional.
[03:11] Otherwise it is going to returns an empty optional.
[03:15] So this is cool, right?
[03:16] Instead of using of() and empty() separately, we can use a ofNullable().
[03:20] Maybe what I can do is, I can remove all this code, and I'll try to create a String variable with the
[03:26] name msg to the same msg variable, and going to assign a value inside my if condition.
[03:34] The value I'm trying to assign is
[03:36] Hi World.
[03:37] Now outside this Eve, I can simply have a single return statement which I can build with the help of
[03:44] optional ofNullable().
[03:45] To these ofNullable()
[03:47] I'm going to pass the msg as an input here.
[03:50] We're getting a compilation error saying that msg might have not initialized.
[03:54] Maybe what I can do is I'll try to initialize to a null value.
[03:58] With that we should be good.
[04:00] So the beauty of these ofNullable() here is if the msg is a null object, which is going to happen in
[04:07] the scenario of odd numbers, then the return type from this method is empty Optional.
[04:12] Otherwise a valid msg object it is going to be wrapped inside my Optional, and the same is going to
[04:18] be returned to the caller.
[04:19] Now let's see the story on the main() method.
[04:23] So here what I'm going to do is I'll try to repeat these three lines of code again.
[04:28] So first I'll try to invoke the sayHi() method.
[04:31] So when we invoke the sayHi() method, and if you try to catch the output with a variable as msg of type
[04:39] String, obviously you're going to get a compilation error because the return type from the method is
[04:44] optional off String, but you're trying to accept the output using the String object.
[04:49] So to resolve this, we can change this variable name to optional msg as the variable name, followed
[04:57] by
[04:58] I'll try to change the data
[05:00] as Optional of String.
[05:02] With that, now you have optional instance in the form of this variable which is optionalMsg.
[05:08] Now what we can do is instead of this ugly null check that we are trying to perform here, we can leverage
[05:14] methods available inside the optional instance.
[05:17] So with the help of this optionalMsg, I can try to invoke a method which is isPresent().
[05:24] So this isPresent() is going to give me a boolean value true if there is a value present inside my optional
[05:30] instance, we can confirm the same by reading the documentation here.
[05:34] So if a value is present it is going to return true, otherwise it is going to return false.
[05:39] Let me go back to OptionalDemo.
[05:40] The developer is going to do only if the return type of the method is optional type, whereas if the
[05:46] return type from the method is a normal String object, then it's an assurance to the developer that
[05:53] he or she is always going to receive a proper object.
[05:56] Now inside this if block, if you see we are trying to print out this message variable, instead, we
[06:02] want to display the message that is returned from the sayHi() method.
[06:07] Now I'm sure whenever these if condition is passed, there is an element inside my optional instance.
[06:13] So how to get that element using the get() method.
[06:16] So let's use this optionalMsg and invoke the get() method.
[06:21] So whenever I'm invoking this get() method it is going to simply return the value that I have inside my
[06:29] optional instance.
[06:30] Whereas if you try to invoke this get() method directly without performing this isPresent()
[06:35] check
[06:35] then in the scenarios where the value is null, you're going to get an exception which is no such element
[06:41] exception.
[06:42] Otherwise we are going to get a proper value as an output.
[06:45] So that's why always make sure whenever you are invoking the get()method, please check if the value
[06:51] is present or not with the help of this method.
[06:53] So now if I try to execute this code, if the number is a even number, we should be able to see the
[06:59] output which is
[07:00] Hi World, let me try to execute one more time.
[07:03] This time both the numbers are odd numbers.
[07:05] That's why I'm not getting any output.
[07:07] Instead isPresent() we can also invoke
[07:11] isEmpty() method. isEmpty() method
[07:13] it is going to give me a true as an output whenever the value is not present inside my optional.
[07:19] Otherwise it is going to give me false.
[07:20] So if you want to use isEmpty() to validate if a given optional has some content or not, then use
[07:27] the Not condition.
[07:28] So with that so not of
[07:30] isEmpty() means there is some element inside your optional instance.
[07:34] So this code is also going to work perfectly.
[07:36] So here you can see the second instance I got a odd number.
[07:40] That's why I didn't get any output.
[07:41] Let me run this one more time.
[07:43] This time you can see the second method got even number.
[07:46] That's why I'm getting the output as.
[07:48] Hi world, I hope you are clear with the discussion that we have done so far around the optional.
[07:53] Everything that we have discussed around the optional I have mentioned in these two slides.
[07:57] So please note that with the optional we are not going to get rid of the NullPointerException.
[08:04] Using these Optional, we are only going to handle the NullPointerExceptions gracefully.
[08:10] So how we are able to achieve that?
[08:12] We are communicating to the other developers who are trying to invoke a method saying that that this
[08:17] method may potentially have a null value.
[08:20] So how we are going to communicate that by having a return type of the method as Optional, if the return
[08:26] type from the method is optional, then obviously the developer will not be able to invoke the methods
[08:32] of the objects like toUppercase() directly.
[08:34] First, the developer has to work with the optional related methods like a get or isPresent() post
[08:41] that only the developer will be able to get actual object that is wrapped inside the optional instance.
[08:49] This way, the optional class indirectly encouraging the developers to handle the NullPointerException
[08:56] gracefully.
[08:57] I also give some examples here on how to create an Optional instance.
[09:01] So these are all the different approaches like emptyOf() and ofNullable() that we have discussed so
[09:06] far.
[09:07] In the next slide, I also highlighted about an important point, which is if you try to invoke the
[09:12] get() method available inside the optional directly with without checking if an element is present or
[09:18] not
[09:18] with the help of isEmpty(), or with the help of isPresent(), you're going to get a beautiful runtime exception,
[09:24] which is no such element exception.
[09:26] So instead of NullPointerException, you're going to get some other exception.
[09:30] So that's why
[09:31] but always good developers, whenever they see the optional as an return type from a method, they will
[09:36] make sure they're not invoking the get() method directly.
[09:40] I also have a meme for the developers who are trying to invoke the get() method without using isPresent()
[09:47] method.
[09:47] So this is the expression that is method is going to give to you.
[09:51] Saying that I'm a joke to you.
[09:54] I'm there for you to check if the element is present or not without using me
[09:58] if you try to use the
[09:59] get() method, you are obviously going to get no such element exception.
[10:03] That's why this method is giving these helpless expression to the developers who are trying to use get()
[10:08] method directly without using isPresent()method.
[10:12] I hope you like this.
[10:13] Now, before we try to close this lecture, let me highlight the advantages that we have with the optional.
[10:18] The very first advantage is we don't have to perform the null checks.
[10:22] There are no more required.
[10:24] And at the same time, whenever you use optional properly, you're not going to get any
[10:29] NullPointerException.
[10:29] At the worst case, you may get no such element exception.
[10:33] And the third advantage is whenever you are using this optional, you can develop the clean and neat
[10:38] APIs at the clean programs inside your project.
[10:42] And at last, there is no need of writing a lot of boilerplate code handling the NullPointerException.
[10:48] With the help of the methods available inside the Optional, you will be able to write some clean and
[10:53] less code to handle the NullPointerException.
[10:55] .
[10:56] I hope you are clear
[10:57] thank you and I'll catch you in the next lecture,
[10:59] bye.

----------------------------------------

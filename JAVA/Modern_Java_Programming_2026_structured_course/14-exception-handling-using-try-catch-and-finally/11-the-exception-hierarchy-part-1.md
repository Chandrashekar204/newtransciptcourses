# 14.11 — The Exception Hierarchy - Part 1

> Section 14: Exception handling using try, catch and finally

[00:00] As of now, whenever we are trying to declare a catch block to handle an exception, we're trying to
[00:06] provide a class name like NullPointerException, StringIndexOutofBoundsException.
[00:11] or ArrayIndexOutofBoundsException or Exception.
[00:14] So these are all the Java classes.
[00:16] So if you can open any of these class you'll be able to see that these are Java classes.
[00:21] But here I want to highlight about an important point.
[00:25] We can't mention our use any Java class as part of the catch block definition.
[00:31] For example, here I can try to mention String because String is also a Java class.
[00:36] Inside the Java library you can see I'm getting a compilation error because Java only allows certain
[00:42] set off exception classes to be defined as part of the catch block.
[00:47] With that, you may have a question which is how can I identify whether a Java class can be used as
[00:53] part of the catch block definition?
[00:55] So that's a great question.
[00:57] Let me try to explain the same. Inside Java
[00:59] all exceptions that we have
[01:01] they follow an exception hierarchy or inheritance hierarchy.
[01:06] Like you can see at the top we have a Throwable class.
[01:10] So this is a super class that you can think for all kinds of exceptions that we have inside the Java library.
[01:17] Under Throwable class, there are two subclasses like Error is one subclass and Exception is
[01:24] another subclass.
[01:25] And similarly under Exception subclass we have another subclass which is RuntimeException.
[01:31] And this RuntimeException we have many other subclasses which we can't list here.
[01:36] On the similar lines, there are good amount of exceptions which are acting as a subclasses.
[01:41] For the Exception class, I can also show you this hierarchy very quickly inside the JDK library.
[01:47] So first let me open the Throwable.
[01:50] So these are superclass for all exceptions
[01:53] inside Java.
[01:54] This is present inside the java.lang package.
[01:58] If you try to read the documentation it is very clear that the Throwable class is a superclass.
[02:03] For all errors and exceptions in the Java language.
[02:07] I will explain you what is an difference between an runtime error and runtime exception in a few minutes.
[02:14] For now, let's focus on the inheritance hierarchy of all the exceptions and the errors that we have
[02:19] inside Java library.
[02:20] You can also see they also highlighted only objects that are instances of this class are one of its
[02:26] subclasses, are thrown by the Java virtual machine, or can be thrown by the Java throw statement.
[02:33] Similarly, only this class are one of its subclasses can be the argument type in a catch clause.
[02:39] So this confirms we can only use the objects of this class or its subclasses as the input arguments
[02:46] to the catch block.
[02:47] Similarly, the same applies for the throw and throw statement.
[02:50] We are going to discuss what is a throw and throw statement in the coming lectures.
[02:54] For now let's focus on the catch block.
[02:56] The also highlighted about the two subclasses of this class, which is Error and Exception.
[03:01] So let me open this Error.
[03:03] You can see this is another class which is extending the Throwable.
[03:08] And the Throwable is going to act as a superclass.
[03:10] Similarly if you can open this exception, this is also another subclass which is extending the Throwable
[03:16] superclass.
[03:17] So all the runtime errors that we have inside Java, they are going to extend the error as a superclass.
[03:24] Similarly, all exceptions inside Java they are going to have two types of superclasses one is the Exception
[03:31] itself, the other one is RuntimeException.
[03:34] So let me open the RuntimeException.
[03:38] So this is also present inside the java.lang package.
[03:41] So there is a reason why all exceptions are divided into so many subcategories.
[03:46] We're going to discuss about this reason in few minutes.
[03:49] For now I'm assuming your super clear about the exception hierarchy.
[03:53] At the top we have Throwable.
[03:54] Under the Throwable we have two subclasses Error and Exception.
[03:58] All the runtime errors inside Java, they are going to extend the Error class as a superclass and similarly
[04:04] under Exception there are two types of exceptions.
[04:07] One is a set of exceptions where they are going to have the superclass as a RuntimeException, whereas
[04:13] the remaining set of exceptions they are going to directly inherit the Exception class.
[04:18] So based upon these categorization inside Java, all the exceptions they are categorized into two types.
[04:25] One is unchecked exception and the other type is checked exceptions.
[04:30] So all the subclasses of Error and RuntimeException we can call them as unchecked exceptions, whereas
[04:37] the subclasses that are directly inheriting from the Exception class, we can call them as checked exceptions.
[04:44] So there is a clear difference between checked and unchecked exceptions, which we are going to discuss
[04:49] in the coming lectures.
[04:50] And this topic is going to be a super important topic for your interviews as well.
[04:55] That's why I'm going to discuss about unchecked exceptions and checked exceptions in a separate
[05:00] lecture.
[05:00] For now
[05:01] please note that all subclasses of Error and RuntimeException classes.
[05:05] We can treat them as unchecked exception, whereas the subclasses of exception we can treat them as
[05:11] checked exception.
[05:12] You might be thinking that all the exceptions inside Java, they are going to be present inside the
[05:17] package java.lang, but that's not correct.
[05:20] There are a few exceptions as well which are present inside other packages.
[05:24] For example, IOException is present inside the java.io package.
[05:29] Because Java team developed all the logic related to the input and output inside the java.io package,
[05:37] that's why they might have felt keeping the IO related exceptions inside the java.io package itself
[05:43] is going to make sense rather than Java lang, so that's what they have done.
[05:48] Similarly, there are some exceptions available inside the java.util package.
[05:52] For example, there is an exception with the name MissingResourceException.
[05:57] So this exception is present inside the package java.util.
[06:01] I hope you are clear about these initial introduction about the exception hierarchy.
[06:06] We need to discuss more on the same.
[06:08] Let's continue the same in the next lecture as well.
[06:11] Thank you,
[06:12] bye.

----------------------------------------

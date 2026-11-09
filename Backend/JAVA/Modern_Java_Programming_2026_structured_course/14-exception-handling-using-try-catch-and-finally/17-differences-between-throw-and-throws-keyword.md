# 14.17 — Differences between throw and throws keyword

> Section 14: Exception handling using try, catch and finally

[00:00] There are a good amount of differences between throw and throws
[00:03] keyword.
[00:04] Let's try to understand one by one.
[00:06] The very first difference is using throw keyword
[00:10] we can manually throw an exception when an error or unexpected situation arises, and we can use this
[00:18] throw keyword only inside a method body.
[00:21] Whereas coming to the throws keyword, throws keyword is used in the method signature to indicate that
[00:28] a given method may throw list of exceptions due to certain statements or actions within its body.
[00:35] So please be very clear about the placements.
[00:38] Throw can always be used inside the method body, whereas throws can be used only in the method signature.
[00:44] Now coming to the syntax on how to use these keywords whenever we are using the throw keyword, after
[00:51] mentioning the throw keyword, we need to provide an object or an instance of an Exception class.
[00:57] That means always the throw keyword should be followed by the instance variable containing the Exception
[01:04] object.
[01:05] For example, here, immediately after the throw keyword, I'm trying to create the object of the
[01:10] ArithematicException class by using the new operator.
[01:13] If I don't mention this new operator, you can see I'm going to get a compilation error.
[01:18] That means my throw keyword
[01:19] always going to expect a object of a class, which is a subclass of Throwable.
[01:26] If I try to create an object of String, I'm going to get a compilation error because String is not
[01:32] a subclass of Throwable class, which is a superclass for all the exceptions and errors inside the Java
[01:39] library.
[01:39] That's why always make sure you are creating the object of a subclass of Throws class.
[01:45] I hope this is clear.
[01:46] Coming to that throws keyword syntax,
[01:49] it is very simple.
[01:50] Whenever you are trying to mention throws keyword inside a method signature.
[01:54] After the throws keyword, you need to mention the list of class names of the exceptions that may be
[02:00] thrown by the method.
[02:02] So all these list of exceptions, they need to be separated by comma.
[02:05] The next difference is using the throw keyword,
[02:08] we can only throw one exception at a time, whereas with the help of throws keyword, we can declare
[02:14] multiple exceptions that are separated by commas.
[02:18] The last difference is somewhat complicated to understand.
[02:21] That's why let's put some good amount of efforts to understand these last difference.
[02:26] Whenever we are throwing unchecked exceptions with the help of throw keyword, there won't be any issues.
[02:33] The unchecked exception it is going to be propagated very easily to the parent classes as well.
[02:39] Whereas if you try to throw a checked exception using the throw keyword, in such scenarios, the Java
[02:46] compiler will make sure that a method is either handling that checked exception or it added the checked
[02:53] exception details to the method signature with the help of throws
[02:56] keyword.
[02:57] Let me show you a demo around this.
[02:59] As of now here you can see I'm trying to throw an ArithmeticException which is unchecked exception,
[03:05] whereas if I try to throw and check it, exception things will change a lot.
[03:10] For example, let me try to throw one of the checked exception which is FileNotFoundException.
[03:16] As soon as I tried to throw an FileNotFoundException, you can see I'm getting a compilation error
[03:21] saying that that this method is not handling these checked exception.
[03:26] So to resolve this issue I need to have a catch block or I need to add the throws statement to the method
[03:34] signature by mentioning the file not found exception to the list.
[03:38] That's why whenever you are trying to throw an unchecked exception, the unchecked exception, it is
[03:43] going to be propagated very easily to the invoking methods as well.
[03:48] Whereas when you try to throw a checkered exception, your Java compiler will make sure that a given
[03:53] method either it is handling it or it is throwing to the caller methods with the help of throws
[03:58] keyword I hope you are clear.
[04:00] Let me revert back to the normal unchecked exception, which is ArithmeticException.
[04:06] In the similar lines, whenever you are trying to use a throws keyword to throw the unchecked exceptions,
[04:12] the propagation is going to be super easy.
[04:15] Like here you can see inside the ThrowsDemo.
[04:17] As of now I have a try and catch block.
[04:20] Even if I remove these try and catch block, nothing is going to happen because these are unchecked
[04:26] exceptions and whoever is invoking these method, they will not be forced to handle them.
[04:33] Whereas if I try to throw one of the checked exception which is like FileNotFoundException, then
[04:39] immediately a compilation error may arise
[04:42] in all the classes where this divide() method is being invoked.
[04:45] You can see the compiler is trying to force the developer to handle the exception, which is
[04:51] FileNotFoundException because it is a checked exception.
[04:54] So that's why always please note about these checked and unchecked exceptions when ever
[04:59] you are trying to use them as part of the throws and throw keyword.
[05:04] So that is what the last point is trying to highlight with this.
[05:08] I hope you are clear with all the differences between throw and throws keyword.
[05:11] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

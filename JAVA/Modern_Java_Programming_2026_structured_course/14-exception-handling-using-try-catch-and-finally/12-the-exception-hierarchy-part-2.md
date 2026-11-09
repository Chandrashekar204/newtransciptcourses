# 14.12 — The Exception Hierarchy - Part 2

> Section 14: Exception handling using try, catch and finally

[00:00] Based upon our previous lecture discussion, all the exceptions and errors inside Java library, they
[00:07] are extending a common superclass which is Throwable.
[00:11] If you go and check that java.lang package where there are majority of the exceptions and errors
[00:17] are available, you will find almost three dozen most commonly used exception classes and a couple of
[00:23] dozen error classes.
[00:25] So all these subclasses of Throwable, they're not going to define a lot of new methods, or they're
[00:31] not going to override the methods from the Throwable.
[00:34] Instead, all the subclasses of Throwable, they are going to utilize the methods available inside the
[00:40] Throwable class.
[00:41] For example, you can see under the Error class we don't have any methods except to some constructors.
[00:47] So you can see all of them.
[00:49] They are constructors.
[00:50] Similarly, under the RuntimeException also we have only constructors but not any methods.
[00:56] The same applies for the exception.
[00:58] With that it should be pretty clear for you that all the subclasses of Throwable, they are going to
[01:04] inherit the methods available inside the Throwable, and they are not going to perform any overriding,
[01:10] and at the same time they are not adding any extra functionality. Inside throwable
[01:15] there are many methods, but we need to understand what are the most important methods available inside
[01:21] Throwable and under which scenarios we should use them.
[01:24] So let's try to understand the same.
[01:26] The very first common method that you're going to use with the help of the object of any Exception class
[01:33] is PrintStackTrace.
[01:34] We already saw the demo of this in the previous lecture.
[01:37] Whenever you are looking to print the stack trace details of an exception or an error that has occurred
[01:44] at the runtime, you can simply invoke these method.
[01:48] It is not going to return anything, but instead it is going to print all the stack trace details of
[01:54] the exception, like all the method details and the hierarchy of the method invocations, along with
[01:59] the details where the exception has occurred.
[02:02] So all such details we will be able to see on the console whenever we use printStackTrace() method.
[02:08] So you can use this method inside Catch Blocks to understand more details about where the exception
[02:14] happened.
[02:15] We don't have to specifically use System.out.println() to print the details of the exception.
[02:20] Instead, we can rely on these readily available method which is printStackTrace().
[02:25] But please note that please never use this method inside any production code, because if you use this
[02:32] inside a production code, there is a good chance that it is going to expose some sensitive information
[02:38] about your libraries and classes and methods inside the console.
[02:43] So this can give some clues to the hackers.
[02:46] That's why inside production code never use them
[02:48] instead, try to use the logging framework to log the exception details into log files.
[02:55] So whenever we perform the logging in production environments, the logging statements, they are going
[03:00] to be logged separately inside separate log files which your server admins
[03:05] they can protect them with the proper security.
[03:07] The next method that we have here is getStrackTrcae().
[03:11] So it is going to give you the array of stack trace element objects representing the method calls
[03:18] that led to the point where the exception or error occurred.
[03:22] For example, if you are trying to invoke a method1() from the main() method and this method1() is
[03:28] invoking the method2(),
[03:29] method2()
[03:30] invoking the method3().
[03:31] And if the runtime exception happened at the method3(), then all the method hierarchy or the stack
[03:37] trace details you can fetch with the help of these getStackTrace() method.
[03:42] This is not going to be commonly used by the developers, but this is available if you are interested.
[03:47] You can invoke them to understand the stack trace details which are leading to the various method invocations.
[03:54] The next method that we have inside the Throwable class is getMessage().
[03:58] Whenever you want to know what is the reason of an exception in an user friendly explanation format.
[04:05] In all such scenarios, you can use the getMessage() method.
[04:09] So this method is going to give a short description about your exception why it has occurred.
[04:15] You will not get multiple lines of error or multiple lines of exception details like when we use
[04:22] printStackTrace() method and at last we have getCause() method.
[04:26] This method it is going to return the exception or error that caused the current exception to be thrown
[04:33] or null if the cause is unknown or nonexistent.
[04:37] Sometimes in Java programs, an exception can be thrown by another exception, so there is a possibility
[04:44] that your root exception will be wrapped by another exception.
[04:49] In this kind of scenarios, if you are looking for the root exception or the main exception which is
[04:54] resulting this runtime exception, in such scenarios you can invoke these getCause() method.
[05:00] So these methods, they are going to help you to understand the reasons are the details why an exception
[05:06] occur many times whenever you want to fix a defect, or whenever you want to fix a runtime exception,
[05:13] you can rely on these methods inside your local system to debug the program and post that
[05:19] you can decide how to fix the exception or how to handle the exception.
[05:22] Now, as a next step, let's try to understand what is the difference between error and exception?
[05:27] What kind of subclasses we have under these Error classes.
[05:31] Inside Java, the Error class which is present inside the java.lang package.
[05:36] It is going to act as a parent class for all the runtime errors that can happen.
[05:41] And we know this Error class inherits Throwable class.
[05:45] So what is an Error we already saw what is an exception in the previous lecture.
[05:49] It is an unexpected output that may occur due to some invalid data, or due to some invalid actions
[05:57] performed by an end user, but coming to the error, it is going to be thrown by the Java virtual machine.
[06:03] So whenever these errors are being thrown by the Java virtual machine, they are going to be considered
[06:08] very critical or very severe because your JVM is going to throw these kind of errors only in very critical
[06:16] scenarios, like if there is no proper memory available inside your system for the JVM to run the Java
[06:21] programs in all such critical conditions, only these errors will be thrown by the JVM.
[06:28] Let's see a few examples of such errors.
[06:31] Like you can see, the very first error is StackOverflowError.
[06:34] We know inside Java the JVM is going to maintain a stack memory using which it is going to maintain
[06:41] all the method invocations, and inside the stack memory only, it is going to maintain the local variables.
[06:48] So sometimes if you try to run a infinite loop, or if there is no enough memory assigned to the JVM
[06:54] to run the Java programs, in all such scenarios, you're going to get an Stack Overflow error.
[07:00] The next error that we have is NoClassDefFoundError.
[07:04] So this error is going to be thrown by the JVM when it is not able to identify a class inside the classpath
[07:11] or inside the dependent libraries.
[07:14] For example, think like you're trying to write a Java program to generate a PDF document based upon
[07:20] the given data.
[07:21] In such scenarios, in real projects, definitely you're going to rely on the third party libraries
[07:27] where they are going to give good amount of utility classes and methods to generate the PDF very quickly.
[07:33] In this kind of scenarios, think like at runtime one of the class, which is dependent by your Java
[07:38] program.
[07:38] It is not available inside the third party library or the dependent library.
[07:43] In such scenarios, at runtime, JVM is going to throw an error saying that NoClassDefFoundError
[07:49] and at last we have OutOfMemoryError.
[07:53] We know JVM needs memory to run our Java programs, so whenever we try to run our Java programs behind
[07:59] the scenes JVM is going to create lot many Java objects.
[08:04] And these objects are going to be stored inside the heap memory.
[08:07] For some reason, if there are too many objects are getting created, or if the garbage collection is
[08:13] not able to clean the memory properly, or if there are some memory leaks happening inside your Java
[08:18] program.
[08:19] In all such scenarios, you're going to get an OutOfMemoryException.
[08:23] Because whatever default memory that we are trying to provide to the JVM or the Java program, it is
[08:29] not going to be sufficient.
[08:31] And when it is not sufficient, the JVM, it is going to throw this error.
[08:35] So if you see here there is a common point.
[08:37] All these errors are going to be thrown by the JVM due to the limitations inside the system, maybe
[08:43] due to lack of enough memory or maybe due to missing class.
[08:47] So these kind of errors, we should not try to handle them with the help of catch block, because even
[08:54] if you try to handle them, you can't do anything.
[08:57] If there is no memory available at runtime, what are you going to do by by catching this error, you
[09:02] can't add extra memory at runtime.
[09:05] Whenever you want to add extra memory, you need to restart your application or you need to restart
[09:10] your Java program.
[09:11] The same applies for StackOverflowError.
[09:14] NoClassDefinitionFoundError at runtime.
[09:17] Think like your JVM is not able to identify a given class.
[09:20] That's why it is going to throw an NoClassDefinitionFoundError.
[09:24] You will not be able to handle these kind of error, because at runtime you can't fix the error.
[09:29] By providing a dependent class, you need to check the library and you need to properly build the dependency
[09:36] library.
[09:36] Only by such actions, these kind of errors, they are going to be resolved.
[09:40] So since you can't perform any action at runtime, whenever these errors happen, it is always advisable
[09:47] to not handle these errors inside your Java program.
[09:51] I hope you are clear.
[09:52] Like what is an error in real projects?
[09:55] Most of the times we will not face these errors, we will only face runtime
[10:00] exceptions
[10:00] based upon defects inside our code are based upon the invalid data, or based upon invalid
[10:07] actions performed by the end user.
[10:09] That's why whatever minimum information that we have discussed around the error should be enough for
[10:14] your interviews or for your real projects as well.
[10:17] I'm not saying there are only three errors inside the entire Java library.
[10:21] There are other types of errors also available, but you will hear about these errors most commonly.
[10:27] That's why I tried to discuss about them and shared more details around them.
[10:31] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

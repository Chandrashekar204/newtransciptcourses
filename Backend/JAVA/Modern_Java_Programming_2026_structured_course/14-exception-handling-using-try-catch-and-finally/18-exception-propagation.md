# 14.18 — Exception Propagation

> Section 14: Exception handling using try, catch and finally

[00:00] Let me explain about what is an Exception Propagation
[00:04] Inside this lecture. We know whenever an exception is being thrown from a method, and if the same
[00:10] is not being catched or caught within that method, then the exception will try to propagate to the
[00:16] calling method.
[00:17] So this process continues until the exception is properly handled with the help of a catch block or
[00:25] it reaches the top level method.
[00:28] So what will be the top level method inside our Java programs?
[00:31] It is main() method in the case of an unchecked exception, being trying to propagate to the caller methods
[00:39] or the parent methods, then in such scenarios, there is no mandatory to have a throws statement or
[00:45] to have a catch block, so the unchecked exception eventually it will propagate to the top level method
[00:51] or a main() method.
[00:52] Whereas in the scenario of checked exceptions, since the compiler is going to force the programmers
[00:58] to handle the checked exceptions either with the help of throws or with the help of catch block.
[01:03] In the case of checked exceptions, the exception will try to propagate to the nearest catch block,
[01:09] or it will keep propagating to the main() method or the top level method.
[01:14] Let me show you a example here.
[01:16] Like you can see inside my method stack at the bottom we have the main() method.
[01:20] main() method is invoking method1() followed by method2(),
[01:23] method3(),
[01:24] method4(),
[01:25] method5().
[01:26] Think like
[01:26] there is an exception occurred inside the method5().
[01:30] In this kind of scenario, my method5(),
[01:32] first, it will check if there is any catch block handling a given exception.
[01:37] Then the exception will not be propagated to the parent methods or the caller methods inside the method
[01:44] stack, whereas if the exception is not handled with the help of a catch block, in such scenarios,
[01:50] the exception will be propagated to the method4(), and this process will keep on continue until there
[01:56] is a catch block inside a method where the exception is being handled, or it reaches to the main() method.
[02:03] I can also show you a quick demo around this Exception Propagation
[02:07] very quickly.
[02:07] Inside my intelliJ I'm going to create a new Java class.
[02:12] The class name that I'm going to mention here is ExceptionPropagationDemo.
[02:18] So inside this class first I'm going to create the main() method post that
[02:23] I'm going to create a static method with the name method1().
[02:28] And it is not going to accept anything.
[02:30] For now let's try to keep it as simple.
[02:32] Very similarly, I'll try to create multiple other static methods with a different names like method2(),
[02:38] method3().
[02:40] So now from main() method I want to invoke the method1(), and from the method1() I will try to invoke
[02:48] the method2(), followed by inside method2() I will try to invoke the method3(), whereas inside
[02:56] the method3() I will try to manually throw an unchecked exception.
[03:01] Maybe I can try to throw NullPointerException by using throw new NullPointerException.
[03:07] And to this constructor I will provide a message which is an null pointer exception occurred.
[03:15] So if I try to execute this program, you will be able to see that the exception is propagated to the
[03:21] main() method, like from method3() to method2(), metho2() to method1(), and from method1()
[03:27] to the main() method.
[03:28] Whereas if I have a catch block in the method1() to handle the NullPointerException, then in such
[03:35] scenarios the exception is not going to be propagated to the main() method.
[03:38] Let me show you the same.
[03:39] So first I'm going to mention that try block and inside the try block I'm going to invoke the method2()
[03:44] and post that
[03:46] I'm going to catch the NullPointerException inside the catch block
[03:51] I'm going to write a System.out.println(), and I'm going to invoke the ex.getMessage(),
[03:58] and post that inside the main() method
[04:00] I'm also going to write a another System.out.println() saying that main() method.
[04:05] So these are input I'm trying to print with this System.out.println().
[04:10] So if I try to execute this program you can see I'm getting a
[04:14] NullPointerException occurred.
[04:15] The exception is not propagated to the main() method.
[04:18] And it did not disturb the further execution of the main() method.
[04:22] That's why I'm able to see this main() method output inside the console.
[04:27] Like you can see, if I don't have this try and catch blocks, then obviously the exception is going
[04:33] to be propagated to the main() method as well.
[04:35] And with that we will not be able to execute these statement.
[04:39] So let me execute this program.
[04:41] And this time you can see the exception eventually propagated to the main() method.
[04:46] And that's why the next statement that we have after the method1() is not being executed.
[04:51] So this is what is going to happen as part of exception propagation whenever we are trying to throw
[04:57] an unchecked exception.
[04:59] But
[04:59] let's see the story with the checked exception.
[05:02] This time I'll try to change this to throw new FileNotFoundException and post that I'm going to
[05:09] update this message to File not Found
[05:12] Please check.
[05:14] So this is the message I want to convey as part of this exception.
[05:18] Now you can see I'm getting a compilation error because this is a checked exception.
[05:23] And when this checked exception is being thrown from this method3().
[05:27] The method3() is not even handling this checked exception either with a catch block or with a throw
[05:33] keyword.
[05:34] So to resolve this, we can simply mention throws followed by FileNotFoundException.
[05:40] And with that, now you can see we are going to get an error inside the method2(), because method2()
[05:46] also is not handling the checked exception either with a catch block or with the throws keyword.
[05:52] So to fix that we need to copy
[05:54] this throws keyword along with the FileNotFoundException and mention the same inside the method2().
[05:59] And with that, now my method1() will have a compilation error.
[06:03] So I'm going to mention the throws keyword along with the FileNotFoundException.
[06:07] So now my main() method is going to have these compilation error.
[06:11] And at last you can see all the compilation errors are resolved.
[06:14] Because now all the methods they are having a throws keyword along with the FileNotFoundException
[06:21] inside the method signature or
[06:23] the other way is by having a proper catch block handling the given checked exception.
[06:28] For example, inside the method1() I can have a try block
[06:31] inside the try block I can have method2() followed by catch
[06:35] Inside the catch I can try to mention FileNotFoundException ex and post that
[06:41] I will just try to print the message with the help of
[06:46] ex.getMessage() with this
[06:48] this throws keyword is unnecessary because we are handling with the catch block.
[06:53] So let me remove this.
[06:54] Now the throws keyword here inside the main() method is also unnecessary.
[06:59] That's why I have removed the same.
[07:01] If I try to execute this program.
[07:03] You can see please check message came as part of the method one exception handling and post that since
[07:09] the exception is not propagated to the main() method, we are able to see this main() method inside the
[07:15] console as an output.
[07:17] Before I try to close this lecture, let me show you one more important demo.
[07:21] As of now you can see this method1()
[07:24] it is trying to handle the FileNotFoundException.
[07:27] But if I try to throw some other exception, maybe if I try to throw NullPointerException then definitely
[07:34] this catch block is going to be useless and the exception is going to be propagated to the main() method.
[07:41] And that's why we are not going to see these inside the console.
[07:44] Let me execute this program.
[07:46] You can see we are not seeing any output inside the console with the message main() method.
[07:51] We are directly seeing the exception details.
[07:54] So this is how the exception propagation is going to work.
[07:57] That's why always make sure you are performing the exception handling properly.
[08:04] If you're not handling the exception handling properly, eventually the exception is going to be propagated
[08:10] to the parent methods or the invoking methods, and sometimes you may get unexpected results.
[08:17] I hope you are clear.
[08:18] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

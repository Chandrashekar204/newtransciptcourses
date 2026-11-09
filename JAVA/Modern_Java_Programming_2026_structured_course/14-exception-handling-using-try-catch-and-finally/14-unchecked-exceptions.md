# 14.14 — Unchecked Exceptions

> Section 14: Exception handling using try, catch and finally

[00:00] Unchecked
[00:01] exceptions are the exceptions that the Java compiler does not require or force the programmer to handle
[00:08] in the code.
[00:09] Why?
[00:09] Because the compiler cannot detect these kind of exceptions that may happen at runtime.
[00:16] The examples of unchecked exceptions are NullPointerException,
[00:20] ArrayIndexOutofBoundsException,
[00:22] ArithmeticException.
[00:23] These kind of exceptions, the compiler cannot detect how my compiler will know that an object can be
[00:30] a null during the compilation itself.
[00:32] It is not going to detect that because it can't check the object, since the objects are going to be
[00:38] created at runtime inside the heap memory.
[00:41] Similarly ArrayIndexOutofBoundsException this
[00:43] also my compiler cannot detect because during the compilation my compiler cannot check array object
[00:51] how many elements it is going to have, what is the length of the array.
[00:54] So all these details it cannot detect during the compilation, as the array objects are going to be
[01:00] created during the runtime only on the similar lines.
[01:03] ArithmeticException also is a unchecked exception, because my compiler cannot detect the errors that
[01:11] may happen during the compilation time based upon my arithmetic operations like division, multiplication,
[01:19] addition.
[01:20] So in all such scenarios, since it cannot detect, it will not force the developer to handle this exception
[01:26] as well.
[01:26] In simple words, we can say Java compiler will not complain and continue with its work.
[01:33] Even if you write a risky code that may result in one of the unchecked exceptions.
[01:38] However, it is generally a good practice to handle all kind of exceptions wherever possible inside
[01:45] a Java program.
[01:46] To improve the robustness and reliability of the program. We also have a shortcut to identify unchecked
[01:54] exceptions.
[01:55] All unchecked exceptions
[01:57] they are going to have a same superclass, which is RuntimeException available inside the
[02:04] java.lang package.
[02:05] Apart from these RuntimeException subclasses, all the Error subclasses also are considered as unchecked
[02:12] exceptions.
[02:13] The errors like StackOverflowError, OutofMemoryError, NoClassDefinitionFoundError.
[02:18] So all these errors are also comes under unchecked exceptions, and it is recommended to not worry about
[02:25] these errors because even by handling these errors with the catch block is not going to make any difference
[02:31] inside your program.
[02:32] Let me show you that demo of unchecked exceptions very quickly.
[02:36] Inside my IntelliJ, I'm going to create a new Java class.
[02:41] The Java class name is going to be UncheckedExceptionsDemo.
[02:46] So inside this class, first I need to create the main() method post that I'm going to write some logic
[02:52] that may result into NullPointerException or ArrayIndexOutofBoundsException.
[02:57] We already have such logic.
[02:59] Let me go to the class, which is MultipleCatchDemo.
[03:03] So inside this class you can see we have a logic that may result into NullPointerException and a
[03:09] StringIndexOutofBoundException.
[03:11] We can take this code and I can paste it inside this main() method.
[03:15] Let me remove this
[03:16] try related logic logger related logic.
[03:19] And you can see here nowhere my compiler is asking me to handle these exceptions.
[03:25] That may happen like NullPointerException or StringIndexOutofBoundsException.
[03:31] The reason is compiler is clueless during the compilation time, what content I'm going to have inside
[03:38] an object, or how many elements I'm going to have inside an array because my compiler is clueless on
[03:46] what kind of data that my String object is going to have at runtime.
[03:51] At this point of time, a String object is not going to be created.
[03:54] But whenever we are trying to assign a data to the String object reference variable, then the physical
[04:00] object is going to be created in the heap memory.
[04:02] And when that is going to happen only during the runtime.
[04:05] That's why all unchecked exceptions cannot be detected by your compiler.
[04:10] And with that reason, it is not going to force you to handle inside your Java program.
[04:15] But like I said, it is always a good practice to handle all kind of exceptions inside your Java code.
[04:22] You as a Java developer, you know in a better manner on what kind of exceptions that your code may
[04:28] throw.
[04:28] That's why to handle unexpected situations like invalid input data or a bug inside the Java code.
[04:35] For all these kind of scenarios, it is always recommended to have exception handling logic.
[04:40] I hope you are clear about that demo of the UncheckedExceptionDemo.
[04:44] I'm going to keep this class like this only, so that it is going to give some clarity to you that the
[04:50] compiler is still is going to compile your program successfully without any compilation errors.
[04:56] I am providing a list of checked and unchecked.
[05:00] For your reference, this is not the complete list of checked and unchecked exceptions.
[05:05] I'm only trying to give a few, most commonly face ID checked and unchecked exceptions inside your Java
[05:12] project.
[05:13] So inside interviews, if someone asks you what is unchecked and unchecked exception, you can try to
[05:19] share the definition with them and post that if they ask the examples, you can give these list of examples
[05:25] as a reference to them.
[05:27] I also provided details on when these kind of exception may happen.
[05:31] For example, you can see MalformedURLException.
[05:35] So this is a checked exception which which may happen whenever you are trying to create an URL object
[05:41] based upon the given URL.
[05:43] Since you are going to create the object of URL based upon a String URL, your compiler will ask you
[05:49] to handle this exception, because your compiler is going to anticipate a scenario where if someone
[05:56] passes an invalid URL String data. I hope you are clear
[06:00] with all the discussion that we have done around the checked and unchecked exceptions, I can't provide
[06:06] all the list of exceptions that are available inside JDK or Java library.
[06:10] That is unnecessary as well.
[06:12] You will get to know about more and more exceptions that you need to handle inside a Java program in
[06:18] future
[06:19] whenever you are trying to understand a Java program which is written by other senior developers or
[06:24] tech leads, you can try to understand how they are performing the exception handling.
[06:28] Though the syntax is always going to be the same like we discussed, but you need to understand what
[06:33] kind of exceptions they are trying to handle, how they are handling, because the handling logic will
[06:39] differ from project to project based upon your business requirements.
[06:43] Few projects, they may say, just handle the exception by logging the exception details into your logger
[06:49] file.
[06:49] Whereas few other projects they may say to trigger an email to the production support team.
[06:55] So the handling mechanism can be anything, but you should be perfect with the syntax on how to build
[07:01] the try block, catch block, finally, block and try with resource.
[07:05] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

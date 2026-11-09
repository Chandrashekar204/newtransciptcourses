# 14.13 — Checked Exceptions

> Section 14: Exception handling using try, catch and finally

[00:00] Inside Java
[00:01] all the exceptions and errors.
[00:03] They are categorized into two categories.
[00:06] One is checked and other one is unchecked
[00:09] exceptions.
[00:09] Inside this lecture, let's try to put some efforts to understand more details about these checked and
[00:15] unchecked exception.
[00:16] First, we are going to focus on checked exception.
[00:19] If you ask me what is the definition of checked exception?
[00:22] It is very simple.
[00:23] Whenever a compiler is forcing the developer or programmer to handle a specific exception.
[00:31] So such exceptions we call them as checked exceptions.
[00:34] So why we call them as checked exceptions?
[00:37] Because your compiler is checking whether the programmer handled a particular exception or not.
[00:44] Examples of checked exceptions are IOException, SQLException and a FileNotFoundException.
[00:51] These are the most commonly faced checked exceptions by developers on day to day work.
[00:56] So whenever you are writing a code inside a Java method that is going to deal with the input and output
[01:03] operations like accepting an input.
[01:06] In all such scenarios, your compiler knows that you are writing the code related to input and output
[01:12] processing.
[01:13] That's why it will force you to handle the IOException by saying that hey buddy, you're writing lot
[01:19] of input and output processing business logic.
[01:22] It will always be a wise decision to handle these IOException.
[01:27] Similarly, whenever you are writing a Java program which is going to run some SQL queries on top of
[01:33] a database by connecting to it in such scenarios, Java compiler knows that you are trying to write
[01:39] some SQL related business logic.
[01:42] That's why it will force you to handle the SQLException.
[01:46] And similarly, whenever you are trying to read a file, there is a good chance the file may not be
[01:52] available at a given path.
[01:53] So what should happen in this kind of scenarios?
[01:55] Since compiler is going to worry about these kind of scenarios, it will force you to handle the
[02:01] FileNotFoundException as well.
[02:03] So if someone asks you what is a checked exception, we can simply say, checked
[02:07] exceptions are the exceptions that the Java compiler is going to perform the validation at the compilation
[02:14] time, and if we don't handle them inside our code, it is going to simply throw an compilation error.
[02:21] In a funny way
[02:22] we can say Java compiler will be angry at you or at developer and throw a compilation error.
[02:29] If you write the risky code, that may result in one of the checked exceptions, but not handled it
[02:35] inside the Java method. There is also a shortcut to determine whether a given exception is a checked
[02:41] exception or a unchecked exception.
[02:43] The shortcut is checked exceptions
[02:45] they are not going to inherit the RuntimeException in the inheritance hierarchy.
[02:51] They are going to directly inherit the Exception class.
[02:54] I hope you are clear about checked exception definition.
[02:57] Let me show you that demo of these checked exceptions very quickly.
[03:01] Inside IntellIj.
[03:02] Inside my IntelliJ, I'm going to create a new Java class which is CheckedExceptionDemo inside this
[03:10] class.
[03:10] First I'm going to create the main() method post that
[03:14] inside this main() method, I'm going to write some risky code that may result into one of the checked
[03:19] exception.
[03:20] I'm going to paste few lines of code.
[03:22] All this code we have discussed in the previous section.
[03:25] Like
[03:25] first, I'm trying to create the object of BufferReader.
[03:28] Post that with the help of BufferReader, I'm trying to invoke the redLine() method.
[03:33] So whenever I'm trying to perform this redLine() method, or whenever I'm trying to invoke this close()
[03:39] method by using the BufferReader, you can see my compiler is throwing a compilation error saying that
[03:46] unhandled exception, which is java.io.IOException.
[03:51] So this is a classical example of checked exception.
[03:55] So to resolve this compilation error I need to build a try and catch block.
[04:01] And I need to make sure I'm handling the IOException.
[04:04] So how my Java compiler knows that I'm going to perform the I o operations because with the help of
[04:09] BufferReader object, I'm trying to invoke the readLine() method.
[04:13] If you go and check the redLine() method, which is available inside the Java library, you can see it
[04:18] is throwing the IOException whenever a method signature have these throws and an exception, that
[04:24] means that this method is going to throw an IOException in the scenarios whenever some unexpected things
[04:31] are happening inside the method logic.
[04:34] Since we are trying to use this redLine() method, it is our responsibility to either handle these
[04:40] IOException inside our method, or we can try to add the throws block to our method signature.
[04:47] For example, to resolve this compilation error, I can simply add throws IOException.
[04:53] So with this you can see the compilation errors are resolved.
[04:56] But with these throws, what we are trying to do is I'm not going to handle
[05:00] IOException whoever will invoke my main() method, they have to make sure to handle the IOException.
[05:07] So it's like we are throwing this responsibility to someone else.
[05:10] We are going to discuss more details about throws and throw keyword in the coming lectures.
[05:15] For now, let's not throw this IOException to someone else, because inside this main() method we ourselves
[05:21] are writing this business logic.
[05:22] That's why it is always a good practice to handle the a given exception which may get thrown based upon
[05:30] our business logic written.
[05:32] So that's why I am going to remove these throws block post that I'm going to have and try
[05:38] and inside the try I can move all this code followed by I can write a catch block and inside the catch
[05:45] block I'm going to handle the IOException with the object reference name as ex.
[05:50] And at last I can also have finally block and inside the
[05:54] finally I can mention these bf.close().
[05:57] Instead of this we can also try to use that try with resource.
[06:01] So let me try to use that try with resource.
[06:03] So inside these parentheses I'm going to create these two objects.
[06:07] So let me copy into these parentheses.
[06:10] And with that you can see we don't need to have this finally block.
[06:14] And I can simply remove.
[06:15] And I can also free myself from invoking these close() method.
[06:19] And at last inside this catch block you can write whatever handling logic that you want to build for
[06:24] your Java program.
[06:25] For now, I'm just going to write ex.printStackTrace() so that I can see the details of the exception
[06:33] inside my console.
[06:34] But like I said, please don't use this in real production applications.
[06:39] The main point that I want you to observe here is, whenever you are dealing with a Java logic that may
[06:45] result into checkered exception.
[06:46] In such scenarios, your Java compiler will force you to handle that either with the help of catch block
[06:53] or by throwing to the caller method with the help of throws keyword.
[06:57] In the similar lines, I can also show you a demo of another checked exception for the same inside the
[07:04] same class
[07:05] I'm going to create an method which is public void readFile().
[07:11] So this is a method which is going to readFile().
[07:14] So inside this method I'm going to create the object of FileReader to read a given file.
[07:20] So how to do that by using the FileReader class.
[07:23] You can see I'm trying to create the object of FileReader.
[07:27] And to the constructor of the FileReader() I'm trying to pass the path where my file is present.
[07:32] So here my compiler knows that I'm trying to read a file.
[07:36] That's why it is throwing a compilation error saying that unhandled exception which is of type
[07:43] java.io.FileNotFoundException.
[07:45] So how to fix this compilation error?
[07:48] We can either add throws keyword and after the throws keyword we can mention the FileNotFoundException.
[07:54] With this, we are not taking the responsibility of handling these exception.
[07:59] Instead, we are simply throwing to the caller() method whoever tried to invoke this ReadFile() method.
[08:06] But like I said, it's not a good practice
[08:08] always
[08:09] we should try to handle an exception if we are writing any business logic that may result into an checked
[08:16] exception.
[08:16] Here I have written with my own hands to read a file.
[08:19] Then it is my responsibility to handle it.
[08:22] Why should I throw it to someone else?
[08:24] That's why I'm going to remove this throws block and post that I'm going to mention
[08:28] try block and inside the try block I'm going to move this code followed by I'm going to have a catch
[08:35] block with the FileNotFoundException.
[08:39] And inside the catch block I can simply have ex.PrintStackTrace.
[08:44] With this you can see the compilation error is resolved.
[08:47] I hope you are clear about what is an checked exception inside the next lecture.
[08:52] Let's try to understand more details about the unchecked exceptions.
[08:56] Thank you,
[08:56] bye.

----------------------------------------

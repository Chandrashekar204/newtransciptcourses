# 5.4 — Single line Comments in Java - Demo

> Section 5: Comments in Java

[00:00] To see the demo of single line comments inside Java.
[00:03] First, I'm going to create a Java class under section5 project
[00:08] inside the source folder, I'm right clicking on the source folder and selecting the new Java class
[00:14] option.
[00:14] The class name that I want to give here is, SingleLineCommentDemo.
[00:20] So these are name.
[00:22] Once I have provided this name, I'm going to press enter and this is going to create an empty class
[00:28] like you can see here.
[00:29] The very first Java method that I want to write here is, public static void main().
[00:34] So let me try to create this.
[00:36] As a next step I will try to create some class level variables.
[00:40] So just after my class definition I'm going to create a variable or field with the name int age.
[00:48] So this variable is going to store the age.
[00:51] But do you know whose age it is,
[00:53] is it a person age or is it an animal age or is it an tree age?
[00:58] Since there is a chance that other developers may get confused with this variable declaration, we can
[01:04] try to provide some single line commands explaining about the purpose of this variable.
[01:09] So here I'm going to mention the single line comment just after the Java statement for the same, I'm
[01:15] going to mention //, followed by I will try to type whatever I want.
[01:20] So here I'll type saying that Represent the age of the customer.
[01:26] So you can see here whatever I have defined with the help of single line command, it is grayed out
[01:33] by my internal age as well.
[01:35] This is because whatever we have defined with the help of single line Java comment is going to be completely
[01:41] ignored by the Java compiler.
[01:43] I can also prove you that let me try to save this and do a build.
[01:47] To do the build, I'm going to select this build project.
[01:51] Once the build is completed, I can go to the output folder and open the compiled class available inside
[01:58] this section five project folder.
[02:00] If I try to open these, you can see this is a .class file
[02:03] and this is the source code built by my intelliJ based upon the byte code present inside this
[02:09] .class file.
[02:10] Do you see anywhere the single line comment that we have written?
[02:13] No.
[02:14] This is because my Java compiler completely always ignores whatever comments that I'm going to write
[02:21] inside the source code.
[02:22] I hope you are convinced with this demo.
[02:24] Now let me try to create one more variable.
[02:27] This time I'm going to create a static variable of type final and the data type of this is int.
[02:34] Since the variable is final, I need to use the snake case.
[02:38] That's why I'm mentioning Max in capital letters followed by underscore followed by retry followed by
[02:45] underscore attempts.
[02:47] To this variable I'm going to assign a int value, which is three.
[02:50] Like we discussed before, if we just define this variable like this, it may not provide complete details
[02:56] to other developers to provide some context around this variable here
[03:00] also, I can use single line comment.
[03:02] This time I'm going to mention the single line comment just above the variable declaration.
[03:07] So I'm going to mention // post that I'm going to mention maximum number of login retry
[03:16] attempts allowed.
[03:18] So this is going to provide some context to the other developers to better understand my Java code.
[03:23] This way we can create any number of variables.
[03:27] As of now, we have created the single line commands for the class level Java fields that we have created.
[03:32] Let me try to create few variables inside my method as well.
[03:36] And when we define the variables inside a method and try to define the single line comment for those
[03:42] variables, the process and syntax is always going to be the same.
[03:47] For example, here I'm going to create a two char variables like char y is equal to 'Y' in the capital letters
[03:56] followed by char n is equal to capital 'N'.
[04:00] I'm trying to store here.
[04:02] So for these variables I want to provide more details with the help of single line commands.
[04:07] So what I can do is on top of these variables, I can mention comments saying that y indicates yes,
[04:15] and similarly I can copy the same comment and mention just above the N char as well.
[04:20] So here I'm going to replace n represents no.
[04:24] So this will provide more details about these char variables to the other developers who are trying to
[04:30] read my Java code, the same syntax we need to use wherever we want to define a single line command.
[04:37] For example, I want to explain about the purpose of this main() method.
[04:41] I can simply mention single line comment on top of this method, saying that main() method is used to
[04:47] start the Java program.
[04:50] So the process is not going to change regardless of where you are trying to define the single line comment.
[04:56] So this is one of the advantages that we have with the single line comment
[05:00] where it is going to help us to improve the readability of the code.
[05:04] But please note that inside real projects, you should only provide the comments to the code only if
[05:10] your code is complex or if you want to provide some additional information to the other developers.
[05:16] Only in such scenarios, we need to provide the comments or single line comments
[05:20] Inside Java, there is no mandatory that you need to provide the single line command for all variables,
[05:26] for all the methods that you are going to create. That is truly unnecessary and it is going to make your
[05:32] code also clumsy.
[05:33] Please always use the comments are single line comments wherever they are needed.
[05:38] Moving on to the second advantage of single line comment is, with the help of single line comments
[05:44] sometimes we can temporarily comment the code or disable the code.
[05:48] I can also show you a demo here.
[05:50] So here, after the main() method, I'm going to create a new method and the method is going to be public
[05:57] static void sum().
[05:59] And to this method I'm going to accept two int variables like into num1, int num2.
[06:07] So these are the two variables I'm trying to accept.
[06:10] And inside these method I'm going to perform the addition of those two variables.
[06:16] So let me try to perform the addition for the same
[06:19] I'm trying to write a logic here which is int num3 is equal to into num1 + into num2.
[06:26] And once the calculation is completed, I'm going to print the num3 value, which is the total
[06:33] value after performing the addition of two given input numbers.
[06:36] Now this method I want to invoke from my main() method.
[06:40] So let me try to invoke from my main() method by using the method name and passing the integer details
[06:46] like 12, 8.
[06:47] So if I try to execute this code, you can expect the output 20.
[06:51] So you can see here inside the console I'm able to see that 20 output.
[06:55] For example, for some reason you want to temporarily not invoke this method.
[07:00] In such scenarios, you can simply mention // just before this method invocation.
[07:06] And with that, the method sum() is never is going to be invoked.
[07:11] I can also show you that by running the program this time, you will not see any output inside the console
[07:18] because this method is never invoked.
[07:21] Just like how we are trying to comment the entire method invocation.
[07:25] Very similarly, we can also try to comment a particular statement.
[07:30] Think like I don't want to print the num3 value.
[07:33] In such scenarios, I can simply mention // just before my System.out.println().
[07:40] So with this code, since I have removed the two forward slashes just before the sum() method, my sum()
[07:45] method is going to be invoked, but the System.out.println() is not going to be printed.
[07:50] So I can keep a breakpoint here to show you that the sum() method is going to be invoked.
[07:55] So let me execute this in a debug mode.
[07:57] You can see the breakpoint stopped here as soon as I release this.
[08:01] If you go to the console this statement is never executed because this statement is commented out.
[08:07] That means my Java compiler is going to ignore it during the compilation process and in the execution
[08:13] process as well.
[08:14] This way, if you want to temporarily comment out a single Java statement or a method invocation, you
[08:20] can always use the single line comment with this demo.
[08:24] I'm assuming you are clear about the single line comment inside Java class.
[08:28] My humble request is to try out the single line commands with various combinations inside your Java
[08:34] code as well, so that you will be familiar with this syntax.
[08:37] Before I try to close this lecture, let me show you the generated compiled class inside the out folder.
[08:45] So let me open this dot class file.
[08:47] You can see nowhere I'm able to see the comments that we have mentioned.
[08:52] This is because my Java compiler is not going to construct them to generate the bytecode, since my
[08:58] intelliJ is trying to generate the source code from the bytecode present inside this .class file,
[09:04] we are nowhere seeing the single line comments that we have mentioned inside the source code file.
[09:10] So this confirms always
[09:12] java compiler is going to ignore your comments inside your Java program.
[09:17] I hope this all clear to you.
[09:18] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

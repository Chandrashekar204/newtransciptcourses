# 3.5 — How Java became a platform independent language - Part 2

> Section 3: What happens behind the scenes when a Java program executes

[00:00] Inside the previous lecture, we talked on how Java became a platform independent language.
[00:06] Now let me show you a different perspective about the life cycle of a Java program.
[00:12] Like you can see
[00:12] first there'll be a source code with the name MyClass.java.
[00:16] Whenever we want to compile, we'll feed that to the compiler, and the compiler will validate for all
[00:21] the syntax errors.
[00:22] If everything looks good, I'm going to get a MyClass.class which is going to have bytecode.
[00:29] So whatever process that we are doing to convert our source code to the bytecode, we call it as a compilation
[00:37] stage.
[00:37] So inside this compilation stage we are converting our Java source code into and semi binary format
[00:45] which is known as bytecode.
[00:47] This bytecode we are going to feed to the JVM and the JVM is going to be the platform dependent.
[00:55] So if I'm using windows operating system, then I need to feed to my windows specific JVM.
[01:01] Similarly for mac and Linux or any other operating system, I need to feed my bytecode to the operating
[01:08] system specific JVM.
[01:09] So the JVM is going to convert the bytecode into the native executable code that can be understand by
[01:17] my operating system or by my CPU processor, and eventually I'll get my Java program output.
[01:23] So whatever process is happening with the help of JVM, we call it as interpretation stage.
[01:29] Because inside this interpretation stage, my JVM is trying to convert a semi binary format which is
[01:36] byte code, into the native executable code.
[01:40] That's why if anyone asks you is Java is a compiled language or interpreted language, you should always
[01:47] say Java is a both compiled and interpreted language.
[01:51] Why
[01:51] Java followed this approach to achieve the platform independence by utilizing a JVM that is specific
[01:59] to each platform.
[02:01] I want to be very, very clear here because in interviews people can try to confuse you.
[02:07] They'll ask you if Java is a platform independent,
[02:10] you'll answer yes immediately
[02:12] they are going to ask you what is making Java as a platform independent language.
[02:17] Obviously, since you listened all this discussion, you're going to tell them JVM.
[02:21] And the next question that you can expect here is, is JVM is a platform independent or dependent?
[02:27] So the answer that you need to give here is platform dependent.
[02:31] The interviewer can also deep dive here by asking why we should have different, different jvms for different
[02:36] different operating systems.
[02:38] The answer is very obvious, since each operating system has their own style of executing the native
[02:44] instructions.
[02:45] We need to have separate, separate Jvms to to convert a given bytecode into the operating system specific
[02:51] instructions.
[02:52] I hope you are clear for your reference
[02:54] I have mentioned all the points that we have discussed like what happens in compilation stage.
[02:59] So inside compilation stage, all your source code is going to transform into a basic binary instructions,
[03:05] or semi binary instructions.
[03:07] And this format we call it as a bytecode.
[03:10] So this is going to be something different from other languages like C or C++ .
[03:15] So inside the C or C++ languages your source code is directly going to be converted into a native
[03:22] instructions or native executable code.
[03:25] But in the case of Java, we are going to first convert our source code into an compiled format, which
[03:33] is known as bytecode.
[03:34] This bytecode will feed it to the JVM inside JVM
[03:39] since your JVM, which is a Java Virtual Machine, is going to read your bytecode instructions and try
[03:45] to interpret them as an native executable code, we call this stage as interpretation stage.
[03:52] And here you may have a question,
[03:53] if my JVM try to convert each of the bytecode present inside the .class file to a native executable
[04:02] code or a machine specific code, don't you think it is a performance issue?
[04:07] Because my JVM has to continuously convert or try to interpret the bytecode into a machine code?
[04:12] Whenever I try to run a program which has thousands of lines, I agree with you and it is a great question
[04:18] also.
[04:19] But let me give assurance to you there won't be any performance issues with Java.
[04:23] The reason is behind the scenes,
[04:25] the Java is going to optimize the performance by using dynamic compilation or JIT compilation.
[04:33] So what is JIT, Just In Time compilation.
[04:36] So think like you have given a bytecode to your JVM which has thousands of lines.
[04:41] The JVM is not going to convert all your thousand lines of bytecode into the machine code immediately.
[04:49] It is only going to do the conversion on the fly based upon the particular method that you are trying
[04:55] to invoke.
[04:56] Think like I'm trying to execute only the addition logic
[04:59] inside my Java program, but not the subtraction, multiplication and division.
[05:04] In such scenario, my JIT compilation or dynamic compilation, which is a process inside my JVM, is
[05:10] going to interpret only the logic present inside my addition method, but not in the other methods.
[05:16] This way it is going to improve the performance, and at the same time it is also going to recognize,
[05:22] what is the piece of code that is going to be executed very commonly.
[05:27] So such a code, which is going to be executed very frequently inside your Java program, it is going
[05:33] to identify them as a hot spots for all the code present inside these hot spots,
[05:38] it is going to do the conversion from bytecode to the machine code only once.
[05:43] So it is going to cache that and whenever the same common code is being executed one more time in the
[05:49] future, it is not going to do the interpretation one more time.
[05:52] It is simply going to use the already available machine code in the cache.
[05:56] So this way the performance is going to be super, super fast, even though Java is following both compilation
[06:03] and interpretation.
[06:05] I hope this is clear in case if you have still some confusion how this JIT compilation is going to work,
[06:11] don't worry, I am going to give some real time scenarios to understand this JIT compilation.
[06:17] Think like you are asked to read a book of instructions, but these instructions inside this book,
[06:22] they are not in the plain English.
[06:24] So you are supposed to interpret line by line.
[06:28] And in this interpretation process you need to convert that instructions present inside the book into
[06:33] a natively understandable language, which is English.
[06:36] So this is what JVM does whenever it is trying to run a Java program.
[06:41] So bytecode is a format which can't be understand by operating system.
[06:44] That's why it is going to convert that bytecode into operating specific native code.
[06:49] So in the same scenario, if you are trying to read the book many times as a human, you can start remembering
[06:56] what to do without having to interpret the instructions every time.
[06:59] So this is what the JIT compiler also follow.
[07:03] It is going to compile the Java bytecode into machine code only once, and if the same piece of instructions
[07:09] are bytecode is trying to be executed more number of times, the JVM is not going to convert again and
[07:16] again, it is simply going to follow the JIT compiler strategy.
[07:21] This way the execution is going to be faster.
[07:24] Let me tell you one more scenario to be more clear for you.
[07:27] Think like you are a child and your mother gives a list of tasks that you have to do inside your home.
[07:33] You can read all the list, each one by one, and you can do one at a time.
[07:38] But if you are a smart person, what you're going to do is you're going to group all the tasks together
[07:43] so that you can start doing them more efficiently.
[07:46] For example, all the tasks related to the kitchen, going to the kitchen, cleaning the kitchen, cleaning
[07:52] the dishes, setting the table, putting away the dishes.
[07:55] So all such common tasks which are specific to kitchen, you're going to group them and you're going
[08:01] to execute them all at once. So that you can avoid going to the kitchen everytime.
[08:07] If you try to perform these tasks randomly and independently.
[08:11] So the jit compiler also follows a very similar strategy.
[08:15] It tries to group together the Java bytecode that is used most often, and compiles them into machine
[08:21] code.
[08:22] Post that it is also going to cache that machine code so that it can be executed by the CPUs or your
[08:28] local systems very efficiently.
[08:31] So if someone asks you inside the interviews, what makes Java program to run very fast
[08:36] though we are using compilation and interpretation.
[08:39] The answer is very simple.
[08:41] JIT compilation is one of the reason why Java programs run so fast.
[08:46] I hope this is all clear to you.
[08:48] In the next lecture I'm going to do some mock interview.
[08:51] I'm going to ask a few questions to you and you need to provide the answers.
[08:55] If the answers are not correct, then there is a punishment for you.
[08:58] The punishment is to rewatch this lecture and last lecture one more time.
[09:04] I hope you are with me on this challenge.
[09:06] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

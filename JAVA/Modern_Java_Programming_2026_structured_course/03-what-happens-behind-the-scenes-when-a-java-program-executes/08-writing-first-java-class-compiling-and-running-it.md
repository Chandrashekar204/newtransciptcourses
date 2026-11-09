# 3.8 — Writing first Java class, compiling & running it

> Section 3: What happens behind the scenes when a Java program executes

[00:00] Inside this lecture, we're going to write our first Java program.
[00:05] And the same we are going to compile and execute it.
[00:08] To get started, first I need to create a file with a .java extension.
[00:13] For the same I have created a Java folder inside my desktop.
[00:16] From my terminal I'm going to navigate to the same folder.
[00:20] The folder location is User/easybytes/Desktop and inside the desktop I have a folder with the name Java,
[00:27] so let me navigate to that folder.
[00:30] If I try to run the pwd command, you will get the output,
[00:34] what is the present working directory where my terminal is running?
[00:39] So this is the directory where right now my terminal is running.
[00:42] So please make sure you also opened your operating system specific terminal.
[00:48] Inside windows you can open the windows shell or command prompt.
[00:52] Once you open the terminal inside a folder called Java, we need to create a Java class for the same,
[00:58] let me first clear my terminal.
[01:01] The command that I'm going to run here is touch,
[01:04] what is the file name?
[01:05] The file name is going to be HelloWorld.java.
[01:10] So please make sure you are following the Pascal case style.
[01:14] So with this touch command a file will be created inside my Java folder.
[01:19] So this is a command that I need to execute inside my Mac operating system.
[01:24] Whereas inside windows operating system you can go back directly to the Java folder and right click
[01:30] and create a new text file and post that, rename that text file to Hello World and remove the .text
[01:36] extension and replace it with the java extension.
[01:40] So you can see right now I have a file with the name HelloWorld.java.
[01:45] This is empty.
[01:46] So let me open this with a text editor.
[01:49] So I'm using Sublime Text Editor inside this file,
[01:53] first we need to type public, after public I need to type the space followed by class, followed by what
[02:01] is the class name?
[02:02] The class name is going to be same as our file name.
[02:06] HelloWorld.
[02:07] If you try to use a different class name, you're going to get an error.
[02:11] I can show you that in the demo also.
[02:13] So to show you the demo I can say HelloWorld1 as my name post that I will give opening brace and
[02:20] curly brace. Inside my HelloWorld class,
[02:23] I need to create a method which is public static void main() and to this main() method I'm going to accept
[02:32] the input parameter which is string two square brackets followed by what is the variable name?
[02:39] The variable name is going to be args.
[02:41] Now for my method, I need to mention what is the opening brace and curly brace. Inside my method, I'm
[02:47] going to write a logic which is System.out.println().
[02:54] And to this method I'm going to pass a text which is Hello World and I need to terminate this
[03:01] Java statement.
[03:03] Here what I'm going to do is I'm going to make multiple mistakes intentionally.
[03:06] First, I'll try to remove the semicolon, which is present at the end of System.out.println() and post
[03:12] that instead of main() method, I will change this main() method name to that test().
[03:17] With this I should get a multiple compilation errors.
[03:20] So let me save this file.
[03:22] As a first step, we need to do the compilation of our Java file.
[03:25] So whenever we want to do the compilation of the Java file, the command that we need to use is
[03:32] javac space.
[03:33] And what is our file name where you have written your Java code.
[03:37] The file name obviously will be HelloWorld.java.
[03:41] So if I try to execute this command you can see I'm getting an compilation error.
[03:47] So let me try to resolve that compilation error.
[03:50] The compilation error that I'm getting here is, the semicolon is expected after this statement.
[03:56] So let me try to add the semicolon.
[03:58] So I'm trying to add the semicolon here.
[04:00] And saving the file.
[04:01] This time I'll try to compile the program again.
[04:04] And this time you can see we are getting a different error which is HelloWorld1
[04:10] is a class name and it should be declared in a file name
[04:14] HelloWorld1.java.
[04:15] So the file name and the class name are mismatching,
[04:19] that's why we are getting this compilation error.
[04:21] So let me fix this compilation error
[04:23] also we know how to resolve this.
[04:25] To resolve this we just have to simply remove this one
[04:28] and with this the compilation error should get resolved.
[04:31] So let me try to run the same javac command this time
[04:35] you can see I got a successful output.
[04:37] There are no compilation issues.
[04:39] So here you may have a question,
[04:41] we have defined the method name as test(), but JVM expects the main() method.
[04:45] So why it is not throwing an error.
[04:47] So the answer is very simple.
[04:49] Right now the Java compiler will only look for the syntax errors, and this method does not have any
[04:54] syntax errors.
[04:55] Any method name is fine according to the Java compiler. but when I try to
[05:00] execute my java program
[05:01] my JVM is going to look for the starting point at that time
[05:05] hopefully we can see the error.
[05:07] So now my compilation is successful.
[05:09] I have used this javac command.
[05:11] So this javac command is present inside the bin folder of our Java installation folder.
[05:18] So inside this bin you can see there is a javac command which is going to use for the compilation.
[05:24] Now if I go and check the Java folder you can see there is a .class file generated with the same
[05:29] name which is HelloWorld.
[05:31] And the extension name is going to be .class.
[05:33] And the content of this .class file is going to be the bytecode.
[05:37] So let me try to open this bytecode and see whether we can make any sense out of it.
[05:42] So from my text editor I'm going to open the HelloWorld.class.
[05:47] And you can see this all bytecode which we cannot understand anything from it only JVM can understand.
[05:54] Let me close this file.
[05:55] So whatever .class file that is generated, the same .class file can be given to your friend
[06:02] who is using different operating system.
[06:04] This way the Java code and compilation can be done only once, and it can be run on any platform with
[06:11] the help of platform dependent JVM.
[06:15] So now the compilation is successful.
[06:16] I want to execute my Java program.
[06:18] So the command that we need to use is java.
[06:22] This time they should not be C, javac we should only use for compilation.
[06:26] For execution we should use only the java space
[06:30] and what is the java class name?
[06:32] The Java class name that we want to execute here is HelloWorld.
[06:36] We don't have to give any extension.
[06:38] Simply give your class name.
[06:40] So if I try to execute this you can see my JVM is throwing an error.
[06:45] I don't know where to start.
[06:46] I looked for the main() method and I did not find any main() method inside the class
[06:52] HelloWorld.
[06:52] Please define the main() method as public static void main( String args).
[06:57] So these are standard that we need to follow, which indicates the starting point to my JVM.
[07:04] So let's try to fix the problem.
[07:06] So here I'm going to rename this test() method name to main().
[07:10] So now I'm saving the file.
[07:11] This time I'm going to run the command which is java HelloWorld.
[07:15] And you're going to see a surprise here.
[07:17] So if I try to run the command you can see I'm still seeing the same error
[07:21] why?
[07:21] Because after making the code changes inside my source file, I did not perform any recompilation.
[07:28] So whatever .class file right now is present inside my folder.
[07:32] It has a old method name which is test().
[07:35] So that's why whenever we make any code changes inside our Java source code, we need to make sure we
[07:40] are recompiling post that only.
[07:42] We need to run the Java program to see the latest changes.
[07:46] Let me do the compilation again.
[07:48] Before that, let me clean my terminal.
[07:50] The command that I want to run is javac
[07:53] HelloWorld.java and this is going to replace the existing .class file.
[07:59] Now the compilation is successful.
[08:01] I'm going to run the command which is java HelloWorld.
[08:05] You can expect a successful output this time.
[08:08] And you can see we are getting an HelloWorld output.
[08:12] Hooray!
[08:12] We successfully executed our first Java class by following all the steps that we have discussed, like
[08:20] compilation and execution.
[08:23] I hope this demo clarified most of your
[08:26] any pending questions for your reference, I have mentioned all these steps inside the slide as well.
[08:31] Let me quickly show you the same.
[08:33] So this is the sample first Java class that we have written.
[08:36] For your reference, I have highlighted each word and what is the purpose of each word inside this Java
[08:42] class.
[08:42] So all these details you can identify inside the slides we already discussed.
[08:48] I'm just trying to mention for your future reference inside this slide.
[08:51] So once you have defined this Java class we need to make sure we are compiling the Java class with that
[08:58] javac command and post that we need to feed the bytecode to the JVM with the help of Java command.
[09:05] So I have mentioned all the steps here.
[09:07] A sample screenshot also for your reference.
[09:09] I hope you are super happy with the progress that we are making.
[09:13] I'm also feeling very happy right now because we're able to make some progress inside this course,
[09:18] and as we are making progress inside the course, we are learning lot many new concepts inside the Java
[09:24] programming language.
[09:26] We are going to discuss a lot in the coming sections as well.
[09:29] More exciting topics on the way.
[09:31] Brace yourself.
[09:32] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

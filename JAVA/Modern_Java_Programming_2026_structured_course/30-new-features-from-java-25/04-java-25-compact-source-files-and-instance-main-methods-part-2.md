# 30.4 — [JAVA 25] Compact Source Files and Instance Main Methods - Part 2

> Section 30: New features from Java 25

[00:00] Let's see what is going to happen if we try to create another main method inside this compact source
[00:07] file.
[00:07] So what I'll do is I'll try to create traditional main method by typing public static void main.
[00:16] And this main method it is going to accept array of string as an input.
[00:20] Inside this main method I can write System.out.println or I or dot println.
[00:25] Let me go with the old style of System.out.println.
[00:29] If you closely observe our compact source file, it has two different main methods.
[00:35] One is the traditional main method and the other one is the instance main method.
[00:39] In this kind of setup, the JVM, it is going to give the preference to the static main method.
[00:45] If I try to execute this program, I'm going to get the output inside this method.
[00:50] Maybe I can change this to hi world.
[00:54] Let me save this.
[00:55] Do the build.
[00:55] Once the build is completed, I'm going to execute this program.
[00:59] As you can see, I'm getting the High World program.
[01:02] I hope you are getting this.
[01:04] This can be a very good interview question.
[01:06] That's why I want to highlight about this scenario.
[01:09] The next important point that I want to highlight here is when you are defining a main method inside
[01:15] a compact source file, it don't have to be either completely this method or this method.
[01:22] You can also define any of these main method variations instead of simply mentioning void method.
[01:29] If you simply mention public void method without any input parameters, still the compiler is going
[01:35] to accept.
[01:35] Let's try to define these variations.
[01:38] So instead of void main.
[01:39] This time I'll just simply mention public.
[01:42] So let me get rid of these old main method.
[01:45] And I'll try to execute this program.
[01:47] Even if I try to mention public void main.
[01:50] I'm going to get the Hello World output this time.
[01:53] Let me try to mention only static instead of public.
[01:57] So if I try to execute this program this time.
[02:00] Also, I'm getting the output.
[02:01] As a next step.
[02:02] I'll try to define both the public and static with this combination.
[02:07] Also, we're going to get the expected output.
[02:10] If you mention array of string as an input, then it is going to become a normal traditional main method.
[02:15] I hope you are seeing how the Java team is giving the flexibility to the developers, and what are the
[02:21] different ways of defining a main method.
[02:24] You can completely go with the compact instance main method by simply typing void main, or you can
[02:31] mention a combination of public void main or static void main args.
[02:36] Public static void main along with the array of string as an input parameters.
[02:41] We already saw with the help of these Iwo class, the console interaction for the beginners or for the
[02:47] experienced developers, it became super easy.
[02:50] Instead of typing System.out.println, we can simply mention iwo dot println.
[02:56] Just like how we have println method.
[02:58] We also have a method with the name read ln.
[03:03] So with this method we can accept input from the end user.
[03:08] For the beginners this is going to be super helpful.
[03:10] We know inside Java to accept an input from the end user.
[03:14] We have to do a lot of setup like creating an object of scanner class.
[03:19] Along with the scanner class, we need to attach the input source like system dot in.
[03:24] So to set up all this for a beginner, it may look very cumbersome and even for the experienced developers.
[03:30] Also, if they want to quickly prototype some logic, they don't have to go that lengthy approach.
[03:35] Instead, they can rely on these method read ln inside the IO class.
[03:40] So here I can type a statement saying that enter your name.
[03:45] So the output from the read ln method I can catch with the variable name as var name.
[03:52] This name whatever I'm receiving from the read ln method, I can try to print in the next line by just
[03:59] mentioning hello colon bless name.
[04:04] And with this, if I try to execute this program inside the console, the name will be asked.
[04:09] Let me type mother and as soon as I press enter I'm going to get an output.
[04:14] Hello?
[04:15] Colon.
[04:15] Mother.
[04:15] So do you see how simple it is, even for the beginners or for the experienced developers to interact
[04:21] with the console?
[04:22] If you want to print something onto the console, or if you want to read something from the console,
[04:26] the developers can happily use the methods available inside the I o.
[04:30] The methods are read ln and println, just like println.
[04:35] We also have print method and a println method which is not going to accept any input parameter.
[04:41] So based upon your requirements, feel free to use any of these methods.
[04:45] With this introduction to the Compact Source and Instance method, you may have a burning question which
[04:50] is modern?
[04:51] Java is a object oriented programming language where every logic has to be written inside a Java class.
[04:58] But here we're not writing any Java class.
[05:01] Then how come this instance method is getting executed?
[05:04] So this can be your question.
[05:06] So let's try to answer the same.
[05:07] So when you define a compact source file along with an instance method behind the scenes, the compiler
[05:14] during the compilation process, it is going to create an implicit class.
[05:19] That means based upon the file name, the compiler is going to take care of creating a class and a default
[05:25] constructor, which are mandatory things to execute an instance method.
[05:29] All of them will be created behind the scenes and will be taken care by the compiler.
[05:33] For example, if I compile this code and go to the out folder so there is a file with the name hello
[05:40] world.
[05:40] This is a compiled file.
[05:42] If I try to open the same the IntelliJ, it is going to decompile the dot class file and show me the
[05:47] source code.
[05:48] So here behind the scenes the compiler.
[05:50] It has created an implicit final class with the name Hello World.
[05:55] And inside this hello world we have a static main method and few of the decompilers.
[06:01] They will not show you the default constructor.
[06:03] That's why I'm not able to see.
[06:05] But behind the scenes, as I said, the compiler it is going to create the default constructor as well.
[06:11] So when we try to execute a main method inside the compact source file behind the scenes, the object
[06:16] of this class will be created, and this instance method will be invoked by the Java itself.
[06:22] Whatever final implicit class that is being created by the Java behind the scenes.
[06:27] So this will be always placed in an unnamed package or in that default package.
[06:33] That's why when we create a compact source file, the hello world file is created under the src, but
[06:39] not inside these compact subpackage.
[06:42] The compact source file should always have an instance main method.
[06:46] For example, if I delete this main method and try to create another method like void hello world and
[06:54] inside this if I try to have System.out.println.
[06:57] You'll be able to see I'm getting a compilation error saying that compact source file contains no main
[07:03] method.
[07:04] That means when you are defining a compact to source file, it is mandatory to have a main method either
[07:12] in the form of instance method or in the form of static main method.
[07:16] This should give a confirmation to you by using compact source file.
[07:20] We can't write any normal business logic.
[07:23] It should always have a main method above this instance.
[07:27] Main method we can define fields are.
[07:30] Instance method.
[07:31] For example, I can define a field saying that string greeting is equal to hello world and the same.
[07:36] I can try to pass as an input to the IO dot println.
[07:42] So if I try to execute this program, I'm going to get the expected output.
[07:46] Like.
[07:47] First I'll type my name.
[07:49] Both Hello and Statement and hello world statement.
[07:51] Were able to see if you try to see the compiled version of this class, this time Inside the implicit
[07:57] class there is a Java field with the name greeting.
[08:00] So whatever you are defining outside of your main method.
[08:05] So those will become the members of the implicit class.
[08:09] The same we are seeing here.
[08:11] So this time let me create an instance method.
[08:14] For example I'm creating an instance method with the name greeting and this instance method.
[08:20] It is not going to accept anything as an input, but it is going to return a string as an output.
[08:26] The string value is hello world.
[08:28] The same I can try to invoke from the main method instead of this greeting.
[08:32] This time I'll try to invoke the greeting instance method.
[08:36] Let me compile this and execute this class.
[08:40] I'm going to type the name as method and press enter, and inside the console we got the expected output.
[08:46] If you go and check the Decompiled class, this time inside the implicit class, along with the field,
[08:52] we also have instance method with the name greeting.
[08:55] So whatever you define outside of the instance main method, they all will be the members of the implicit
[09:01] class.
[09:01] So you can define static fields static methods, instance methods, instance fields.
[09:08] It's up to you what you want to define.
[09:10] Let me show you another beautiful developer friendly feature introduced as part of the compact source
[09:16] files inside the main method.
[09:18] After this simple logic, I'm going to paste few lines of code.
[09:21] As you can see here, I am writing some list related logic where I have defined some names inside list
[09:29] with the variable name as authors.
[09:31] The same authors details.
[09:33] I'm trying to iterate with the help of this for loop and print them one by one.
[09:38] So along with the name, I'm also printing their length.
[09:41] So if you see the beauty here, I'm using a list class which is present in the package Java dot util.
[09:48] We know by default inside Java Java dot lang package is going to be imported, but these java.util.
[09:55] It is not going to be imported by default, but still inside my compact source file.
[10:00] This code is working, though I have not mentioned any import statement around this list.
[10:05] On top of the file.
[10:06] This is because, as I was saying in the previous lectures, inside the compact source files, by default
[10:13] the Java dot base module is going to be imported by the compiler.
[10:18] So why this has been provided only to the compact source files?
[10:21] Because to make the Java developer friendly many times, either beginners or the experienced developers,
[10:28] they may want to write some good amount of code around the collections or by using the class present
[10:34] inside that Java dot base.
[10:35] So for those classes, they don't have to manually import the classes.
[10:40] Instead, they can keep focusing on the business logic and behind the scenes, the Java is going to
[10:45] take care of importing all the required classes by importing the Java dot base module.
[10:50] So let me save these, do the build and if I go to the Decompiled the class.
[10:56] So here you'll be able to see Java dot to dot list.
[10:59] Import statement is present, though I have not mentioned inside the source file how this is happening
[11:05] behind the scenes.
[11:06] By default, the compiler is importing the module Java dot base and inside this module.
[11:11] Since we are only using the list, that's why we are able to see only a single import statement here.
[11:18] So let me execute this program.
[11:20] First.
[11:20] It is going to ask me my name.
[11:22] I'm going to type the same and press enter.
[11:24] And getting my done in all the places.
[11:26] This is because inside this for loop, instead of this name I should mention author and author dot length.
[11:33] Let me save this.
[11:34] Do the build and execute this program.
[11:37] Let me type my name and we got expected output.
[11:41] Whatever we discuss around the compact source files and instance main method everything.
[11:46] I have mentioned them in these slides for your reference, so feel free to refer the same to know more
[11:52] details around this feature.

----------------------------------------

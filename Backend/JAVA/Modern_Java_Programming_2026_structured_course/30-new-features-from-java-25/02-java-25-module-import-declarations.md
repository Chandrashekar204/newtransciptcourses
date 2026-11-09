# 30.2 — [JAVA 25] Module Import Declarations

> Section 30: New features from Java 25

[00:00] As part of Java 25 release.
[00:03] In new feature with the name module import declarations is released for the developers.
[00:09] According to me, this is the simplest feature or enhancement introduced in Java 25.
[00:15] It is very easy to understand and implement as well, so let's try to understand more details about
[00:21] this feature.
[00:22] We know inside Java by default a package with the name Java dot lang.
[00:28] It is going to be imported in each and every Java class that we write.
[00:33] That's why when we write code to display a content onto the console by using System.out.println, we're
[00:40] not going to import either system class or println method, because internally the Java.lang package
[00:47] is imported automatically.
[00:49] But as Java language started evolving from Java one version to Java 25, more and more commonly used
[00:56] classes are introduced.
[00:58] For example, if you want to write some collection related logic by using least or set or map.
[01:05] Similarly, if you want to write some code to accept input from the end user by using scanner, or if
[01:11] you want to write code which is going to interact with the files.
[01:15] In all these scenarios, we are forced to import the respective packages because these commonly used
[01:21] files are not present in the default Java.lang package.
[01:24] Instead, they are present in Java.util package java.io package.
[01:29] So even to write a simple Java program, the beginners or the experienced developers, they may end
[01:36] up writing lot of import statements in their source code.
[01:41] Of course, there is nothing wrong with this.
[01:43] All these days we are doing this very happily.
[01:45] There are no problem.
[01:46] But with these new feature module import declarations, what Java team they are trying to provide to
[01:50] developers is convenience.
[01:52] Instead of importing all the respective packages or classes manually one by one, what as a developer
[01:59] we can do is we can import the entire module itself.
[02:04] We know inside Java the entire classes.
[02:07] They are organized into modules.
[02:09] So as part of Java nine, a new concept with the name modules is introduced.
[02:14] Each of these modules, they are going to focus on a specific area.
[02:18] For example there is a module with the name Java Base.
[02:21] Inside this module, all the base packages and classes are being maintained.
[02:27] Instead of importing all these packages manually one by one, the developer can simply mention a single
[02:34] import statement saying that import module Java dot base.
[02:38] Similarly another modules, they can also be imported.
[02:41] The syntax is import module.
[02:44] So by using this module keyword, the JVM is going to differentiate whether the import statement is
[02:50] related to a module or related to a package.
[02:53] I hope you got some good introduction about these feature.
[02:57] Let's see a demo followed by.
[02:59] We can discuss some special scenarios or scenarios inside my Java project, I have created a package
[03:07] with the name Java 25.
[03:10] Inside this package, I'm going to create another sub package with the name module import.
[03:17] Inside this package I'm going to create a new Java class with the name import module demo.
[03:26] Inside this new class I'm going to paste a main method along with some logic.
[03:31] So first let's try to understand what logic I have inside this main method.
[03:35] So first, by using the scanner logic, I'm trying to accept some names from the end user.
[03:40] Once the end user is done providing the names, the user can type exit to finish the process unless
[03:46] the given input is not matching with the exit, the names entered by the end user will be saved into
[03:53] this list with the name names.
[03:54] Once the names list is prepared and the end user type to exit, then the next logic is going to be executed.
[04:01] So here we are going to sort the names by using collections dot sort.
[04:05] As part of the next logic, we're going to create a file with the name names dot text.
[04:10] And into this file we are going to write all the sorted names one by one.
[04:14] Once a saving of the names into the file is completed, we are going to read the same file and display
[04:21] the data present inside the file line by line, with the help of the System.out.println.
[04:27] At last we are going to close the scanner.
[04:29] So this is a simple logic that I have inside this class.
[04:32] Now let's move on to our discussion of importing modules.
[04:36] If you see this is a very simple Java class for this simple Java class, to make it work, we may need
[04:42] to import a lot of statements from the package Java and Java dot util as well.
[04:48] Here this asterisk statement is added by the IntelliJ automatically.
[04:52] This is due to a setting inside IntelliJ.
[04:55] Let me show you the same.
[04:56] If you go to the settings of IntelliJ and type import in the search results, you can go to this code
[05:03] style and select the Java and click on these imports inside this section if you can scroll down, there
[05:09] is a default setting inside IntelliJ with the name class count to use import with asterisk.
[05:15] If I change this 5 to 50, the IntelliJ is going to replace the import statements with an asterisk symbol
[05:23] only if the import statements are equal or more than 50 from the same package.
[05:28] So let me apply and click okay.
[05:30] Now if I try to optimize the imports this time the asterisk symbol is gone.
[05:36] And instead we are seeing the individual import statements.
[05:40] And this is how your source file is going to look like.
[05:43] If you're not using any IDE like IntelliJ, if your IDE is not optimizing the imports like IntelliJ,
[05:50] then as a developer, your job is going to be very tough.
[05:53] Maintaining all these import statements and looking at them every time inside the source file also is
[05:58] very annoying.
[05:59] With the help of Java 25, what we can do is we can import the entire module.
[06:04] All these are the most commonly used files and these files are present inside a module with the name
[06:09] Java dot base.
[06:10] If you can open any of the file like Bufferedreader, you should be able to see that these class is
[06:16] present in a module with the name Java dot base.
[06:18] So let me close the same.
[06:20] Since all these import statements are from a module Java dot base, we can now replace all these import
[06:25] statement with a single statement.
[06:27] Let me type import module Java dot base.
[06:34] So with this now I can get rid of all the remaining import statements.
[06:39] And my code still is going to work without any issues.
[06:42] To use this feature, please make sure you have downloaded the JDK 25 under configure the same for your
[06:48] project as well.
[06:49] Inside my IntelliJ for this project, I have configured the JDK 25.
[06:53] As you can see under this project SDK, I'm using JDK 25.
[06:58] If you don't have JDK 25, you can click on this arrow button and go to the down.
[07:03] And here you have an option of download JDK.
[07:06] And please make sure you are selecting version 25 and select any of the vendor available.
[07:11] So you can select Amazon or Azure or Oracle based upon your requirements.
[07:17] So once the download is completed you need to select the corresponding JDK here.
[07:21] And next you need to go to the modules.
[07:24] And here under the sources you need to select the supported version as 25 hyphen compact source files
[07:31] comma module imports.
[07:32] If you're not seeing this option, then that means you are IntelliJ is not updated, so please make
[07:38] sure to update the same to the most recent version.
[07:41] I hope you are clear on how to use these import module statement.
[07:45] Now, before we try to close this lecture, let's try to discuss some special scenarios.
[07:50] When you are importing an entire module inside your Java class, you may end up into some compilation
[07:57] errors.
[07:57] For example, let's consider a scenario where inside a Java file, you have imported both Java dot base
[08:03] and Java dot SQL modules, and inside your business logic you are using the date class, but with this
[08:10] setup the compiler it is going to have some ambiguity because it is clueless whether it has to consider
[08:17] the date class present inside the Java.util, which is a package present inside Java based module,
[08:22] or whether it has to construct the date class present inside the Java dot SQL package.
[08:28] So to resolve this kind of ambiguity compilation errors as a Java developer, what you have to do is
[08:34] after mentioning the module import statements, you need to mention the import statement related to
[08:41] the specific class that you are trying to use.
[08:44] For example, if you are looking to use the date class present inside the Java dot SQL package, then
[08:50] you need to mention the corresponding import statement.
[08:52] And with that, you are going to resolve the ambiguity for the compiler and the compilation issue will
[08:58] get resolved.
[08:59] I hope you are clear.
[08:59] This is very important because when you are importing an entire module, you will end up importing a
[09:06] lot of packages, thousands of classes.
[09:09] And with that, this will be the most common problem that you may face.
[09:13] But with the solution or the tip that we have discussed, you can easily fix the problem.
[09:18] Now let's try to talk about the best standards on how to group the import declarations.
[09:24] So right now with this feature we can write the import modules related to the module.
[09:29] And we can write an import statement related to a package.
[09:33] And we can also write a import statement related to a Java class.
[09:38] So when you have these multiple options to import, there is a good chance that you may end up mixing
[09:44] all these import statement at random places on top of your source file, but instead you can follow
[09:50] a best practice, which is.
[09:52] First, you need to mention all your module imports, because by using the module imports, you're going
[09:58] to provide the least specific details to the compiler.
[10:01] After the module imports, you can mention the package imports, and at last you can mention the single
[10:08] type imports which are most specific imports.
[10:11] So here I have given an example as well.
[10:14] So let's construct there is an employee app class on top of this class.
[10:18] First I make sure that module imports are mentioned.
[10:23] So these module imports are least specific imports because I'm not giving any details to the compiler
[10:30] on which specific package are on which Java class I want to use.
[10:34] So based upon my business logic, the compiler has to figure out after the module import statements
[10:41] I'm going to mention the package imports.
[10:43] So by using these asterisk symbol we are going to import the entire package with the name Java.util.
[10:50] So inside this package, if you have 100 classes, all of them will be imported.
[10:55] After the package imports.
[10:56] You can mention the single type imports where you're going to mention the complete class package name.
[11:04] For example.
[11:04] Here I'm trying to import the list and local date for the same.
[11:08] I have mentioned the package name along with the class name, so please make sure you are following
[11:12] these best practice.
[11:14] So this is going to improve the readability of your source file.
[11:18] Now let me try to clarify a few of the burning questions that you may have.
[11:22] So the very first question that you may have is around the performance impact.
[11:27] You may ask a question here.
[11:29] So modern we are trying to import an entire module.
[11:33] And inside the module we may have thousands of classes.
[11:37] So with these thousands of classes being imported into my Java class, don't you think the size of my
[11:42] Java class is going to be increased?
[11:44] So this can be your question.
[11:46] Let me try to answer the same.
[11:47] Regardless whether you are importing a specific class or an entire package or an entire module, only
[11:55] the classes you actually use in your code are loaded at runtime.
[12:00] The compiler is smart enough to load the classes only you are using inside your business logic.
[12:06] That's why there will be no performance issue with importing an entire module.
[12:12] Next, I want to highlight that Java dot base module is automatically imported on demand in a compact
[12:20] source file.
[12:21] Again, this compact source file is a new feature released in Java 25.
[12:26] We're going to discuss about this in few minutes.
[12:29] At that point of time, I'm going to explain in detail about this point.
[12:32] At last, I want to share a caution.
[12:35] When you have an unnamed module, you can't use the import module statement because in order to use
[12:42] this feature, the module should have a module name.
[12:45] In case if there is an unnamed module, you can't import that by using this import module feature.
[12:52] I hope you're clear with this new feature.
[12:54] Don't try to update all your existing Java classes with this new feature.
[12:59] You can try to adopt this new feature for all the new classes that you are going to create for the existing
[13:04] classes.
[13:05] I don't think you're going to bring any value add by removing the import statements and replacing it
[13:11] with the module import statement.

----------------------------------------

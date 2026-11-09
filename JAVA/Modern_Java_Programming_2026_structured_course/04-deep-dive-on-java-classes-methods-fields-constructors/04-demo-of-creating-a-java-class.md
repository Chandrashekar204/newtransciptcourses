# 4.4 — Demo of creating a Java class

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] In the previous section, we created a sample class with the name HelloWorld, and inside this class
[00:05] we have written a main() method.
[00:07] Now inside this lecture let's try to create few other classes and in the process, let's try to validate
[00:13] all the points that we have discussed in the previous lecture.
[00:16] As of now, this HelloWorld.java class is present inside the project with the name HelloWorld
[00:22] and this is present inside a folder
[00:24] location
[00:25] Documents/Storage/ Workspaces/java/section3/HelloWorld.
[00:29] .
[00:30] We can also go to the folder location by right clicking on the project
[00:34] and you can go to the open in option.
[00:37] And inside the mac I'll get the finder option, because inside the mac finder means this is a folder
[00:44] location.
[00:45] If you are using windows operating system, please select the option which will take you to the folder
[00:51] location where your project is saved.
[00:53] So let me click on this finder.
[00:55] You can see this is our folder location and this Hello world is present inside a folder
[01:00] section3.
[01:01] And this section3 folder is present inside a folder with the name Java.
[01:06] We call this setup as workspace.
[01:09] So there is a terminology or a jargon that you need to be aware here.
[01:13] So wherever we are trying to store our Java projects we call that location as workspace location.
[01:19] So if you join any organization and try to start your work as a Java developer, the very first task
[01:26] that you're going to get is to set up your workspace.
[01:28] Other developers or other team leaders
[01:31] they will ask you to set up workspace with the help of IDE.
[01:35] So workspace means you need to import all the already developed Java projects into your folder location,
[01:42] and the same you need to open inside the IDE like IntelliJ.
[01:46] So we're trying to do the same here.
[01:48] So as of now, Java is my workspace folder location.
[01:51] Inside the Java, I have created a folder with the name section3 and inside the section3 I
[01:57] have a project with the name HelloWorld.
[01:59] Now since we are into the new section, I want to create a new project with the name section4.
[02:05] So whatever concepts we are going to discuss inside this section4, I'm going to develop all of
[02:10] them inside the section4 project itself.
[02:13] So this will give you a flexibility for me to upload all this code into the GitHub repo based upon the
[02:19] section wise, and this will also provide more clarity to you under which section what we have discussed.
[02:25] So inside the GitHub repo I'm going to provide all the details what we have developed, what is the
[02:30] steps that we have followed to develop a particular class.
[02:33] So all those details you can always refer inside the GitHub repo.
[02:37] So now I don't have any project with the name section4 I have to create a new project.
[02:43] So in order to create a new project you can close your existing project which is with the name HelloWorld.
[02:49] .
[02:49] So let me close this
[02:50] now it will ask you whether you want to create a new project or to open an existing project.
[02:56] So since I want to create a new project, I need to click on this new project and the project name that
[03:01] I want to give here is section4.
[03:04] So all the concepts that we are going to discuss inside this section, I'm going to develop inside this
[03:08] project only.
[03:09] And this project I'm going to store inside a workspace location like Document/Storage/Workspaces/java
[03:16] .
[03:16] So after selecting the location we need to select the language as Java, build system as interlliJ
[03:22] and the JDK as 21%.
[03:26] Let me click on this create button.
[03:28] You can see we got a brand new Java project, and inside this project there are no classes defined as
[03:35] of now.
[03:35] So let's try to create a class.
[03:37] So what is a step that we need to follow to create a class inside IntelliJ.
[03:41] You need to right click on this SC folder.
[03:44] Once you right click you need to go to the new option.
[03:47] And inside the new option we have a Java class option.
[03:50] So let me click on that.
[03:52] And here first we need to provide the name of our Java class.
[03:56] Let's try to create a class name as Car post that
[04:00] let me press enter and you can see I got a brand new Java class.
[04:04] So there is a C icon as well indicating Java class.
[04:08] So I can try to zoom this code by pressing command and moving my mouse wheel inside window
[04:14] you can do the same by using control and mouse wheel.
[04:18] So you can see this is a syntax which we need to follow whenever we want to create a Java class.
[04:24] The IDE or
[04:25] the intelliJ is doing a great job here, helping the developers to create the class very easily.
[04:32] Like we know, the extension of the Java class has to be .java.
[04:35] So the important information that I want to share here is always make sure this class has to be in the
[04:42] same small letters, because this is a keyword inside Java, which will help my JVM to understand what
[04:49] is this file?
[04:50] Is it a Java class or is it an interface?
[04:53] So interface is another concept inside Java which we are going to discuss in the coming sections.
[04:58] For now, let's focus on class alone.
[05:00] So let's see what is going to happen if I try to change this to capital letter.
[05:04] So you can see here I'm getting a compilation error immediately.
[05:07] So this confirms always we need to use c l a s s in complete small letters here.
[05:14] IntelliJ also is trying to help us by highlighting all keywords in Java in a different color.
[05:21] Like you can see here
[05:22] public and class are two different keywords.
[05:25] That's why it is highlighted them in a same color which is orange.
[05:29] Whereas developer defined name like car, it is in the white color font.
[05:34] So this is also can help you to differentiate between a Java keyword or a developer defined value.
[05:40] Like I said before, this public key is completely optional if you don't mention this public
[05:46] also, still your JVM is not going to complain anything, it is going to accept it as a valid Java class.
[05:52] So there is a very good history behind the modifiers like public, private, default,
[05:58] So there are some modifiers which we need to discuss in the coming sections.
[06:02] But for now, let's continue to use public as an modifier just before your class keyword.
[06:09] And this opening and closing curly braces are mandatory.
[06:12] If you try to give something a normal bracket, you can see you're going to get an error.
[06:18] That's why always use the curly braces only.
[06:21] And whatever you want to define inside your class, you need to define inside these curly braces.
[06:27] Only if I try to go outside of this curly braces and try to mention something like int age as a variable,
[06:35] you can see my compiler is not going to accept it is going to shout at you hey developer, please define
[06:41] all your variables, methods, everything inside the class body only don't go outside of the class,
[06:46] so class is our boundary inside which we have to define all our Java code.
[06:51] So let me remove this error code.
[06:53] I hope you are clear with this basic step of creating a class inside Java.
[06:58] Now, as a next step, let's try to create one more class with with the name Employee.
[07:04] I want you to pause this video and try to create this class on your own, and see if you are successful
[07:10] at it.
[07:11] I hope you're successful at it.
[07:13] Otherwise don't worry.
[07:14] Please follow the steps that I'm trying to explain here.
[07:17] As usual, you need to right click on the source and here select the new Java class option.
[07:22] And the class name that I want to give here is Employee.
[07:26] The case style that we have to follow whenever we are trying to define a class name is Pascal Case Style.
[07:32] That means each and every word has to start with a capital letter.
[07:35] But this is not a mandatory rule.
[07:37] Even you can create a class by following camel case or all capital letter or all small letters.
[07:44] Let's see if the compiler is going to accept it or not.
[07:47] So I'm trying to give the class name as Employee, and here I have not followed any Pascal case style.
[07:54] I have given all small letters inside my class name.
[07:57] So let me create this class.
[07:59] You can see there are no compilation errors.
[08:02] This confirms it is not mandatory to follow the Pascal case style or any other case style, but as a
[08:09] Java developer, we are responsible to follow the standards because all other developers, if they follow
[08:16] a standard and if you are not following, then your code is not going to look good for others.
[08:21] So that's why let's follow the standards for the same,
[08:24] First, let me delete this file.
[08:26] So let me select this class and press delete.
[08:29] It will ask you for confirmation.
[08:31] You can click on this okay button.
[08:33] Now I'll try to create the class one more time.
[08:35] This time I will try to give a proper name with the Employee as capital letter.
[08:41] Let me press enter here
[08:42] you can see we have created a another class successfully.
[08:46] Hooray!
[08:47] We are successful at this initial baby step.
[08:50] I know this may look very basic for you, but believe me, you are going to create thousands of classes
[08:56] throughout your life, so please be familiar with this process.
[09:00] I hope you are clear on how to create a Java class, and why we should create a Java class.
[09:05] As a next step, we should populate the body of a class with the required attributes or variables and
[09:12] the methods based upon our business scenario.
[09:15] So let's try to understand how to create a variables or fields inside a class from the next lecture.
[09:21] Thank you.
[09:21] Bye.

----------------------------------------

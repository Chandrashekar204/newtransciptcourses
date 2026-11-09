# 4.19 — Problem with default or no-args constructor

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now, we have a constructor where it is not performing any initialization.
[00:06] We simply have a System.out.println() statement.
[00:09] As a next step, I want to further enhance this constructor.
[00:13] If you see, as of now we are trying to initialize the fields like firstName, lastName, age and
[00:19] gender
[00:20] once the object is completely created. Instead of doing this, I want to initialize the fields during
[00:27] the object creation process itself. For the same where I need to write that initialization logic,
[00:34] I need to write inside the constructor of the Employee class.
[00:37] So let me go to the Employee.java and here is the constructor.
[00:41] Here inside my constructor, I can simply try to invoke the firstName which is available inside this
[00:47] Java class.
[00:48] To this I'm going to assign the value which is John.
[00:53] With this, I'm able to assign a value to the firstName field, but this is not a standard.
[00:58] Whenever you are trying to assign a value to the Java object field, then we should use a keyword which
[01:05] is this this dot.
[01:07] Then I should invoke the field name.
[01:10] So what is ' this '
[01:11] refers, ' this ' inside Java refers to the current instance of the class or the current object of the class
[01:18] that we are trying to create.
[01:20] So very similarly, let me try to mention this.lastName and to this lastName I'm going to assign
[01:27] the value doe.
[01:29] And after the lastName I'm going to mention this.age and the age value I'll mention as 30, followed
[01:36] by this dot gender.
[01:39] And the value that I want to mention here is M with this right now we are doing the initialization in
[01:46] the constructor itself.
[01:47] So let me save this and go to the EmployeeMain.
[01:50] And I'm going to remove all these four lines of code.
[01:54] But instead of removing them I'm going to comment this code.
[01:57] So what is commenting, inside Java
[01:59] instead of deleting the code we can comment it for later use.
[02:03] I want to comment this code so that you can have this as a reference
[02:07] when I check in this code into the GitHub repo. Whenever we comment our code, the JVM and the Java
[02:12] compiler, they are going to ignore all the commented code and they are not going to execute that commented
[02:18] code.
[02:19] We are going to talk very in detail about Java comments in the coming sections.
[02:23] For now, I want to comment these entire four lines of code.
[02:27] So I have to select this code and post that
[02:30] I can use a shortcut, which will help me to comment the block of code.
[02:34] So how to know what is a shortcut?
[02:36] To understand what is a shortcut, you can go to the help button here and click on the option which
[02:42] is Keyboard shortcut PDF.
[02:44] As soon as you click on that, you're going to see a PDF inside your browser.
[02:49] And this PDF has complete shortcuts that you can use inside your IntelliJ.
[02:55] So this first page is showing the shortcuts that you can use for Windows and Linux
[03:01] operating system.
[03:02] Whereas in the next page we have mac OS related shortcuts.
[03:07] So inside this PDF, if I search for comments, there are two shortcuts.
[03:12] One is which is going to help me to comment and comment a given line, whereas the second one is going
[03:18] to help me to comment a block of code.
[03:21] I'm more interested of the block comment.
[03:23] So the shortcut for this in Windows or Linux is, Ctrl + Shift +/, whereas inside
[03:30] mac it is going to be command option forward slash.
[03:34] So let me press command option forward slash inside my mac OS.
[03:40] And you can see right now the code is commented.
[03:43] That means this code is as good as deleted from Java compiler or JVM perspective.
[03:48] If you want to retain for future use or future reference, we can always comment that code.
[03:54] So now whatever breakpoint that we have put here, it is going to be invalid because at this line there
[04:00] is no Java code.
[04:01] This is a commented code.
[04:03] With that reason we can remove these breakpoints.
[04:06] I'll try to run my program in a debug mode.
[04:08] You can see all the code that we have defined here is executed.
[04:13] Now if I try to release this breakpoint inside my constructor, I'm getting an output which is object
[04:18] is getting created and the age and the char details.
[04:22] Did you see the beauty?
[04:23] I have not defined the data for my variables inside the object, inside my EmployeeMain, but still
[04:29] I'm seeing the age and gender details inside my output.
[04:32] Because we have written this initialization logic inside the constructor of the Java class, I can also
[04:39] show you at runtime by keeping a breakpoint at the line number 10.
[04:43] So let me run the program in debug mode.
[04:45] Now the Java program stopped inside the constructor.
[04:48] I can resume the program, and this time the breakpoint stopped at the line number 10 of EmployeeMain.
[04:55] At this point of time, if I open this Employee object, you'll be able to see
[05:00] all the values that we populated inside the constructor firstName, lastName, age and gender.
[05:06] So these are power of constructor.
[05:08] We have written some initialization logic, which is going to be executed every time we try to create
[05:13] an object.
[05:14] So let me release this program.
[05:16] But there is a problem here.
[05:18] We're trying to hardcode the values like John, Doe, 30 and M inside the constructor.
[05:24] What is a disadvantage with this approach?
[05:26] If I try to create any object with the help of Employee, all those objects, they are going to have
[05:33] the same values.
[05:34] I can also show you that.
[05:36] For example, let me try to create one more object with the name as employee2, whereas the previous
[05:43] one I will rename it as employee1.
[05:45] Here I'm trying to define two Employee objects since the employee variable name is nowhere available
[05:52] I'm getting this compilation errors.
[05:54] So let me replace this employee with employee1 and let me copy these two statements.
[06:00] And in the place of employee1 I'm going to mention employee2.
[06:03] This time let me execute the program.
[06:07] We'll see that both these objects, they are going to have same values.
[06:10] So let me execute this.
[06:11] The breakpoint stopped inside the constructor.
[06:14] Let me release this again
[06:15] you can see after releasing one more time the breakpoint stopped.
[06:18] The reason is we are trying to create two objects here like employee1 and employee2.
[06:24] With that reason the breakpoint is going to stop two times.
[06:27] If I try to release this time, the breakpoint will stop at the System.out.println()
[06:32] java statement.
[06:33] This time you can see there are two objects.
[06:35] One is employee1 and employee2.
[06:38] Both these objects, they have the same data.
[06:41] So this is kind of a disadvantage if you try to hard code the initialization values inside the constructor
[06:47] instead.
[06:48] What we have to do instead, we need to ask the developer itself to pass the values that he want to
[06:55] assign to a particular object that we can achieve with the help of constructor overloading.
[07:01] Let's discuss what is this constructor overloading in the next lecture.
[07:05] Before that, let me go to the debug window and release the breakpoints.
[07:10] You can see I'm getting the object is getting created two times because we have created two objects
[07:15] and the output also we received two times because we have mentioned the System.out.println() for
[07:21] both objects like employee1 and employee2.
[07:24] I hope this is clear to you.
[07:25] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

# 8.23 — Local variables & Scope - Theory

> Section 8: Control flow statements in Java

[00:00] As of now
[00:01] we gained knowledge inside this course on how to build a conditional logic with the help of if statements
[00:08] and looping logic with the help of for loop, while loop, do while.
[00:12] So we have done a lot of discussion around the conditional statements and branching statements with
[00:19] this knowledge
[00:19] now you should be able to easily understand about a new concept which is local variables and scope.
[00:27] At the starting of the course, we discussed about instance variables and static variables that we can
[00:33] create as part of the class definition.
[00:35] But what are these local variables?
[00:37] So let's try to understand the same.
[00:39] Local variables are the variables that are declared inside a method or a block.
[00:45] When I say block, it can be an if block or for loop block or while block, or do while block or switch
[00:52] block.
[00:52] So whenever you define a variable inside a block or a method that variable, we can call it as local
[00:59] variable and the scope of it is going to be limited to the block or the method in which it is declared.
[01:06] When I say scope, the meaning is we can only access that variable only within the area where we have
[01:13] defined that variable.
[01:14] If I declared a local variable within a if block, then I can access that variable only within that
[01:20] if block.
[01:21] So the scope is going to be limited to that if block itself.
[01:24] And we should not be able to access that variable outside of the if block.
[01:29] Let me give an example to make it more clear.
[01:32] Here you can see I have declared a method with the name my method.
[01:36] Inside the method I have defined a variable x of type int and this holds a value ten.
[01:43] So here x is a local variable because I'm not defining this variable inside the class definition.
[01:50] Since this is only applicable within this method, we can call it as local variable and this local variable
[01:57] I can access only within this method.
[02:00] Outside of this method or
[02:02] after ending of this method, x is no longer is going to be available.
[02:07] So this is the example of defining a local variable inside a method.
[02:12] I'm going to show you how to define local variables inside a if block or for loop or switch statement
[02:19] in few seconds.
[02:20] But before that, I want to highlight you that whenever we are defining instance variables, local variables,
[02:26] or static variables inside our Java class, you can use the same name and your compiler is not going
[02:32] to complain anything. Because when I define an instance variable, how can I access that only with the
[02:38] help of the object of the class, whereas a static variable or a class variable I can access only with
[02:44] the help of the class name, and similarly the local variable I can access only within the scope.
[02:49] With that, since there is a clear difference on how to access all these kind of variables, the compiler
[02:56] is not going to complain anything.
[02:58] Even if you use the same name for an instance variable,
[03:01] static variable and local variable.
[03:03] But it is always advisable to use different and meaningful names for your variables
[03:10] to avoid confusion.
[03:11] We know instance variables are going to be stored inside the heap memory, and the class level variables
[03:17] are static variables
[03:19] they are going to be stored inside the method area or class area.
[03:22] But coming to the local variables they are going to be stored inside the stack memory.
[03:29] So what is a stack memory?
[03:30] Inside the stack memory only all our method invocations, they are going to be maintained in a stack
[03:36] manner.
[03:37] Whenever we are invoking a new method, a new stack is going to be created and all the local variables
[03:43] related to that method, along with the method parameters, everything, they are going to be stored
[03:48] inside the method stack.
[03:50] So once the method execution is completed, the method stack is going to be destroyed.
[03:55] And with that, we will not be able to access any of the local variables.
[03:59] As a next step, let me show you on how to declare the local variables inside the for loop.
[04:05] Like you can see here, I have a method with the name my method
[04:08] inside my method I have an for loop.
[04:11] Inside my for loop I have declared so many local variables.
[04:15] For example, i is a local variable which I can access only within my for loop.
[04:20] Very similarly here I have defined an variable with the name x.
[04:24] So this is also a local variable, and the scope of this local variable is going to be only within the
[04:31] for loop.
[04:32] As soon as we are done with this for loop execution, I will not be able to access this x and i variables
[04:38] even inside the same method like the for loop is present inside a method
[04:43] myMethod().
[04:44] Even inside this method, once I executed my for loop, I will not be able to access both of these local
[04:50] variables, because the scope of these local variables is restricted to the for loop that we have defined.
[04:57] Very similarly, let's try to look at an another
[05:00] example where I'm trying to create multiple local variables inside if and else statement.
[05:07] Here you can see into number is equal to ten.
[05:09] This is a variable within the method and outside of the if and else statements.
[05:15] Since my if and else statements are present within the same method, they should be able to access these
[05:22] local variable.
[05:23] But whatever local variables that I have defined within my if block and else block, I will not be able
[05:30] to access them inside my method like outside of this if and else if I try to access one of the local
[05:36] variable which is square, I'm going to get a compilation error.
[05:40] The same kind of concept is applicable for other kind of loops like while loop, and do while loop.
[05:47] But coming to the switch statement, the local variables that are going to work in a tricky manner.
[05:52] So let's try to understand more details about the local variables inside a switch statement.
[05:58] Here you can see I have an example of a switch statement. Inside my switch statement,
[06:04] under case2, I have defined a local variable i.
[06:07] So int i is equal to number.
[06:10] So the same local variable I will be able to access in the following cases like inside the default,
[06:17] I should be able to access my i variable without any issues, even if I have other case labels like
[06:23] case 3 and case 4.
[06:25] Under my case 2 block, I should be able to access the local variable that I have defined under case 2
[06:31] but case 1 will not be able to access it because by the time the case one is going to be executed.
[06:38] Since the i local variable is not declared,
[06:41] that's why if you try to access the i local variable within the case one, you are going to get the
[06:47] compilation error.
[06:48] On top of that, whatever local variable that we have declared inside.
[06:52] case 2.
[06:53] This variable can only be accessed within the following cases after the case 2, but not outside of
[07:00] the switch statement.
[07:01] Here you can see I'm trying to print the i variable which I have defined under case 2.
[07:06] Since this System.out.println() is outside of my switch statement here
[07:11] also, I'm going to get a compilation error.
[07:13] I hope you are clear about how the local variables are going to work inside the switch block.
[07:19] Before I try to close this lecture, I want to share the standards that you need to follow whenever
[07:25] you are trying to declare local variables inside your methods and blocks.
[07:29] So let's try to understand those.
[07:31] The very first best practice that you need to follow is whenever you are trying to declare local variables,
[07:36] please try to declare them with the narrowest scope possible.
[07:40] That means if you need a variable within the if block, declare it only within the if block.
[07:47] Don't try to declare the local variable outside of your if block within the method, because with that,
[07:53] you are going to increase the scope of your local variable from if block to the method.
[07:59] So this best practice is going to help you in preventing the naming conflicts, and reduces the risk
[08:06] of the accidental modification of the variable values.
[08:10] And the next best practice is, try to give some meaningful variable names for your local variables,
[08:16] so that your code can be easily understand by other developers.
[08:21] Moving on to the next best practice, always make sure to initialize the variables whenever you are
[08:27] trying to declare them.
[08:28] For primitive data types, you don't have to initialize anything because all the primitive data types,
[08:33] they are going to have a default value.
[08:36] Whereas if you are trying to declare a Person object or a String object, don't try to leave them by
[08:42] just declaring them.
[08:44] At least try to initialize them with a null value so that it gives an indication to the other developers
[08:50] that so and so variable object is going to hold a null value, and they need to be very careful while
[08:56] trying to access it, since it may result into NullPointerException.
[09:00] If they don't perform the null check the next standard is,
[09:03] always make sure you are declaring only one variable per line.
[09:08] So Java allows you to define any number of variables in a single line.
[09:12] It's not a good practice because for other developers it is going to be super tough to read your code.
[09:18] So to make your code more readable and maintainable, always try to declare one variable per line moving
[09:25] on to the next best practice, which is avoid declaring unnecessary variables.
[09:31] If you don't need a variable inside your business logic, then don't declare it so
[09:35] this is the simple thumb rule that you need to follow.
[09:38] Otherwise you will have so many unused or unnecessary variables inside your business logic, which will
[09:43] make your code complex to understand and clumsy.
[09:47] And the last, best practice that we have is keep a variable declarations close to their first use.
[09:53] For example, think like your method has 1000 lines of Java code and you are going to use a
[10:00] local variable at the line number 900.
[10:03] Instead of defining this local variable at the line number one of the method, you can simply do the
[10:09] same just before the 900 line.
[10:12] That way you are going to reduce the scope of the local variable.
[10:16] When I say scope in this scenario, all the lines below 900 line, they will not be able to access your
[10:22] local variable because you have not declared it otherwise
[10:25] if you declare it at the very first line, then your local variable can be accessed to write from line
[10:31] number two.
[10:31] So to avoid these kind of situations or error prone scenarios, you can always try to declare local
[10:38] variables close to their first use.
[10:40] With this, I'm assuming you're clear about what are local variables and the scope of them.
[10:45] I know you may have some questions.
[10:47] Let's try to see the demo of this local variables in the next lecture.
[10:51] Thank you
[10:52] bye.

----------------------------------------

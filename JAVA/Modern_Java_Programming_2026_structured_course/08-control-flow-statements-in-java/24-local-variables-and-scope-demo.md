# 8.24 — Local variables & Scope - Demo

> Section 8: Control flow statements in Java

[00:00] Let's see the demo of the local variables for the same,
[00:03] I'm going to create a new Java class.
[00:06] The class name is going to be LocalVariablesDemo.
[00:11] Inside this class I'm going to create a main() method.
[00:15] After the main() method I'm going to create one more method,
[00:19] the method name is going to be public void myMethod().
[00:24] And inside this method I'm going to declare a variable which is x = 10 and the same
[00:31] I'm going to print it with the help of System.out.println().
[00:35] You can see here we have declared a local variable x and this x
[00:39] we should be able to access within this method only.
[00:42] And one more important point that you need to be aware is, you will not be able to access these x local
[00:48] variable above this statement.
[00:51] For example, if I try to mention the same statement just above, the int x = 10, I'm going
[00:57] to get the compilation error because by the time this line number eight is getting executed, this variable
[01:04] x is said to be declared.
[01:06] So this confirms we can only access the local variable once it is completely declared.
[01:12] Like I said before, we can only access this x variable within this method.
[01:16] If I try to access this x variable within the other method like main() method, I'm going to get a compilation
[01:23] error because for this method, this variable which is x is not going to make any sense.
[01:29] So let me remove this System.out.println().
[01:32] If needed, we can define an instance variable with the same name inside your class as well.
[01:39] Like you can see here, I'm able to create an instance variable with the same name, but I'm not getting
[01:45] any compilation error because anyone who wants to access this x variable, they can only access it with
[01:52] the help of the object of this class, whereas this x local variable they can directly access within
[01:59] the method.
[02:00] So inside this method, if you want to access this x variable, first you need to create the object
[02:05] of this class.
[02:06] And from the object only you should be able to access this x variable.
[02:10] But like I said, please don't follow this practice.
[02:13] Though it is technically possible because it is going to create a lot of confusion to other developers who
[02:19] are trying to understand your Java program.
[02:22] As a next step, let's try to explore how to declare the local variables inside the for loop.
[02:26] For the same,
[02:27] I'm going to create a for loop here very quickly.
[02:30] You can see just to save some time, I pasted a for loop within my main() method.
[02:34] So inside my for loop we have two local variables,
[02:38] one is i and the other one is x.
[02:41] So this x and this x is completely different because they are present in two different methods.
[02:47] That's why there is no conflict
[02:49] and I'm not going to get any compilation errors.
[02:51] Since I have defined these local variables within the for loop, I should be able to access only within
[02:58] this
[02:58] for loop, I will not be able to access just outside this for loop within the same method.
[03:03] For example, here, if I try to copy paste the same System.out.println(), you can see I'm getting an
[03:10] compilation error saying that the variables i and x are cannot be resolved.
[03:15] That's what you can see here
[03:17] if I try to hover on the variable x like cannot resolve
[03:21] symbol x is a compilation error.
[03:23] So the same kind of behavior you will be able to see for if block as well.
[03:28] So let me try to create an if block very quickly here by pasting some code.
[03:33] Here I'm pasting few lines of code
[03:35] you can see
[03:36] first I have created a number local variable within the main() method, and the same I should be able
[03:42] to access in the following code.
[03:43] So inside my if block, I'm creating the local variable square and inside the else block I'm creating
[03:50] another local variable absoluteValue.
[03:53] So this square variable i will not be able to access either inside my else block or outside of my if
[04:01] block.
[04:01] The reason is this square local variable is only scoped within these parentheses.
[04:07] That means within the if block.
[04:09] So if I try to access the square variable outside of my if block, you can see I'm getting the error.
[04:15] The same applies for the absolute value as well.
[04:18] But if I try to access the number, I'm not going to get any compilation error because this number we
[04:24] declared just outside of the if block.
[04:27] And since we are in the same method after the line number ten, we will be able to access this local
[04:33] variable number.
[04:34] I hope this makes sense.
[04:35] As a next step, let me quickly show you the demo of the local variables inside the switch case statement.
[04:42] The switch case statement related logic I'm going to develop inside another method that we have created,
[04:48] which is myMethod().
[04:49] So here I'm going to paste a few lines of code.
[04:52] You can see
[04:53] first I have declared a number local variable with the value two and post that using the same I'm trying
[04:59] to
[05:00] build the switch case logic.
[05:02] So there is a case 1, case 2 and default.
[05:05] Inside my case 2, I have created a local variable with the name i to the same
[05:10] I'm trying to assign the value of number.
[05:12] So since I have declared this local variable inside case 2, I will be able to access inside all the
[05:19] cases just before the case 2.
[05:21] Like here, I'm able to access the i variable and I'm able to reinitialize it with the new value, which
[05:27] is 10.
[05:27] That's why even if I'm trying to access it and print it with the help of System.out.println(), I'm not
[05:33] getting any compilation error, but if you try to do the same inside the case 1, we are getting a
[05:39] compilation error because by the time the case 1 is getting executed, this variable is yet to be
[05:46] created inside the case 2.
[05:48] That's why we are getting a compilation error.
[05:50] Let me comment out this now if you can scroll down
[05:54] I have a System.out.println() after the switch statement where I'm trying to access the i variable.
[06:00] Since this i variable is scoped within the switch loop, we will not be able to access it outside of
[06:07] the switch case statement.
[06:08] That's why we are also getting an compilation error here.
[06:12] I hope you are clear.
[06:13] So let me comment out this line as well, so that we are not going to get any compilation error inside
[06:19] our Java program.
[06:20] So please refer to this example and code present inside the GitHub repo.
[06:25] Please try the same inside your IntelliJ as well, and try various combinations and scenarios to better
[06:32] understand about the local variables.
[06:34] If you have any questions, obviously I'm there for you.
[06:37] Please post your questions.
[06:39] Thank you and I'll catch you in the next lecture bye.


########################################

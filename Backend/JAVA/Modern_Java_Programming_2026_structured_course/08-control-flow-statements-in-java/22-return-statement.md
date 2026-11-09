# 8.22 — return statement

> Section 8: Control flow statements in Java

[00:00] The next branching statement that we have is return statement.
[00:04] We have been using the return statement a lot inside our methods to return the output.
[00:10] For example, here you can see I have a method which is going to perform the addition based upon the
[00:16] given two input numbers.
[00:18] After performing the addition, I can return the variable at the output from this method with the help
[00:25] of the return statement.
[00:26] So we have been using these.
[00:28] There is nothing new here, but as of now you might be thinking there will be only one return statement
[00:34] allowed inside the method, but that is not correct.
[00:37] Let me show you an example where I have built a method with the help of if conditions.
[00:43] Here you can see the method name is get student grade and to this method, if you pass the marks as
[00:50] an input based upon the marks, the method is going to return either passed or failed.
[00:56] So how we are returning,
[00:57] we are returning the value based upon the return statement.
[01:00] In this scenario, we have mentioned the return statement at two different places, but still your compiler
[01:07] is not going to complain anything because the reason is the compiler knows
[01:12] at any case, either my if condition will be executed or my else condition will be executed very similarly
[01:19] if needed, you can always use the return statement inside the for loop while loop or do while loop
[01:26] to stop the method execution and return to the parent method.
[01:30] So whenever you are using the conditional statements or looping statements, it's perfectly fine to
[01:36] define multiple return statements.
[01:38] Your compiler can understand your logic and it is not going to complain anything.
[01:43] Let me show you a few examples around the return statement inside my Intellig I'm going to create a
[01:49] new Java class.
[01:51] The class name is going to be ReturnStatementDemo.
[01:56] Inside this class,
[01:57] first I need to create the main() method
[02:00] as usual, this is a tradition that we need to follow.
[02:03] Post that I'm going to create a static method which is public static string getStudentGrade()
[02:09] and this method is going to accept the marks of the students.
[02:17] And based upon the marks, the method is going to return a String value as an output.
[02:22] So let me write an if condition here.
[02:25] If the marks are greater than or equal to 40, then I'm going to return the String which is passed.
[02:35] Otherwise, with the help of the else statement, I'm going to return the string which is failed.
[02:43] So here you can see we have two return statements.
[02:45] Let's try to invoke this method and see what is going to happen.
[02:49] So to invoke this method, I can simply mention the method name inside my main() method and pass the marks
[02:56] which is 90, and from the method
[02:58] since I'm going to get a String output, I can catch the same with the variable result and the same
[03:05] I can try to print out inside the main() method.
[03:08] So let me try to execute this class and we're going to get the output as passed.
[03:12] Now let me show you what is going to happen if I'm not returning anything from one of the else block.
[03:18] So here you can see we are going to get a compilation error.
[03:22] The error is missing return statement.
[03:26] My compiler is asking you to write and return statement inside your else.
[03:30] The reason is my compiler is thinking about a scenario
[03:34] what if the if block is not going to be executed?
[03:37] Only the else block is going to be executed.
[03:39] In such scenarios, if you're not returning anything that is going to violate the method definition
[03:45] that we have defined.
[03:46] So that's why we are getting an compilation error.
[03:50] So to resolve this, we can bring back the return statement.
[03:53] If you don't want to define these multiple return statements, we can also optimize this logic by defining
[03:59] a variable which is String result.
[04:02] And to this result variable I can assign the output like past and the same I can do here as well, like
[04:09] failed.
[04:09] So at last I can simply mention a single return statement which is return result.
[04:15] So this way there are multiple possibilities on how you can write your business logic.
[04:21] At the end of the day, you need to choose what works for you.
[04:24] Now let me show you how to use the return statement inside a for loop. For the same,
[04:30] first, I'm going to create a static method which is public static,
[04:35] after the static, I'm going to mention int as the return type from the method and the method name
[04:40] I'll give it as findAndReturnNumber().
[04:43] So this is the method name.
[04:44] And to this method I'm going to pass the array of the numbers as an input.
[04:50] So the variable name I will keep it as an arrayOfNums.
[04:55] And the second input that I want to pass is what is that targeted
[05:00] element that I'm trying to search inside that given array.
[05:03] So let me mention the curly braces.
[05:05] Inside this method, I'm going to write a logic with the help of for loop.
[05:09] So let me copy the for loop logic that we have written previously inside the break statement.
[05:15] So here we have a logic to search for a number inside the arrayOfNums.
[05:20] So let me copy this and paste it the same here inside my method the variable name is going to be arrayOfNums
[05:27] .
[05:27] So let me mention the same.
[05:29] And at last, since we are looking for the value which is present inside the target variable, I need
[05:35] to mention the same here.
[05:37] So whenever I found the number inside my number, I'm simply going to write and return statement saying
[05:43] that return.
[05:45] After the return I'm going to mention i.
[05:48] So here whenever I found a match, I'm trying to send the position or the index number inside the array
[05:54] at which I found the given target number.
[05:57] Otherwise, if I didn't find any match inside my entire array, I'm going to simply mention return statement
[06:05] outside with the value as -1.
[06:08] So whenever I'm sending minus one, it's an indication to the caller or the parent method that I'm not
[06:14] able to find the given target number inside the array.
[06:18] I hope you are clear with the logic that we have inside the find and return number method.
[06:24] Inside the for loop, you can see I'm using the return statement.
[06:28] So whenever this condition became true, I'm simply returning from this entire method.
[06:34] That means I'm not going to execute any further statements inside this method, including the for loop.
[06:40] As a next step, we can try to invoke this method.
[06:43] To invoke this method, I'm going to go to the main() method.
[06:47] And here I'll create an int variable with the name index and post that I will try to invoke the method
[06:55] and to this method we need to pass the array and the target number.
[06:59] So let me take the array and target number from here and paste it here and post that I'm going to pass
[07:07] the same as an method input parameters for that method that we have defined.
[07:13] So after the method invocation we are going to get the index value as an output.
[07:18] Let me try to print out the index value so that we can clearly identify whether we have found that given
[07:25] number.
[07:25] If I try to change the given number to something else, then the output we are going to get is -1
[07:31] .
[07:32] I hope you are clear, so always use the return statement based upon your requirements.
[07:37] It's perfectly fine to use multiple return statements inside your method.
[07:42] The only rule that you need to be aware is your compiler is going to expect you to return only once,
[07:50] based upon your conditional logic.
[07:53] For example, inside my whole method based upon this if logic, I'm going to return only once.
[07:59] As long as you take care of that rule, the compiler will be happy
[08:03] even if you mention multiple return statements inside different if conditions or inside different loops.
[08:09] With this we are done discussing everything about the branching statements.
[08:13] I hope you are clear.
[08:14] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

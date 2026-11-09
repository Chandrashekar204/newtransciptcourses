# 13.8 — BufferedReader example to identify prime number

> Section 13: Accept input using BufferedReader and Scanner

[00:00] Inside this lecture, let's try to write a small Java program to accept a number from an end user and
[00:07] post that
[00:07] our Java program should identify whether the given input number is a prime number or not.
[00:13] To get started around this example, first I need to create a new Java class, and the class name I'm
[00:19] going to give here is PrimeNumberChecker.
[00:22] Inside this class, as usual, first we need to create the main method and post that I'm going to write
[00:28] the logic first to accept a number from an end user, I can try to take all this code and paste it inside
[00:36] the PrimeNumberChecker.
[00:37] So you can see here we are trying to ask the end user to enter a numerical value.
[00:43] Maybe we can try to further improvise this statement saying that.
[00:46] Please enter a numerical value to identify if it is a prime number or not.
[00:54] So this is the statement that I want to give here.
[00:57] So there is a spelling mistake inside
[00:59] identify.
[01:00] So let me correct that.
[01:01] As a next step I need to write the logic to identify if a given number is an prime number or not.
[01:07] I can try to write all the logic inside the same method, or I can try to create another helper method
[01:13] inside this class, which is going to help me to identify whether a given number is an prime number
[01:18] or not, by accepting a numerical value as an input parameter.
[01:22] So let me try to create the same like I can say private static boolean, and the method name I can mention
[01:29] here is isPrime() followed by int num.
[01:33] So my static method, it is going to accept one into numerical value as an input parameter.
[01:39] So that's why I'm trying to give this int name as an method parameter.
[01:43] Now to write some business logic, first we need to think about when a number is going to become a prime
[01:49] number.
[01:49] So there are two conditions it has to satisfy.
[01:52] The very first condition is, it should be greater than one because zero and one we can't construct them
[01:59] as prime numbers.
[02:00] So that's the very first condition.
[02:02] So that's why let me try to write the code related to the first condition.
[02:07] I will say if given number is less than or equal to one, I will just return false, saying that this
[02:16] is not a prime number for now, I'm not worrying about the negative numbers, any number which is less
[02:21] than or equal to one.
[02:23] I'm going to simply return a value saying that this is not a prime number.
[02:27] The second condition that we need to use to identify whether a given number is a prime number or not
[02:33] is the given number, should not be divisible exactly by any number which is less than itself.
[02:40] For example, if my input number is nine, then I need to divide the nine by all the numbers which are
[02:47] greater than one and less than nine.
[02:49] Like I should start the division right from 2345678.
[02:54] At any point of time, if my number is exactly divisible, then I can simply say my number is not a
[03:01] prime number.
[03:02] So that's the logic that we need to write.
[03:03] So since my logic needs to be run for each number, this can be achieved easily with the looping logic.
[03:10] So I'm going to write a for loop here.
[03:12] So first I'll mention int i is equal to two because we should start that division operation right from
[03:20] the two, but not the one, because every number is always divisible by one.
[03:25] That's why we're not going to consider one followed by I should say i less than given number, which
[03:31] is num.
[03:32] And at last I can mention i++ followed by curly braces.
[03:36] And inside my for loop I'm going to write a logic which is if num exactly divisible by i, then I'm
[03:45] going to return the false as an boolean value for this method.
[03:51] Otherwise, at the end I want to return true, indicating that my given number is a prime number, like
[03:59] if either this condition or this condition is not satisfied, then at the end I'm going to return the
[04:05] true value.
[04:05] So now we have the helper method available inside the class.
[04:09] As a next step, I should use this helper method by invoking it.
[04:14] So first let me mention boolean
[04:17] isPrime is equal to and I'm going to invoke the isPrime() method.
[04:22] And to the same I'm going to pass the input variable which is num.
[04:26] And at last, based upon the boolean output, I want to print a statement whether a given number is
[04:31] a prime number or not.
[04:33] So I can say if is prime, that means if it is true, then I'm going to print a statement saying that
[04:40] given number is a prime number.
[04:44] Otherwise, inside the else I can simply write given number is not a prime number.
[04:51] So now our program is ready.
[04:53] Let me execute the program.
[04:55] You can see it is asking me to enter a numerical value.
[04:59] So first I'm.
[05:00] Going to enter the value as nine.
[05:01] Since this is going to be exactly divisible by three, it is not going to be a prime number.
[05:07] So let me press enter.
[05:08] And here you can see we are getting an output which is given number is not a prime number.
[05:13] This time I'm going to give a valid prime number as an input.
[05:17] Maybe I'll try to give 13 which is a valid prime number.
[05:21] After giving this number I'm going to press enter and this time you can see we are getting the output
[05:25] which is given number is a prime number.
[05:28] Hooray!
[05:29] We are getting the proper output from our Java program.
[05:33] So as of now you can see this for loop
[05:36] it is going to be executed for all the numbers which are less than my prime number.
[05:42] So if I give a big number like maybe a five digit number, then in such scenarios my for loop is going
[05:49] to execute for all the numbers which which are less than my given input number.
[05:53] So though our program is working perfectly right now, it is not a perfectly optimized solution.
[05:58] So there is a better solution than this.
[06:01] So let me show you what is that?
[06:02] The solution is instead of this i < num.
[06:05] I'm going to mention i <= Mathsqrt().
[06:11] So sqrt() is a method which is going to help us to calculate the square root of a given number.
[06:18] So to this square root method I'm going to pass the input number.
[06:23] And with this the for loop it is going to be executed only very few number of times.
[06:29] For example, if I give my input number as 25 square root of 25, it is going to be five.
[06:35] And with that my for loop, it is going to be executed only for two, three, four, five numbers.
[06:41] And it is going to bring lot of performance improvements to my program.
[06:45] So this is one of the approach that we can use to identify whether a given number is a prime number
[06:50] or not.
[06:51] So always calculate the square root of the given number and perform the division by using all the numbers
[06:58] which are less than or equal to the square root number.
[07:01] If it is exactly divisible, then it is a prime number, otherwise it is not.
[07:05] So here you may have a question.
[07:07] How do I know these kind of shortcuts or techniques while solving the other kinds of examples or problems
[07:14] inside real projects, so there is no shortcut for it.
[07:17] You should first look for a most optimized approach by looking all the possible solutions around a scenario.
[07:25] If you take the prime number itself as an example, you need to check the mathematics shortcuts.
[07:29] To identify a prime number and the same you need to replicate with the help of Java program.
[07:35] So that's why always practice as many examples as possible by going to the websites like Topcoder,
[07:42] LeetCode, Hackerrank.
[07:44] So they will have good amount of examples.
[07:47] Since the focus right now inside this course is only to teach you the syntax about the Java programming
[07:52] language.
[07:53] I'm not going to focus a lot on the examples or real life problems, so it is your responsibility to
[07:59] solve those problems because there are thousands of problems.
[08:03] If I start discussing all of them, it is going to take years and years of time to complete this course.
[08:09] I hope you are convinced with my discussion.
[08:11] Now let's try to execute this program and validate if it is really working or not.
[08:16] So first I'm going to enter 25.
[08:18] And for this we are going to get the output as given number is not a prime number.
[08:23] Next I'm going to execute this program one more time
[08:25] and this time I'm going to give the input as 101.
[08:29] And this time you can see we are getting the output which is given number is a prime number.
[08:34] I hope you like this program and you understand it.
[08:37] My humble request is to practice this example inside your intelliJ as well.
[08:42] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

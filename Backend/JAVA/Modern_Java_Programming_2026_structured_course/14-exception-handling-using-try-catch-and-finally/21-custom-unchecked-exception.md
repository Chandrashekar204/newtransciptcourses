# 14.21 — Custom Unchecked Exception

> Section 14: Exception handling using try, catch and finally

[00:00] Let's try to create an custom unchecked exception inside this lecture it is going to be super simple.
[00:06] We just have to copy the same class which is InvalidAException and paste it inside the same package.
[00:13] The class name I'm going to change to DivideByZeroException.
[00:19] I'm going to throw this custom exception whenever someone is trying to perform a division operation
[00:24] with zero as a denominator value, let me press enter and post that
[00:28] the only change that we have to do is we need to make sure the constructor names are also proper, like
[00:34] same as a class names.
[00:35] After that, instead of these exception, we need to extend the RuntimeException.
[00:41] With this we have our own custom unchecked exception ready.
[00:45] As a next step, I can try to use it inside a Java program for custom exception classes
[00:52] you can see IntelliJ is showing them in a different icon.
[00:55] So this is a beauty of IntelliJ.
[00:57] Now let me try to create a Java class with the name DivideByZero. Inside this class,
[01:05] first I'm going to write a main() method, followed by
[01:08] I'm going to create the Scanner object using which I can try to ask and input data from an end user.
[01:16] So first I'm going to ask to enter the numerator value like please enter a numerator number value to
[01:26] perform the division.
[01:28] So this is the very first statement that I can try to accept the input inside a variable, which is
[01:35] numerator of type int using the scanner.nextInt().
[01:41] After this, I can copy the same two lines again inside the same method, and I can change the message
[01:48] to
[01:48] please enter a denominator followed by,
[01:52] I can rename this variable to denominator.
[01:57] So there is a spelling mistake.
[01:58] Let me correct it.
[01:59] Now we have the numerator and denominator ready.
[02:02] As a next step, I can try to perform the actual division and catch the output inside a variable called
[02:09] result.
[02:10] So how to perform the division.
[02:11] So to perform the division first I can mention the numerator value followed by division symbol.
[02:17] And after this I'm going to mention denominator.
[02:19] At last we can try to print out the result onto the console.
[02:23] If I try to execute this program, you can see first it is going to ask me the numerator.
[02:28] I'm entering the value as ten, followed by I'm going to enter the denominator value as five.
[02:34] And you can see we are getting that two as an output.
[02:37] Now this time I'm going to enter the denominator as zero.
[02:42] And obviously we are going to get an ArithematicException.
[02:46] Though this looks good
[02:47] but like I said to look more professional inside the real projects we need to throw our own custom exception.
[02:53] As of now we are trying to throw the ArithmeticException.
[02:56] And it may not be useful for non-technical users to understand about it.
[03:01] That's why I have defined a more meaningful custom exception, which is DivideByZeroException.
[03:08] So let me throw the same by having an if check inside my main() method.
[03:13] So I'm going to check if denominator is equal to is equal to zero
[03:18] I will simply throw the custom exception that I have defined, which is DivideByZeroException.
[03:25] And to this I can pass a message which is Denominator cannot be zero.
[03:32] So this is what I want to pass to the constructor of this DivideByZeroException.
[03:36] Now if I try to execute this program, you can see this time we are going to get a more meaningful exception
[03:43] because we are trying to use a custom exception that we have defined.
[03:46] So first let me enter the numerator as ten followed by denominator
[03:50] I'm going to enter the value as zero.
[03:52] Hooray!
[03:52] We are getting our own custom exception which is DivideByZeroException.
[03:58] So this is a custom unchecked exception
[04:01] that's why my compiler is not forcing me to handle it with the catch block or with a throw keyword,
[04:07] whereas with the custom checked exception that we have seen previously inside the program, which is
[04:14] accept edge details, you can see since we are throwing the custom checked exception, we need to either
[04:20] have a catch block to handle this, or we need to make sure we are having this throws keyword along
[04:24] with the checked exception details in the method signature.
[04:28] With this, I'm assuming you are super clear on how to create your own custom exceptions.
[04:33] For your reference, I'm providing two slides along with the examples on how to create your own custom
[04:40] checked exception and custom unchecked exception.
[04:43] The only difference between them is the superclass that you are going to extend.
[04:48] In the case of custom unchecked exception, you're going to extend the runtime exception, whereas in
[04:54] the scenario of custom checked exception, you're going to extend the exception superclass.
[04:59] Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------

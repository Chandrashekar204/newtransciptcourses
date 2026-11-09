# 14.16 — throw keyword

> Section 14: Exception handling using try, catch and finally

[00:00] Just like throws keyword
[00:02] we also have throw keyword throws is a plural form, whereas throw is a singular form.
[00:08] There is a lot of difference between throws and throw keyword.
[00:11] Like we discussed in the previous lecture, we can use the throws keyword to communicate to others
[00:17] or to the caller methods about the potential exceptions that may arise while executing a given method,
[00:25] whereas with the help of throw keyword, we can manually throw a exception from a method body.
[00:32] Let me show you a demo around the throw keyword, so that it is going to be clear for you.
[00:37] For the same, I'm going to create a new Java class with the name ThrowDemo.
[00:42] So inside this ThrowDemo I'm going to write the main() method.
[00:47] And inside the main() method I'm going to create the object of Division with the help of new operator,
[00:54] followed by default constructor of division.
[00:56] Post that I'm going to perform the divide() operation by invoking the divide method available inside the
[01:04] Division class.
[01:05] To this, I'm going to pass the output 4, 2 and the output
[01:10] from this statement, I'm going to store inside a double variable with the name output and the same
[01:17] at the end
[01:17] I can try to print out inside my console.
[01:21] So if I execute this program, you can see we are going to get the proper output.
[01:25] But let's see what is going to happen if we pass zero as a second input parameter.
[01:30] So this second parameter is going to act as a denominator inside my Division.
[01:34] We know in this kind of scenario we're going to get the ArithmeticException.
[01:38] Me as a developer, I know that I'm going to get a ArithmeticException whenever someone is passing the
[01:45] zero as an second parameter, instead of I invoking this divide() method and getting a runtime exception
[01:52] and post that realizing that there is a runtime exception.
[01:55] Instead of doing all this, I can do some validations on the input data that I'm trying to receive.
[02:02] For example, think like I'm trying to ask an end user using the Scanner object to enter two different
[02:10] numbers.
[02:11] So I have my Scanner object ready post that I'm going to have a System.out.println().
[02:17] Saying that please enter the numerator value followed by I'm going to have a String num1 is equal to
[02:28] Scanner.next().
[02:31] Now I can try to repeat these two statements to accept the second number which is denominator.
[02:37] I can update the System.out.println() to,
[02:40] please enter the denominator value was that I can update this variable name to num2.
[02:47] The same num1 and num2.
[02:49] I can pass as an input to the divide() operation.
[02:52] So let's validate this program if it is working properly.
[02:55] So first it is asking me to enter a numerator value.
[02:58] I'm trying to enter the four post that it is asking me to enter the denominator value.
[03:03] I'm trying to enter the two and you can see we are getting the 2.0 as an output.
[03:07] Now this time I'll try to execute this program one more time.
[03:11] This time I'm going to enter the numerator value as four followed by denominator
[03:16] I'm going to enter a value zero.
[03:17] With this we know we are going to get a ArithmeticException.
[03:21] So this ArithmeticException you can see we are getting from the divide() method which is available inside
[03:27] the Division class.
[03:28] Who invoked this method.
[03:29] The main() method available inside the ThrowDemo class invoke this class.
[03:33] So here I can do a better job instead of I invoking the divide() method and getting scolded by this method.
[03:40] Instead of doing all that long process, I can myself do the input validation and throw an
[03:47] ArithmeticException manually.
[03:48] So let me show you how to do that.
[03:49] So just before this divide operation I'm going to perform if my num2 is equal to zero.
[03:56] So let me check if num two dot equals to zero.
[04:02] So inside this if block I'm going to write throw keyword first.
[04:07] After the throw keyword, I need to create the object of the exception that I want to throw.
[04:11] So here I will mention new ArithmeticException() followed by
[04:16] to this constructor I can mention a message which is Division by zero.
[04:22] Since you are trying to perform the Division by zero, you are getting a ArithmeticException.
[04:26] So this is what I want to communicate to the end user by manually throwing an ArithmeticException.
[04:32] So with this code now we're not going to invoke that divide() method.
[04:36] Instead we are ourselves.
[04:38] Do the validation and if the validation fails we are ourself throwing the exception manually.
[04:44] How we are doing that with the help of throw keyword.
[04:46] So always note that throw keyword is used to manually throw an exception from a method body.
[04:53] Let me execute this program and show you the demo how this is going to change this time.
[04:58] So first I'm going to enter the numerator
[05:00] as 4 followed by denominator, I'm going to enter the zero.
[05:03] As soon as I press enter
[05:04] you can see we are getting a runtime exception of type ArithmeticException with the message that we
[05:11] have provided like division by zero, and this exception triggered at the line number 15 inside the
[05:17] ThrowDemo.main() method.
[05:19] If I click on this hyperlink, I'll be taken to the line number 15.
[05:23] This is the place where the exception is getting triggered.
[05:26] So with the help of throw, I'm doing a better job.
[05:29] I'm not invoking this divide() method unnecessarily because with a zero denominator,
[05:34] if I try to invoke this divide() method, obviously I'm going to get an exception.
[05:38] Why should I invoke other method and get scolded by them instead?
[05:42] I can do a better job by validating the input and throwing the exception manually with the help of throw
[05:48] keyword like you can see on the screen. Everything that we discussed around the throw keyword, along
[05:53] with the example code I have mentioned in this slide
[05:56] for your reference. In the next lecture, let's try to discuss about the difference between throw and
[06:02] throws keyword, because it is a very confusing topic where people may get easily confused.
[06:07] That's why I want to put some more efforts by providing you more details about the throw and throws keyword.
[06:14] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

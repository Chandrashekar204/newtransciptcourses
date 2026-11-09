# 4.10 — Demo of Java methods - Part 2

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Now let's try to create more Java methods for the same.
[00:03] I came to the Employee Java class.
[00:06] First I want to create a Java method which is going to return the age of an employee.
[00:11] So we already have a variable which is going to hold the age value of an employee using the same
[00:17] I'm going to write a Java method.
[00:19] So the method modifier is going to be public.
[00:22] And since I'm going to return the age value of data type byte, I need to mention the return type of
[00:28] the method as byte itself.
[00:30] After the return type, I'm going to mention the name of the method as get age, because I'm going to
[00:37] return the age of the employee for this method
[00:41] also, we're not going to accept any input parameters.
[00:44] That's why I'm keeping it as empty post that I'll just mention the curly braces. Inside the method
[00:49] I'm simply going to write return
[00:52] and what is the variable which is going to hold the age of the employee ?
[00:56] So what is that variable?
[00:57] It is the Java field with the name age.
[01:00] So the same I'm trying to use here. Very similarly
[01:03] this time I'm going to write one more method which is going to return that gender of the employee.
[01:10] For the same,
[01:10] let me copy these existing Java method and paste the same here.
[01:15] You can see here we can't have methods which are looking very similar.
[01:19] So that's why I'm getting an compilation error.
[01:21] Saying that get age is already defined inside the Employee class.
[01:25] To resolve this we just have to change the method details.
[01:29] So first I'm going to change the data type to char.
[01:31] Because from this method we are going to return the gender value and the method name I'll keep it as
[01:38] getGender().
[01:40] And this method also is not going to accept any input parameters.
[01:43] And inside the method body I'm going to return the variable which is gender
[01:48] and this gender variable is present as a Java field inside the Employee class.
[01:53] So whenever someone wants to understand what is the age of an employee or gender of an employee, they
[01:59] can simply invoke these getAge() and getGender() method.
[02:03] So this is a very simple method where it is trying to send that data that we store inside the fields
[02:09] of a given class or a given object.
[02:11] So these kind of methods we call them as getter method because they don't have any other logic other
[02:17] than simply sending that data that they hold inside the Java fields.
[02:22] So that's why we call them as getter methods.
[02:24] Very similarly, we can also write setter methods, which is going to accept the input from the invoking
[02:31] entity and set the same value inside these variables.
[02:35] So we're going to discuss what are these getter and setter methods in the coming sections.
[02:39] But for now I'm just trying to give some information around them.
[02:43] As of now we have return methods which are not accepting any input parameters.
[02:49] Let's try to create a Java method, which is going to accept a method parameters.
[02:54] And based upon those method parameters, we can write some business logic. For the same
[02:59] I'm going to create a new Java class, and the Java class is going to be ArithmeticOperations.
[03:06] So inside these Java class I'm going to perform some arithmetic operations
[03:11] that's why I'm giving the class name as ArithmeticOperations itself.
[03:15] So as of now you can see this class is empty.
[03:18] Inside this class I don't want to create any Java fields because I don't have any such requirement.
[03:24] But I want to create a Java method, which is going to accept two input parameters in the form of integer
[03:31] values, and it is going to perform the addition and return the result to the invoking entity.
[03:37] To get started, first we need to mention public and what is the return type
[03:41] from my method, the return type is going to be int, and after the return type I'm going to mention
[03:46] the method name as sum() and to this method, I always want my invoking callers to send the two input
[03:54] parameters.
[03:54] So these two input parameters are going to follow the data type int only the very first parameter name
[04:02] I'll keep it as num1.
[04:04] And the second parameter name I'll keep it as num2.
[04:07] So number one and number two, it is not mandatory that we always should follow the same data type for
[04:13] all the parameters if needed
[04:15] here I can accept long value, so it's completely fine to have different data types inside the method
[04:23] input parameters.
[04:24] For now, I want to accept both as an int parameters.
[04:28] After defining the input parameters of your method, we need to mention the curly braces and inside
[04:35] the method body, I'm going to perform the addition of these two input parameters.
[04:40] So to perform the addition, what is the expression that we need to write num1 + num2.
[04:47] So this is going to give me an output.
[04:49] And I have to accept that on the left hand side.
[04:52] That's why you can see as of now I'm getting an error because this is not a Java statement.
[04:56] So to accept the output on the left hand side first I need
[05:00] to mention the output variable data type as int and the variable name as result.
[05:05] Now I should not get any compilation errors around this Java statement.
[05:10] The only compilation error right now I have is missing return statement.
[05:14] So let me try to mention the return statement like r e t u r n, is the keyword, and after this keyword
[05:21] we need to mention the variable which is result.
[05:23] So this method has a simple business logic where is invoking this method.
[05:28] They have to pass two numbers and they will get the output as an result.
[05:32] For now we just define the methods.
[05:34] But don't worry how to invoke these methods.
[05:37] We are going to discuss that in the coming lectures.
[05:40] So invoking the methods is also another important concept that you have to understand with these methods
[05:46] that we have created so far, I am assuming you are pretty clear on how to create a non-static methods
[05:53] inside Java classes.
[05:54] Using the same approach, we can create any number of methods.
[05:58] The syntax and the rules are always going to be same throughout the course
[06:02] we are going to create hundreds and hundreds of Java methods in the same process.
[06:07] I'm assuming you will get used to the process to create the Java methods.
[06:12] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

# 14.15 — throws keyword

> Section 14: Exception handling using try, catch and finally

[00:00] throws
[00:00] keyword is another important concept inside Java, which you need to be aware as part of exception handling.
[00:09] Before I try to explain you about throws, keyword and how to use it.
[00:13] First let me share a couple of scenarios.
[00:15] The scenario one is think like you as a developer, you are trying to develop a Java method that has
[00:22] some risky code, and there is a probability that your method may throw an exception are based upon
[00:29] some unexpected situations.
[00:31] The ideal way to stabilize your method is by properly handling the exception inside your Java method,
[00:37] with the help of try and catch, but sometimes a developer may not want to handle the exception.
[00:44] Instead, the developer warned the caller of the method to handle the exception.
[00:49] So in this kind of scenarios, how do we convey this information to the compiler or to the caller methods
[00:56] to handle a specific set of exceptions.
[00:58] So these are scenario one.
[01:00] And the second scenario is this time think like you as a developer want to use a method which is present
[01:07] inside another class.
[01:08] And you have not created this method when you are trying to invoke the method which is written by others,
[01:14] you want to understand whether the method that you are going to use has any potential risky code that
[01:20] may result into an exception.
[01:22] So you want to better understand the method that is written by others in terms of the exceptions that
[01:28] will be thrown by a method, so that you can write enough exception handling logic as part of your own
[01:35] business logic, where you are trying to invoke the method present inside the other class.
[01:40] In these two kind of scenarios, we can use throw keyword.
[01:44] Let me show you a demo about these scenarios and how to handle them.
[01:48] With the help of throw keyword. Inside IntelliJ I'm going to create a Java class.
[01:53] The Java class name is Division.
[01:56] So inside this class I'm going to perform division.
[01:59] So to perform the division operation I'm going to write a method which is public double divide().
[02:06] And to this method I'm going to accept two input parameters which is String num1 and String num2.
[02:14] So I'm going to accept the input data in a String format.
[02:17] Ideally we should accept either in an int format or a double format or a long format.
[02:23] But to show you some demo of exceptions, I am trying to accept in a String format.
[02:28] Post that inside this method, first I need to convert the given numbers into a valid numerical data
[02:35] type.
[02:35] After that, only I can perform an division operation.
[02:39] For example, first I'm going to convert the first parameter into an double value.
[02:44] Like maybe I can mention int n1 is equal to Integer.parseInt(), and to this I'm going to pass
[02:55] the num1 as an input parameter.
[02:57] So Integer is a wrapper class.
[02:59] And inside this we have a static method which is passInt().
[03:02] It is going to accept the String data as an input parameter, and it will try to convert the content
[03:08] of the String object into an int data type.
[03:11] In the similar lines, I'll try to convert the second method parameter as well by creating an int variable
[03:18] n2.
[03:18] And to this I'm going to pass num2 as an input.
[03:22] Post that, I'm going to write a return statement where I'm going to perform the division like n1
[03:28] divided by n2.
[03:30] And with that you can see my divide() method is ready.
[03:32] So here, if this operation result into an int value, it is going to be type casted to double automatically.
[03:40] Since we are going to do the upgrade operation, the casting is going to happen implicitly.
[03:45] As a next step, I am going to write a separate class where I'm going to create the object of this division
[03:51] and invoke these divide() method.
[03:53] So let me create a separate class and the class name I'm going to keep it as ThrowsDemo. Inside this
[04:00] class,
[04:01] first I'm going to create the main() method.
[04:03] And inside the main() method I'm going to create the object of Division with the help of new operator
[04:10] and the default constructor of division.
[04:12] For such, I'm going to perform division.divide(), and to this I'm going to pass 4, 2.
[04:20] I'm trying to pass the valid input data and the output I'm going to catch inside an variable which is
[04:28] output itself.
[04:29] And at last I can try to print out the output value.
[04:32] So if I try to execute this program everything is happy.
[04:35] You can see we are getting the output as 2.0.
[04:37] But how about invalid input data scenarios?
[04:40] Maybe instead of for numerical value I can mention FOUR .
[04:45] So in this kind of scenario, definitely we are going to get an exception which is NumberFormatException.
[04:51] So here there are two issues.
[04:54] This person who has written the throws demo, he's going to ask the developer who has written
[04:59] Division, saying that you never tell me that your method may throw this kind of exception.
[05:05] That is one scenario.
[05:06] The other scenario is based upon this question received from other developer, the developer who has
[05:12] written this class.
[05:13] Now he is thinking on how to communicate to the caller methods about the potential exceptions that may
[05:19] arise based upon the business logic he has written.
[05:22] One potential exception that we have seen is NumberFormatException.
[05:27] The other exception that may happen is, think like someone is passing the zero as a second input parameter.
[05:33] In this scenario, we are going to get the ArithmeticException because we are trying to perform the
[05:38] division by zero.
[05:39] So these are the two possible exceptions that may arise from that division operation.
[05:44] So to communicate about these two other developers, the developer who has developed these methods,
[05:50] he can use that throws keyword inside the method signature.
[05:54] After the throws he can mention any number of exceptions.
[05:58] So the first is going to mention NumberFormatException followed by ArithmeticException.
[06:04] As soon as he mentioned these two exceptions using the throws keyword.
[06:09] Now the other developers who are going to use this method, they have enough information about what
[06:15] kind of exceptions that may arise whenever these method is being invoked.
[06:20] So now if you go to the ThrowsDemo, you can see here
[06:23] now my other developer who is trying to invoke this divide() method, he will check what are the possible
[06:29] exceptions that may happen here.
[06:30] And accordingly he can be well prepared.
[06:33] Maybe he will write a logic to handle these exceptions.
[06:37] For example, he can write a try block and he can move this code inside a try block.
[06:43] And similarly he can also move these System.out.println() into the try block post that he can also have
[06:49] catch block, which is going to catch two different exceptions.
[06:53] One is NumberFormatException followed by pipe symbol followed by AirthematicException.
[07:00] And after mentioning these two exceptions, I can give ex as the object reference for these two exceptions,
[07:06] and inside the catch block I can have a System.out.println() statement saying that invalid
[07:12] data provided.
[07:14] Please provide valid numbers and try again.
[07:20] So these are messages that I want to display whenever there is an exception happen inside this method.
[07:27] If I execute this program this time, you can see I'm not going to get any runtime exception because
[07:32] I handled it and I'm trying to throw an meaningful message to the end user saying that invalid data
[07:39] provided.
[07:40] Please provide valid numbers and try again.
[07:42] And with that he will go and check what is the problem here.
[07:45] And you can see there is a problem and he can correct it and post that
[07:49] if he try to execute this program, we are going to get an output which is an happy ending.
[07:54] Did you see?
[07:54] We are able to handle the both scenarios that we have discussed with the help of throws keyword.
[07:59] So always whenever you are into the scenarios where you don't want to handle a given exception, but
[08:05] you want to educate others about the potential risks that may arise whenever someone is invoking a piece
[08:11] of code.
[08:11] In such scenarios, you can always use the throws keyword as part of the method signature to mention
[08:18] the list of exceptions that may arise when a given method is being executed.
[08:23] All the details that we have discussed around the throws keyword I have mentioned in this slide for
[08:27] your reference.
[08:28] I hope you're clear.
[08:29] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

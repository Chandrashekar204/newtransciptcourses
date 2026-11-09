# 24.16 — Deep dive on Supplier interface

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Let's discuss about the sibling of Consumer which is Supplier interface, why I'm calling them as siblings.
[00:07] Just like in real life, where siblings are always going to fight with each other and they are going
[00:12] to do the exactly opposite.
[00:14] Very similarly, this supplier is going to work in exactly opposite way of Consumer.
[00:21] So what is Consumer is going to do?
[00:23] It is always going to accept the input data, but it will not return anything.
[00:28] Whereas the Supplier, it is always not going to accept any input, but it will return an output.
[00:35] You can use the Supplier in the scenarios where you want to generate a report or OTP, without accepting
[00:43] any input data.
[00:44] In all those kind of scenarios, you can happily use a Supplier interface to write the Lambda expression.
[00:50] So this Supplier interface, it has a single abstract method with the name get().
[00:56] So Supplier is like a getter method inside a Pojo class.
[01:00] So what is the purpose of getter method?
[01:02] You can always invoke the getter method to get the value from a object without passing any input.
[01:07] Similarly Consumer you can assume like a setter method.
[01:11] So what is the purpose of setter?
[01:12] Method will always pass the data to set into the object but not return anything.
[01:18] I hope that makes sense to you, but coming to the static methods and default methods, there are no
[01:23] methods available inside the Supplier functional interface.
[01:27] Obviously there is no need of chaining because the lambda expressions that we are going to write with
[01:33] the help of Supplier, they're not going to accept any input.
[01:37] With that there is no need of chaining, like you don't have to send the output from one lambda expression to
[01:42] the other lambda expression, because Supplier it is not going to accept any input data.
[01:46] So here the T indicates the return type.
[01:49] So you can write a lambda expression which is going to return any kind of data.
[01:54] But please note that it is not going to accept any input data.
[01:57] I hope you are convinced with this image
[01:59] also, like you're always going to send the data outside but not inside.
[02:03] So let's see the demo of these Functional interface very quickly.
[02:07] First let me search for Supplier inside the java.util.function package.
[02:12] Like you can see here.
[02:13] It has a single abstract method and it does not have any default and static methods.
[02:18] So let me create a new class with the name SupplierDemo.
[02:23] Inside this class I'm going to create the main() method post that I'm going to write a lambda expression,
[02:29] which is going to give me the what is the number of current month.
[02:33] So I'm going to get the output in an int format.
[02:36] That's why I'm trying to mention Supplier.
[02:38] And inside the angle brackets I'm trying to mention integer followed by I'll mention the variable name
[02:44] as get current month and the right hand side.
[02:48] Let me mention the empty parenthesis.
[02:50] Since my lambda expression, it is not going to accept any input data.
[02:54] Post that
[02:54] I'm going to mention the lambda symbol, followed by I'm going to write a business logic which is
[02:59] .
[03:00] LocalDate.now().getMOnthValue()..
[03:03] So this is going to give me the month number in an integer format.
[03:08] So now using this lambda expression, if I try to invoke the get() method I'm going to get the current
[03:14] month number the same.
[03:16] I can try to print out with the help of System.out.println().
[03:20] So if I execute this program I'm going to get the current month, which is February.
[03:24] That's why I'm getting the output as two.
[03:26] So when you execute this program based upon your current month, you're going to get the output accordingly.
[03:32] In the similar lines, let me write one more lambda expression, which is going to help me to get the
[03:37] current day of the month.
[03:39] So here I'm going to change the variable name to current day of month.
[03:44] And here, instead of getMonthValue(), I need to invoke the getDayOfMonth() method.
[03:49] So using this lambda expression, if I invoke the get() method, I'm going to get the current date, which
[03:55] is 21.
[03:56] I hope this makes sense to you.
[03:58] We're not passing any input data, but we are getting the output because we build the lambda expression
[04:03] with the help of Supplier interface.
[04:05] This time I'll write one more last lambda expression, which is going to help me to display the current
[04:11] day.
[04:12] What is the current day, whether it is Monday, Tuesday or Wednesday.
[04:15] So that's why first I'm going to type Supplier.
[04:17] And since I'm going to get the output in a String format, I'm mentioning String here, followed by
[04:23] I'll just mention the variable name as getCurrentDay name was that I'm going to write the lambda expression.
[04:31] This time the logic is LocalDate.now() followed by getDayOfWeek().
[04:39] And after invoking this getDayOfWeek(), we are going to get an enum.
[04:43] But if you're looking for the value of the day, we need to invoke the name() method.
[04:50] With this, I should be able to get the name of that day.
[04:54] So let me use the System.out.println() followed by with the lambda expression
[04:58] getCurrentDayName().
[04:59] I'm going to invoke the get() method.
[05:02] If I execute this program, we should get the output as Wednesday.
[05:05] I hope this makes sense to you.
[05:07] And you are clear with the purpose of Supplier and Consumer, you'll have lot many real projects.
[05:12] Scenarios around Supplier and Consumer.
[05:15] Always use them based upon your business scenario.
[05:18] I have a slide here explaining you the differences between the Consumer and Supplier.
[05:22] All these points we have discussed, but I'm trying to provide this slide just for your quick reference.
[05:27] So please read all these points.
[05:29] They should be pretty easy to understand.
[05:32] If you have any questions you can always post your questions inside the Q&A.
[05:35] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

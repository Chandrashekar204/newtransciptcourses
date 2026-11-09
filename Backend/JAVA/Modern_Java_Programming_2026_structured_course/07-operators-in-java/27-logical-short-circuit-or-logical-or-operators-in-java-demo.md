# 7.27 — Logical Short-Circuit OR, Logical OR operators in Java - Demo

> Section 7: Operators in Java

[00:00] Let's see the demos of OR operators inside this lecture.
[00:03] Inside the same class of LogicalOperatorsDemo.
[00:07] Just after these AND operator logic, I'm going to write a new expression.
[00:12] First, let me try to create a boolean variable with the name b post that I'm going to write num1 less
[00:20] than 10.
[00:21] So these are left hand side operand or expression, followed by
[00:25] I'm going to mention || symbols.
[00:28] After these symbols, I'm going to write an inner expression where I'm going to assign a value to the
[00:34] num2.
[00:34] The value that I want to assign here is
[00:36] maybe this time I'll try to assign a different value, which is 18.
[00:40] After assigning this value, I'm going to mention > 15.
[00:44] So do you know what is output that we are going to get from this expression?
[00:47] Let's try to evaluate the same.
[00:49] First
[00:50] this expression is going to be evaluated as true because the num1 which is 9 < 10.
[00:57] That's why it is going to be become true with that, the right hand side expression is not going to
[01:03] be evaluated by my Logical Short-circuit OR operator.
[01:08] So the overall output that we are going to get is true.
[01:11] But the num value is not going to change.
[01:14] It is going to hold the same initial value.
[01:16] So let me copy these statements and mention the same after the boolean b variable.
[01:22] And this time I'll try to print the b variable along with the num2.
[01:27] So if I try to execute this program, you can see we have true and six as an output at the end.
[01:34] So this confirms that Logical Short-circuit OR operator is not going to evaluate the right hand side
[01:41] operand, if the left hand side operand value is true.
[01:45] Whereas if you try to use a | symbol, which is an representation for Logical OR operator
[01:52] in this scenario, even though the left hand side operand is evaluated to true, still, the right hand
[01:59] side operand is going to be evaluated, and that's why we are going to get the output as 18 inside the
[02:05] num2 variable.
[02:06] So you can see we are getting the output.
[02:08] I hope you are clear with these demos.
[02:09] Please always prefer using the Logical Short-circuit OR operator only because it is going to improve
[02:17] some performance, just like how Logical Short-circuit AND operator is going to provide.
[02:22] And here you may have some burning question which is what are the real project scenarios where I should
[02:28] use this AND operators or OR operators?
[02:31] Let me give you some business scenario examples.
[02:33] Think like you are building a business logic using the Java program as part of the business requirements
[02:39] the condition mentioned is that a person should be an adult, and he should be also staying in the city
[02:46] New York.
[02:47] In such scenarios, you will write the business logic such a way that first, on the left hand side,
[02:51] you're going to check if the person age is greater than 18, and on the right hand side you're going
[02:57] to check the person
[02:59] City address is New York.
[03:01] If both of these checks are true, then you're going to execute a piece of business logic,
[03:05] otherwise you're going to execute another piece of logic or you're not going to do anything.
[03:11] Now coming to the OR operators, you may have a business requirement, which is the person he can stay
[03:17] in a New York City or he can stay in London City.
[03:21] So in such scenarios, you can use an OR operator if the person staying city is in the New York or
[03:29] if the person staying city is in the London, then you are going to execute some piece of logic.
[03:34] Otherwise you're going to execute another piece of logic or you're not going to do anything.
[03:39] So for these kind of scenarios only, we are going to use the logical operators in Java.
[03:45] While using these logical operators, you need to be very careful instead of OR operator
[03:50] if you use AND operator the meaning of your business, logic is going to change drastically.
[03:57] I can also show you some funny images around this.
[04:00] Here you can see someone used an AND operator instead of OR operator.
[04:06] That's why you can see when they tried to open that door of the car, both doors are opening.
[04:11] So this is one funny representation.
[04:14] And what is going to happen if you end up using a wrong logical operator?
[04:19] And understanding your requirements also is very important while you are trying to use these logical
[04:25] operators.
[04:26] For example, here you can see a girlfriend telling to his boyfriend saying that please go to the supermarket
[04:33] and get a carton of milk if they have avocados, also get six.
[04:39] So here the requirement
[04:40] Obviously it is not pretty clear.
[04:42] So the boyfriend understand the requirement in a wrong way.
[04:47] So what he has done is he bought six cartons of milk because his girlfriend said if they have avocados
[04:54] get six.
[04:55] So the requirements are not pretty clear.
[04:57] So these kind of miscommunications.
[04:59] Always happen in real projects as well.
[05:02] So always ask your business analyst and client if something is not clear for you.
[05:07] Otherwise you will end up into the funny scenarios like this.
[05:11] I hope you are enjoying the course.
[05:13] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

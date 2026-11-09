# 24.17 — Deep dive on BiFunctional Interfaces - Part 1

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Let's talk about BiFunctional interfaces.
[00:03] So what are these BiFunctional interfaces?
[00:06] Before I try to explain about these BiFunctional interfaces, let me highlight you that as of now,
[00:11] all the functional interfaces that we have discussed so far, they only accept a single input parameter.
[00:19] exceept a Supplier
[00:20] all the functional interfaces that we have discussed so far, they accept a single input data type.
[00:25] If you have these kind of requirements where you want to accept two input parameters, then you can't
[00:30] build the lambda expressions with the functional interfaces that we have discussed so far.
[00:34] To overcome this challenge, what Java team they have done is they have introduced BiFunctional interfaces
[00:41] under these BiFunctional interfaces
[00:44] they have various functional interfaces which which are equivalent to Predicate, Consumer, UnaryOperator
[00:50] and Function interface.
[00:52] So let's try to understand about them one by one.
[00:54] The very first BiFunctional interface that we have is by Predicate.
[00:58] We know the purpose of Predicate is to accept a single input parameter and return a boolean value.
[01:03] But if you are looking for an option where you want to accept two input parameters of any data type
[01:09] and return the boolean as an output.
[01:11] In such scenarios, you can use the BiPredicate functional interface to develop your lambda expression.
[01:19] So here T and U represents that type of the input parameters that you are by predicate is going to accept.
[01:26] After Predicate,
[01:27] we discussed about Function interface.
[01:30] Since Function interface it is only going to accept and process a single input parameter.
[01:35] To handle the scenarios of accepting two different input parameters we have BiFunction.
[01:41] So BiFunction it is going to accept T and U as an input data types, and R represents the return type
[01:49] of the BiFunction.
[01:51] In the case of Predicate, since always the boolean is the output, there is no need of third type inside
[01:56] the generics, but coming to the by function, since we are going to return any kind of data type as
[02:01] an output.
[02:02] That's why representing the return type, we have the R type here inside the generics.
[02:07] As a next step, let's try to understand BiConsumer.
[02:10] So what is the purpose of Consumer.
[02:12] Consumer is going to accept a single input parameter and process it.
[02:16] And it is not going to return anything on the similar lines we have by Consumer, which is capable of
[02:22] accepting two input parameters of type T and U, and it is not going to return anything similar to Consumer.
[02:30] I hope this makes sense.
[02:31] Now I have a tricky question for you.
[02:32] Do you think we need a BiSupplier just like how we have Supplier?
[02:36] Think about it.
[02:37] If Supplier is going to accept any input parameter, off course not.
[02:41] Then if it is not accepting any input parameter, then there is no meaning of building BiSupplier which
[02:47] is capable of accepting two different type of parameters.
[02:51] That's why there is no BiSupplier corresponding to the Supplier functional interface.
[02:56] Due to the reason that Supplier is not going to accept any input parameters.
[03:00] At last we have binary operator which is a child of BiFunction, just like how we are going to use
[03:06] UnaryOperator in the scenarios where you are input and return type is of type same data type.
[03:11] Very similarly, you can use a BinaryOperator in the scenarios where your two input parameters and
[03:18] the return type
[03:19] all of them belongs to the same data type.
[03:21] So this BinaryOperator, it is going to inherit all the methods from the BiFunction.
[03:26] On top of that, it is also going to have two utility static methods, which is going to help us to
[03:32] identify the maximum or minimum of two elements based upon the comparator logic that we are going to
[03:39] define inside the lambda expression.
[03:41] So these are the two static methods minBy and maxBy.
[03:44] So let's see the demo of all these BiFunctional interfaces very quickly. Here you can see inside that
[03:50] java.util.function package.
[03:52] These are the four BiFunctional interfaces available BiConsumer, BiFunction, BinaryOperator and
[03:59] BiPredicate.
[03:59] To show you the demo around these BiFunctional interfaces.
[04:03] What I'm going to do is I'm going to create a new Java class with the name BiFunctionsDemo.
[04:11] Inside this class I'm going to create a main() method.
[04:15] First using the BiFredicate I want to build a lambda expression.
[04:19] Think like
[04:19] I have a scenario where I want to accept to two input values, these two into values.
[04:25] I want to perform the addition, and once the addition is performed, I want to verify whether the sum
[04:31] value is a even number or not.
[04:33] So this can be a perfect scenario for BiPredicate.
[04:35] That's why I'm trying to type a BiPredicate here, followed by
[04:40] I'll try to mention both the input parameter types as Integer, Integer with the variable name
[04:47] isSumEven.
[04:48] Post that since I'm trying to accept a two input parameters, the parentheses are mandatory.
[04:55] So let me mention the parameter names as num1,
[04:58] num2.
[05:00] Followed by lambda symbol, followed by first I'm going to perform the addition operation
[05:07] num1 + num2.
[05:07] This addition operation value I'll try to surround it by parenthesis, followed by I'll try to write
[05:13] a logic, which is if the sum is exactly divisible by two, then I can assume it is an even number.
[05:20] So the outcome from these expression we are going to get as an boolean.
[05:24] So let me use
[05:25] this isSumEven and invoke the abstract method which is test().
[05:31] And to this test() method I can pass input values like four and nine.
[05:36] So the output from this we can expect as false.
[05:39] So let me confirm the same by printing the output with the help of System.out.println().
[05:45] So if I execute this I'm going to get the output as false because nine plus four is 13 and 13 is not
[05:52] a even number.
[05:53] Let me mention inside the comments as well.
[05:55] What will be the output here?
[05:56] As a next step, let's see the demo off BiFunction.
[06:00] So BiFunction is capable of accepting two input parameters.
[06:03] And it is also capable of returning any data type as an output.
[06:07] This time my requirement is I want to pass two different int values, and I want to calculate the power
[06:13] based upon the two input values that I'm trying to share.
[06:16] For example, if I pass two and three as an input, I want to get the output as two power three, which
[06:23] is eight.
[06:24] Similarly, if I pass five comma two, I want to get the output as five power two, which is 25.
[06:31] So this is my requirement.
[06:32] So since this is a mathematical related operation, we have a utility class with the name Math inside
[06:39] the java.lang package.
[06:41] Inside this class we have a method with the name pow().
[06:44] pow() means power.
[06:45] So it is going to accept two doubles as an input, and it is also going to return a double as an output.
[06:52] So based upon these I can write my lambda expression.
[06:55] So let me go to my BiFunctionsDemo here.
[06:58] First I'm going to create a variable off BiFunction to this by function I'm going to mention double
[07:06] as the data type in all the places.
[07:10] So once I have mentioned this double in three places, I can mention the variable name as calculate
[07:16] power.
[07:17] And after this I'm going to write a lambda expression which is num1, num2, followed by I'll
[07:24] invoke the Math.pow().
[07:27] And to this I'm going to pass num1, num2.
[07:31] So this is a simple logic that I have written.
[07:33] Now using these calculate power.
[07:36] Let me invoke the apply() method to this
[07:39] let me pass the input as 2.0, 3.0.
[07:43] So the output from these apply() method I can try to print out with the help of System.out.println().
[07:49] So let me execute this program and you can see I'm going to get the output 8.0.
[07:55] I hope this makes sense to you.
[07:56] Now let me show you the demo off BiConsumer.
[07:59] This time my requirement is if I pass two different String object values my BiFunction lambda, it
[08:05] has to append both these String objects and convert them into a uppercase value.
[08:10] So once the String data is converted into the uppercase, I want to print the same onto the console.
[08:15] Here we want to send the two String objects as an input, and we are not expecting anything as an output.
[08:21] That's why we should be able to happily use BiConsumer with the data types like String, String,
[08:29] and the variable name
[08:30] I'll just mention appendAndConvert and the right hand side
[08:34] let me mention word1, word2 as a parameter names followed by
[08:42] after the lambda symbol, I'm going to write a logic which is System.out.println().
[08:47] To this println() method, I'm going to pass word1 + word2 and the output from this word1
[08:55] and word2
[08:56] I want to convert into uppercase values, so that's why I'll try to surround these with the parentheses
[09:02] followed by
[09:02] I'm going to invoke the toUppercase() method.
[09:05] I hope this makes sense.
[09:06] If needed, I can try to bring this down to next line so that it is going to be visible to you.
[09:12] Now using these append and convert I'm going to invoke the accept() method.
[09:17] To this accept() method I pass a couple of words which are like Hello space and the second word is Eazy
[09:26] Eazy Bytes.
[09:28] So if I execute this program, you can expect I'm going to get the output as Hello Eazy Bytes
[09:33] in the similar lines
[09:35] this time I can try to append the two different words and print the length of them.
[09:40] So it is going to be super easy.
[09:42] Let me copy these lines of code this time.
[09:45] Since we are trying to print the length, what we can do is, we can mention the variable name as append
[09:50] and length as the variable name.
[09:53] After this inside the System.out.println(), just in the place of invoking two uppercase, we can invoke
[09:59] the
[09:59] length() method.
[10:00] Before I try to execute this program, I need to make sure I'm replacing this variable name here and
[10:06] post that I'm going to execute this.
[10:07] You can see I'm getting the output as 16 like we expect.
[10:11] I hope this makes sense to you.
[10:12] Let's see the demo of binary operator in the next lecture.
[10:16] Thank you,
[10:17] bye.

----------------------------------------

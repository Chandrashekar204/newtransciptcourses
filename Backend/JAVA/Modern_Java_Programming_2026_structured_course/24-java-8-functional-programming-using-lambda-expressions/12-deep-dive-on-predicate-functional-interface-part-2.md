# 24.12 — Deep dive on Predicate functional interface - Part 2

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Let me show you the demo of negate() default method available inside the Predicate function interface.
[00:05] Using the negate() default method, we should be able to negate the output.
[00:12] What is the negation operation?
[00:13] If you give true as an input, you're going to get the output as false and vice versa.
[00:18] So what I'm going to do is first I'll try to type System.out.println(), post that using the
[00:24] isEven predicate, I'm going to invoke the negate() method, and after mentioning the negate, I'm going
[00:30] to invoke that test() method.
[00:32] And to this test() method I'm going to pass the input as 63.
[00:36] So since my 63 is not an even number, I'm going to get the output as false from these isEven predicate
[00:43] condition.
[00:44] But since we are trying to apply the negate, the overall output we are going to get is true.
[00:50] So if I try to execute this program at the end, you can see I'm getting the output as true as a next
[00:55] step.
[00:55] Let's see the demo of not() static method. To invoke the not() static method
[01:01] first we need to type the interface name which is Predicate, followed by
[01:05] I'm going to invoke the not() static method. To this not() static method
[01:09] I'm trying to pass the isEven predicate.
[01:12] Basically, what is going to happen with this code is whatever condition you have written inside this
[01:17] isEven, it is going to be negated and you're going to get a new predicate representing the negative
[01:24] effect of your isEven lambda expression.
[01:27] So on the left hand side, I can catch a new predicate with the generic element as integer and with
[01:34] the predicate name isOdd.
[01:36] So if I try to use these isArt to test the whether a given number is odd or not, I'm going to get
[01:44] the output as true.
[01:45] I can try to confirm the same by printing the output onto the console.
[01:50] So if I execute this program, I should get that true at the end.
[01:54] You can see I'm getting that true, whereas if I try to send the input as four, I'm going to get the
[02:00] output as false.
[02:02] So what happened here is to this not() method, we have provided a predicate condition, and the behavior
[02:07] of the given input predicate condition is going to be negated.
[02:11] And we are going to get a new predicate negated condition on the left hand side.
[02:16] That's why when I use this, I'm getting the output as false with the input value as four.
[02:21] Similarly, let's try to evaluate the ease equal static method available inside the Predicate interface.
[02:29] So let me invoke isEqual() static method.
[02:32] So what is this isEqual() method is going to do behind the scenes.
[02:35] It is going to compare two different objects with the help of equals() method.
[02:40] And accordingly it is going to give the output as true or false.
[02:44] So first I need to provide what is my object to one to this isEqual() method.
[02:49] So here I'm trying to pass a String object with the content as Easy,Bytes.
[02:55] So this is my first object.
[02:57] Using these first object I'm going to get a new predicate which is capable of handling the String objects,
[03:06] because I'm trying to provide the String as an input to these isEqual() method post that I'm going
[03:11] to give a name to my predicate condition, which is check equality.
[03:15] Now you can see I have a checkEquality predicate condition, which is always going to compare a given
[03:21] input object with these object, which is Eazy Bytes.
[03:25] So how to test this?
[03:26] First let me type System.out.println().
[03:29] Now using this checkedEquality, I'm going to invoke that test() method and to this test() method I can
[03:35] pass a String which is modern.
[03:37] So basically this test() method behind the scenes it is going to compare these two objects using the equals()
[03:44] method.
[03:44] Since these two objects are not same I'm going to get the output as false.
[03:49] So you can see I'm getting the output as false.
[03:51] Whereas if I try to mention the same String which is Eazy Bytes, I'm going to get the output
[03:58] as true.
[03:59] I hope you are seeing the purpose of these static methods provided inside the Predicate functional interface.
[04:04] Before I try to close this lecture, let me show you a real life scenario where we are going to use
[04:09] the predicate a lot.
[04:11] For the same, I'm going to create an list object with the help of ArraysAsList() method.
[04:17] To this method, I'm going to pass various int elements like 1, 2, 3, 4, 5, 6,
[04:23] followed by 6, 8, 9, 10.
[04:26] Basically, I'm trying to build a list object which has elements from 1 to 10.
[04:33] Now I'm going to write a small piece of code, which is going to help me to filter the even numbers
[04:39] from this list.
[04:40] So to filter the even numbers, first I need to invoke the stream() method available inside the List object.
[04:47] Where to discuss about the stream().
[04:48] But don't worry, we are going to discuss this in future.
[04:52] After this stream() method, I can invoke one of the existing method which is filter().
[04:57] You can see this filter() is expected.
[05:00] A lambda expression based upon a predicate value.
[05:03] So what is the purpose of filter()?
[05:04] You are going to give an input to the filter(), and it's going to tell whether the output is true or
[05:10] false.
[05:10] So based upon your output the elements they are going to be filtered.
[05:14] So here to this filter() method I can pass a lambda expression which is isEven that we have written
[05:20] in the top.
[05:21] So what is the purpose of this isEven.
[05:23] It is going to check whether a given input number is a even number or not.
[05:27] So behind the scenes this filter() method, it is going to invoke this lambda expression for each of the
[05:33] element that I have inside my list.
[05:35] And at last I want to invoke the collect() method. To this collect() method
[05:40] I want to pass Collectors.toList() as an input.
[05:45] So with this .collect() method, we are trying to collect the list of even numbers into a new list.
[05:51] That's why on the left hand side, let me type list of integer with the variable name as evenList.
[05:59] And at last I can try to print out these evenList.
[06:02] So if I execute this program, you can see I'm going to get only the even numbers.
[06:07] So are you seeing the power of lambda expressions?
[06:10] If you try to combine these lambda expressions with the streams and the collections, you can write
[06:15] any complex of code with a breeze.
[06:18] So here you can see this is looking like a requirement.
[06:21] So someone is saying I'm going to get a stream of data. From this stream of data
[06:26] I want to filter few elements based upon these lambda expression.
[06:30] And at last I want to collect the output.
[06:32] So this kind of code more look like a requirement.
[06:36] Now where I am providing low level instructions like iterating the list of elements, checking each
[06:42] element, using the if condition, and collecting all the elements into a new collection.
[06:47] I'm not given all such instructions.
[06:49] Simply, I'm trying to use the lambda expressions along with the stream API.
[06:54] With that, I'm able to achieve my output with a single line of code, whereas with the imperative approach
[07:00] you need to write at least ten lines of code, you're going to see more and more power of lambda expressions
[07:05] in the coming lectures when we start discussing about the streams API.
[07:09] But before that, I want you to focus on Functional interface and try to master lambda expressions.
[07:15] I hope this makes sense to you.
[07:17] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

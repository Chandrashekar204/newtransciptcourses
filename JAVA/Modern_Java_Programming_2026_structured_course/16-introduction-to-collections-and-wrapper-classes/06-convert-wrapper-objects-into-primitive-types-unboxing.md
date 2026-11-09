# 16.6 — Convert Wrapper Objects into Primitive Types (Unboxing)

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] Do you know what is the Newton's third law?
[00:02] Newton's third law says for every action there is an equal and opposite reaction.
[00:09] You might be scratching your head if you have attended a wrong class, because I'm trying to teach right
[00:15] now
[00:15] physics.
[00:15] Don't worry, I'm trying to refer these
[00:17] Newton's third law, just as an example to convey that just like how we are trying to perform the boxing,
[00:25] sometimes we will also have to perform the unboxing.
[00:28] So what is a boxing?
[00:30] Boxing is a process of wrapping our primitive values into an wrapper class object on the similar line
[00:37] sometimes we may have to perform the exactly opposite of boxing, which is unboxing.
[00:42] We want to convert our wrapper class object into a primitive data type value.
[00:48] Let's try to understand how to perform the unboxing in Java with the help of wrapper classes.
[00:54] For the same, I'm going to copy the same class inside the same package, but this time I'm going to
[01:00] mention the class name as UnboxingDemo.
[01:04] Inside this class, let me remove some unnecessary code.
[01:07] I'm going to retain the code related to valueOf() only, so you can see with the help of valueOf() method
[01:13] we are trying to perform the boxing.
[01:15] Now I'm going to show you how to perform the unboxing by taking these wrapper objects as an input.
[01:21] Think like I want to unwrap the data that I stored inside this integer1 object.
[01:27] So how to do that?
[01:28] It's very simple.
[01:29] Using the same object, we can invoke the instance method available inside the Integer wrapper class,
[01:36] which is intValue().
[01:38] When you invoke this intValue() method, the return type from this method, you're going to get the actual
[01:44] data in the format of primitive data type value.
[01:47] So that's why I'm going to catch that data.
[01:50] And the left hand side with the variable name as num1.
[01:53] Similarly, let's try to do the same for other wrapper class objects like for doubleObj1.
[01:59] I need to invoke the doubleValue() method.
[02:02] It's not the int value always this int double, they are going to be replaced with the corresponding
[02:09] primitive data type name.
[02:10] Here on the left hand side, I'm going to create a variable name which is double num2.
[02:16] The output from this doubleValue() method I'm going to assign to these num2 variable. Very similarly,
[02:21] this time with the help of these longObj1, I'm going to invoke the method which is longValue().
[02:29] So the output from this longValue() method we need to catch on the left hand side with the primitive
[02:35] data type variable, which is long.
[02:37] The variable name I'm going to mention as num3.
[02:40] At last I can try to print out all these num1 and num2, num3 into the console, so that we can confirm
[02:48] we are able to see the same values that we have inside our wrapper objects.
[02:52] So let me execute this program.
[02:54] You can see we are getting the same values that we initially use to wrap them inside the wrapper objects.
[03:02] So what is this process?
[03:03] This process we call them as Unboxing.
[03:06] So to perform the Unboxing always use the corresponding instance methods available inside the wrapper
[03:12] class like intValue(), doubleValue(), longValue(), floatValue(), shortValue(), byteValue().
[03:18] Whereas for the boxing you should always use the value of static method available inside your wrapper
[03:25] class.
[03:26] Maybe to make it more clear for you.
[03:28] I can mention some comments here saying that this is boxing.
[03:32] Similarly, I can try to mention one more comment here saying that this process is unboxing so very
[03:40] similarly inside the BoxingDemo.
[03:42] Also I can mention these process as parsing.
[03:46] So whatever we are trying to do with the help of parse related methods, we can call that as parsing,
[03:52] because we are trying to convert a String value into its corresponding primitive data type value.
[03:58] I hope you are clear.
[03:59] Whatever we have discussed around unboxing all the details along with the code example I have mentioned
[04:07] inside this slide for your reference.
[04:09] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

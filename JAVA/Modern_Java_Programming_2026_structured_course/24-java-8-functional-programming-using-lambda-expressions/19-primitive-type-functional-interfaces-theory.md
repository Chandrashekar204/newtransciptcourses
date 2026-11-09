# 24.19 — Primitive Type functional interfaces - Theory

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Inside this lecture, let's try to discuss about the last set of functional interfaces, which are primitive
[00:06] type functional interfaces.
[00:08] So what are these interfaces?
[00:10] What is the purpose of them.
[00:11] This might be your question.
[00:12] So let's try to understand the same.
[00:14] All the functional interfaces that we have discussed so far like predicate function, consumer or by
[00:19] functional interfaces, they are going to accept or return only the object type values like integer,
[00:26] double, float and long.
[00:28] So these are all the wrapper class representation of the primitive data types.
[00:32] If you have a scenario where you want to build a lambda expression with the help of these function interfaces
[00:38] like predicate function consumer, which is going to accept the primitive data type values, then you're
[00:44] going to have a serious performance problem, because whenever we pass a primitive input value like
[00:50] int long double float behind the scenes, Java is going to perform the auto boxing where it is going
[00:56] to convert this primitive data type to the wrapper objects.
[00:59] And similarly, once the logic is being executed, Java has to convert them back to the primitive types
[01:05] using unboxing.
[01:07] So think like you have implemented a lambda expression with the help of function interface.
[01:13] So this function interface, it's supposed to accept the int value as an input and post that inside
[01:19] the business logic, the lambda expression, it is going to multiply it with the two and return the
[01:25] new value as an output.
[01:27] So in this scenario, it is pretty simple that we are dealing with the inter primitive value.
[01:31] But we know the drawback with the function is it is only going to accept the input and return the output
[01:37] in the form of integer wrapper object.
[01:40] That's why behind the scenes all these autoboxing and unboxing is going to happen.
[01:45] Since there is going to be lot of autoboxing and unboxing is going to happen, it may impact performance,
[01:52] especially in the scenarios where you're trying to feed your lambda expression for the millions of elements
[01:58] present inside a stream or a collection.
[02:01] So in those kind of scenarios, you will see a performance issue if you leverage the function interfaces
[02:08] that we have discussed so far.
[02:09] That's why whenever you have a scenario where you are dealing with the primitive data type values as
[02:14] an input or output, in all such scenarios, you can use the primitive type of functional interfaces.
[02:20] There are good amount of interfaces under this category.
[02:24] So let's try to understand what are those.
[02:26] You can see the very first function interface that we have is inter predicate.
[02:30] We know the return type from the predicate is always boolean.
[02:34] So they should not be any confusion around this.
[02:36] But coming to the input parameter, if you have a scenario where you want to accept the input value
[02:43] with the primitive data type int.
[02:45] In such scenarios, you can use the inter predicate to build the lambda expression.
[02:51] Similarly, if you are looking for a double as an input parameter, you can leverage the double predicate
[02:57] followed by long predicate.
[02:58] If you have a scenario where you want to accept the long as an input value, let me show you one of
[03:04] these predicate functional interfaces inside Intellige.
[03:08] Here I'm going to search for inter predicate.
[03:11] If I can open.
[03:12] You can see this time it is accepting the input parameter as primitive data type, which is int.
[03:18] With that there won't be any auto boxing required.
[03:22] Whereas if you look for the normal predicate interface, it is going to accept the input in the form
[03:29] of object.
[03:30] So that's why we will be forced to mention integer wrapper class whenever we are trying to define a
[03:36] lambda expression with the help of this predicate.
[03:38] But if you know that you're going to accept the inter primitive data type as an input, please use this
[03:44] int predicate or double predicate or long predicate based upon your requirements.
[03:49] After predicate, we have function related functional interfaces.
[03:53] So you can see here we have a function interface with the name into function.
[03:57] If you are working on a scenario where your function has to accept the inter primitive value as an input,
[04:03] and the return type can be any object data type.
[04:06] In such scenarios, you can use these inter function.
[04:09] In the similar lines we have double function long function, which is going to accept double and long
[04:15] as an input values, but the return type can be defined based upon.
[04:19] These are type that we have inside the generic tags.
[04:22] If you are looking for vice versa scenario where you want to accept some object as an input, but the
[04:28] return type should be an int.
[04:31] In such scenarios you can use that to into functions.
[04:34] Here the t represent the input data type, whereas the output is always going to be the inter primitive
[04:40] data type.
[04:41] And the similar lines we have two double function, which is going to return that double as an output
[04:45] by accepting any data type as an input.
[04:48] Similarly, we have two long function which is going to return the long as an output.
[04:53] After these two long function, we have into two long function.
[04:57] So if you are working on a scenario where.
[05:00] Your method parameter has weakly into primitive data type and the output data type should be long,
[05:06] then you can use this into two long function.
[05:09] Similarly, we have into two double function where into primitive data type is going to be the input
[05:14] and double is going to be the output data type.
[05:17] So with this you're going to avoid a lot of autoboxing and unboxing which will save your code from performance
[05:24] issues.
[05:24] Most of these function interface names are self-explanatory.
[05:28] If you see here we have long two int.
[05:30] That means the input parameter is going to be long primitive data type, but the output is going to
[05:36] be int.
[05:36] Let me go to the next slide.
[05:38] Here we have long two double which is going to accept long as an input.
[05:43] And the output is going to be return in the form of double.
[05:45] So this is the abstract method name which is apply as double.
[05:49] Similarly there is a double to int which is going to accept double as an input and return into primitive
[05:54] data type as an output.
[05:56] Next we have double to long, which is going to accept double as an input, and it is going to return
[06:01] long as an output.
[06:03] Now, coming to the by function, if you are working on a scenario where you are going to accept to
[06:08] two input parameters of any object type like t and U, but the output you are always expecting in an
[06:16] inter primitive data type.
[06:17] Then you can use these two int by function.
[06:20] So here you can see the input is of type t and u.
[06:24] But the output is a primitive data type which is int.
[06:27] In similar lines we have to use long by function to being to return linstant and two double by to create
[06:33] function, which is good return double.
[06:35] Now instance to the consumer we know consumer enum going to return error clapping.
[06:40] It is always going to accept the input.
[06:42] So other than if you are working on a side where your consumer type is going to accept a primitive data
[06:47] type previously, then instead of you cannot normal object or functional interterm data can happily
[06:52] use what is a inter consumer.
[06:54] You can see it is accepting inter primitive input as an input so that the similar line.
[06:59] We have a question consumer, which is going to accept the long as adding more input data type.
[07:03] In our next we also have data consumer which is side accept the inter as an input parameter.
[07:09] And I'm working on a scenario.
[07:11] We can one of the input to a meter to your class is going to be of any data type.
[07:16] When it has, the other polesitter is always going to be inter primitive to class type.
[07:21] In such cases you can use these each object into consumer.
[07:25] So here the T indicates what is the data type of your as an parameter.
[07:29] So same we have obj type consumer really good.
[07:33] The second parameter objects is going to be data type.
[07:35] And we also have obj double consumer where the second meter is always going to be double.
[07:41] Now lastly to the supplier object or primitive type.
[07:44] Since interfaces you can going to I have an behind supplier which can always going to give the struct
[07:50] as an output.
[07:51] So here it is.
[07:52] I hope to data type by.
[07:53] Let's see if lambda expression.
[07:54] With the close of this abstract message, we can avoid the auto unboxing performance related issues
[08:01] in the similar lines, we also have long supplier double supplier, boolean supplier where they are
[08:06] going to return primitive data types like long, double and boolean after supplier.
[08:10] We can explore the unary operator related functional interfaces like you can see here.
[08:15] If you have a scenario where you want your unary operator to accept inter primitive data type, and
[08:21] the return type also is going to be inter primitive data type, then you can happily use these int unary
[08:27] operator.
[08:28] You can see both on the input side and on the output side.
[08:31] We have primitive data type which is int.
[08:34] In the similar lines we have long unary operator where on the input side and on the output side it is
[08:40] going to be long.
[08:41] Similarly, we have double unary operator, where double primitive data type is going to be used as
[08:47] an input and output.
[08:49] As a last step, let's try to explore the binary operator related functional interfaces.
[08:54] If you have a scenario where both the input parameters to your binary operator is of type int and the
[09:01] return type also is going to be int, you can happily use into binary operator, whereas if you are
[09:07] dealing with the long primitive data type, you can use long binary operator or double binary operator.
[09:13] In the scenarios where you are dealing with the double primitive data type.
[09:17] So these are all the primitive type functional interfaces which you need to use to build the lambda
[09:22] expressions.
[09:22] Whenever you are dealing with the primitive data types as an input or as an output.
[09:28] So all these functional interfaces you should be able to identify inside the same package.
[09:33] You can see these are all the functional interfaces that we have discussed so far.
[09:37] Anytime.
[09:38] If you have any question, you can always read that documentation of that particular function interface.
[09:43] Then it is going to be super clear for you.
[09:45] I hope you are clear with this theory discussion.
[09:48] I'll show you the demo of these function interfaces very quickly.
[09:51] Thank you and I'll catch you in the next lecture by.

----------------------------------------

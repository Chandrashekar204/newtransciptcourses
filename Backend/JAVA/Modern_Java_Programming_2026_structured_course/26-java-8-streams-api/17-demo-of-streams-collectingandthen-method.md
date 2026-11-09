# 26.17 — Demo of Streams collectingAndThen() method

> Section 26: [JAVA 8] Streams API

[00:00] Just like how we have collective terminal operation.
[00:03] We also have another terminal operation with the name collecting.
[00:08] And then the name itself is very catchy and self-explanatory.
[00:12] We need to use this terminal operation in the scenarios where you want to collect the elements inside
[00:17] a stream object.
[00:19] Once the collection is completed, you want to perform some other operation.
[00:24] In all such scenarios, you can use these collecting and then terminal operation.
[00:29] So here you can see I also highlighted its first argument is a collector that collects the data from
[00:36] the stream.
[00:36] This is going to work very similar to the collector that we have discussed in the previous lecture.
[00:40] But coming to the second argument, we can call this as a finisher, which is a lambda expression built
[00:46] based upon the function functional interfaces.
[00:49] The finisher is passed as a result.
[00:51] So this result we are going to get from the first collector that we have defined as a first argument.
[00:56] So the same result can be modified based upon the lambda expression that we have provided as the second
[01:03] argument.
[01:03] So the return type of these collecting and then is always going to be the return type of the finisher.
[01:09] So here I also provided it is going to accept two parameters.
[01:12] The first parameter is the instance of collector.
[01:15] In other words, any collector can be used here.
[01:18] It can be two list or two map or two set, or it can be counting, or it can be min by max by.
[01:24] As long as it is a type of collector, it should work as a very first parameter to this collecting.
[01:30] And then.
[01:31] But coming to the second parameter, which is a finisher, like I said, we need to pass a lambda expression
[01:36] implementing the function functional interface.
[01:39] So here I have an example.
[01:41] This example may look very complex to you.
[01:44] First, let me give you a high level introduction about this example.
[01:47] First that we can try to implement this inside interface.
[01:50] During the same process we can try to discuss in detail.
[01:53] You can see here.
[01:54] First I have a list object that is going to store product Objects.
[01:59] I tried to create various product objects like Apple, Samsung, Nokia, BlackBerry, Apple Pro Max,
[02:06] mi, and OnePlus.
[02:07] So these are all the mobile products, the product object it is going to have, what is the product
[02:12] name and what is the price of it?
[02:13] Now, using this product list object, I'm trying to get the stream object by invoking the stream method,
[02:19] followed by I'm trying to invoke that terminal operation which is collect.
[02:23] We should not invoke the collecting, and then we should invoke the same terminal operation like we
[02:28] discussed in the previous lecture.
[02:29] It is going to be collect, but when we are trying to pass the input to this collect, we need to invoke
[02:35] this method which is collecting and then method available inside the collectors.
[02:40] To this method we need to pass two parameters.
[02:43] One is on how to collect the result.
[02:45] Once the result is collected, and the same result is going to be passed as an input to the second parameter
[02:50] that we have provided here.
[02:52] So basically what I'm trying to do here is first I'm trying to identify what is the product which has
[02:57] a highest price.
[02:59] The same I'm trying to achieve with the help of first parameter.
[03:02] Now, with the help of second parameter, I have written a logic which is if there is a product with
[03:09] the highest price available, I'm just trying to send its name to the output, otherwise I'll send the
[03:14] output as none.
[03:15] At last I'm going to print the what is the name of the product which has highest price.
[03:21] So this is my business problem, which I'm trying to solve here with the help of collecting and then
[03:26] terminal operation.
[03:27] So let's see the demo so that if something is not clear we discuss in detail inside IntelliJ.
[03:32] Inside IntelliJ.
[03:33] First I'm going to create a Pojo class with the name product.
[03:37] And inside this product I'm going to create couple of private fields with the field name as name, followed
[03:45] by the second field I'm going to mention as price.
[03:49] Now as a next step I'm going to generate the constructor by using these two fields, followed by I'm
[03:57] going to generate only the getters.
[03:59] Let me generate the getters for these two fields.
[04:02] I don't want to generate the setters because I'm always going to update the data with the help of constructor.
[04:07] Now we have our Pojo class ready.
[04:09] As a next step, let's try to create a list object which is capable of storing the objects of product.
[04:15] So here I'm going to create a new class with the name stream collecting and then demo.
[04:23] So first let me create the main method followed by I'm going to create a list object that is capable
[04:30] of storing list of products.
[04:32] So let me mention the name as product list.
[04:36] Now on the right hand side with the help of arrays dot as list, I'll try to pass multiple objects of
[04:43] product like new product and the very first product name I'm going to mention as Apple, followed by
[04:49] the price I'm going to mention as 1200.
[04:51] So this way I want to pass multiple object to details.
[04:56] So let me mention multiple objects.
[04:59] So as of now I have three objects.
[05:01] Let me mention fourth, followed by fifth followed by six followed by seventh.
[05:06] So these are the all the product objects.
[05:08] But as of now they all have the same name and price.
[05:10] Let me correct one by one.
[05:12] I'll try to correct all these product names and prices behind the scenes, just to save some time behind
[05:18] the scenes, I have corrected all the product names and price details.
[05:21] So now using this product list object, I want to invoke the stream method.
[05:27] Once the stream object is available, I want to invoke the collect method.
[05:31] You can see there is no terminal operation with the name collecting, and then instead we should use
[05:38] the same operation which is collect and as an input to this collect terminal operation, we need to
[05:45] pass the input which is collectors dot collecting.
[05:49] And then so there is a static method with the name collecting.
[05:52] And then inside the collector.
[05:54] So let me open this.
[05:55] So this is accepting two input parameters.
[05:58] One is of type collector and the other one is of type function.
[06:02] Here you can also see they gave one example as well.
[06:05] First they have a people collection object using the same.
[06:08] They are trying to invoke the stream method.
[06:10] After that they are trying to invoke the collect and to this collecting.
[06:14] And then they are first trying to pass the two list as an input, followed by the second parameter.
[06:20] They're trying to pass the lambda expression with the help of method reference.
[06:25] So inside collections we have Unmodifiable list method which is going to create a new list which cannot
[06:32] be modified.
[06:33] So this is one example of collecting.
[06:35] And then but inside our example we are trying to solve some other problem.
[06:39] That's why we are going to write different logic based upon our requirements.
[06:43] My very first requirement is to identify the product which has the maximum price for the same as a first
[06:50] parameter.
[06:51] I'm going to send the logic with the help of collectors dot max buy.
[06:57] So in the previous lecture I was telling there is a collector operation with the name Max.
[07:01] Buy.
[07:02] To this Max buy.
[07:03] We need to send the comparator logic to identify the element which has a maximum value to provide the
[07:09] comparator logic.
[07:10] What I'm going to do is I'll just take the help of comparator class.
[07:13] And inside this we have a method with the name comparing.
[07:17] So this method it is going to ask you to provide a lambda expression on how to perform the comparison.
[07:24] So here they also gave an example.
[07:26] If you are looking to compare person objects based upon the person last name, then this is how we need
[07:31] to use it like comparator dot.
[07:33] Comparing and to this comparing method, we need to provide a lambda expression with the help of method
[07:37] reference.
[07:38] The same I'll try to do here to this comparing.
[07:41] I'll try to provide method reference with the help of product colon colon followed by get price because
[07:47] we want to perform the comparison based upon the price.
[07:50] So with this comparison my collector it is going to identify what is the element which has a maximum
[07:56] price.
[07:57] Now, as a next step, I want to provide the second input parameter to this collecting and then method.
[08:03] But before that let me correct all these parentheses.
[08:06] Seems I have too many parentheses here.
[08:08] So what I'll do is first I'll check these opening parentheses for the same.
[08:13] Here we have a corresponding closing parenthesis.
[08:16] Similarly I'll check this one and there is a closing parenthesis for this one.
[08:21] There is a closing parenthesis.
[08:22] And for this one there is a closing parenthesis.
[08:25] So this looks good to me.
[08:26] I can mention comma here post that I can try to provide the second input parameter.
[08:32] But before that let me put a semicolon here so that all my compilation errors will get resolved.
[08:37] So what is the second input parameter we have to provide.
[08:40] We need to provide a lambda expression, which is going to help my collecting and then method to derive
[08:46] the result based upon the output that it is going to get from this first parameter.
[08:51] So this these first two parameter, which we built with the help of max by method, is going to simply
[08:56] give the product to object which has the highest price.
[09:00] If you open this max by, you can see the return type of this method is optional of t, T indicates
[09:07] product.
[09:08] So what is optional?
[09:09] Optional is another beautiful concept introduced inside Java eight to avoid null pointer exceptions.
[09:15] For now, let's not worry about it.
[09:17] I'll just try to use it without much explanation.
[09:20] But when I start explaining about these in the coming sections, it is going to make more sense to you.
[09:25] So basically, we are going to wrap our output inside the optional in the scenarios where we are not
[09:33] confident that we are always going to send a positive output.
[09:36] Sometimes we may also have a scenario where we may send a null as an output.
[09:41] In all these kind of scenarios, we are going to wrap our object inside optional so that the end user,
[09:49] whoever is trying to consume your output.
[09:52] They know that a null object is also possible as an output.
[09:56] Please do enough validations on your side before processing it.
[10:00] So this kind of heads up, we are going to give to the developer or the end user who is trying to catch
[10:05] this return type.
[10:06] So that's a history of optional.
[10:08] Now I'll go to the main class and here I'll try to provide the lambda expression.
[10:14] So my lambda expression it is going to accept a input parameter with the name product optional.
[10:21] So I'll just mention product optional followed by I'll just mention lambda symbol.
[10:27] Now as a next step, first I need to verify whether I have any valid product object inside my optional
[10:34] object, because in the scenarios where this product list is empty, then in such scenarios, my max
[10:40] by operation may send the null object as an output.
[10:43] That's why using this product optional.
[10:46] First I need to invoke the method is present.
[10:50] So this is present is going to give me a boolean value as true.
[10:54] If there is a valid product object is available.
[10:57] Otherwise it is going to give me false.
[10:59] So if I'm getting the output as true, then based upon the ternary operation, I want to fetch the object
[11:06] that I have inside this product.
[11:08] Optional.
[11:09] So here using product optional, I'm going to invoke the get method which is going to give me a product
[11:16] object.
[11:17] So inside product object we know we have a method with the name get name, which we can use to get the
[11:22] name of the product.
[11:23] So our target is to display the name of the product which has the highest price.
[11:29] That's why when this is present is returns true.
[11:32] First, I'm trying to get the object that is wrapped inside my optional object with the help of this
[11:36] Get method, followed by I'm trying to invoke the getter method, which is going to return me the name
[11:41] of the product.
[11:42] But if this is present is returning null, then in such scenarios I just wanted to return the product
[11:48] name as none.
[11:49] With these, we populated both the input parameters to the collecting and then method.
[11:54] So are you seeing the complexity here?
[11:56] If someone who is coming from normal imperative style background, who don't know the basics of lambda
[12:02] expression and these method references, they're going to be clueless what is happening with these lines
[12:08] of code in the imperative approach, if you want to achieve the same, you need to write at least ten
[12:13] different lines of code.
[12:14] But here I'm just trying to achieve the same with the just three simple lines of code.
[12:19] But I'm assuming you are clear about this code because you know the basics of lambda expression and
[12:24] how to read this code.
[12:25] So now on the left hand side, I'm going to catch the out with the help of string and the variable name
[12:30] as max price product.
[12:33] Finally, I'll try to print out these max price product onto the console with the help of System.out.println.
[12:40] So what is output you're expecting here?
[12:42] We should get this name as output which has highest price $1,500.
[12:47] So if I execute these, you will be able to see that I'm getting Apple Pro Max.
[12:52] But if you are looking to get the product which has a minimum price, then obviously we are having multiple
[12:59] minimum elements like here Nokia has 800 and mi has 800.
[13:04] Let me correct these two 600 and change these max by two min by.
[13:09] And with that the code should still work and we should get the output as Nokia.
[13:15] Hooray!
[13:15] We are getting the output like we expect, but let me roll back to max by so that this code is always
[13:21] going to return the product name with the maximum price.
[13:25] I hope you are clear on how to use these collecting and then method which is available inside the collectors.
[13:31] So always use these along with the collector terminal operation.
[13:35] Whenever you have a requirement where first you want to collect the elements from the stream, later
[13:40] on, you want to execute some other business logic to derive the final result.
[13:45] Thank you and I'll catch you in the next lecture by.

----------------------------------------

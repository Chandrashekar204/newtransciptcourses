# 25.6 — Demo of Constructor Reference

> Section 25: [JAVA 8] Building Lambda expressions using Method References

[00:00] Sometimes while you are trying to create a lambda expression, the only logic that you may have inside
[00:05] your lambda expression is to create an object of a class.
[00:09] In this kind of scenarios, you can leverage the constructor reference.
[00:14] I know this may look very confusing.
[00:16] Let's see a demo so that it is going to be super clear for you.
[00:20] So inside my project, first I'm going to create a new Java class with the name Product.
[00:26] Inside this Product class I'm going to create a couple of fields like private String name and the next
[00:34] field is private int price.
[00:36] So these are the two fields.
[00:37] So based upon these two fields I want to generate the constructor by considering these two fields post
[00:45] that I also want to generate the getter and setter.
[00:49] So let me select these two fields and generate the getters and setters.
[00:53] And at last I also want to generate the toString() method as well.
[00:57] So to generate the toString() method you need to select these toString() option and select these two
[01:02] fields post that
[01:03] if you click on this okay button you're going to get a toString() implementation.
[01:07] So now we have a Pojo class ready with the name Product.
[01:10] Think like I want to create an lambda expression, which is always going to help me to get an object
[01:17] of this Product class.
[01:19] So to build the same lambda expression, first I need to create a functional interface with the name
[01:25] Product interface.
[01:27] So this is a random name that I'm trying to give here.
[01:29] Once this interface is created, we need to mention the @FunctionalInterface.
[01:35] On top of this interface, followed by, we need to create a abstract method.
[01:39] Since we are trying to build a lambda expression which should return an object of Product, we need
[01:44] to mention the return type of the abstract method as product() itself, followed by the method name I'm
[01:50] going to mention as getProduct() and this method
[01:53] it is always going to accept two input parameters.
[01:56] The first parameter is what is the name of the product, and the second parameter is what is the price
[02:01] of the product.
[02:02] So these are abstract method that I have.
[02:04] So now using these functional interface I can write a lambda expression to define a lambda expression
[02:09] first let me create a new Java class with the name ConstructorReferenceDemo. Inside this class,
[02:17] first let me create the main() method followed by
[02:20] first, I'm going to write a lambda expression manually with the variable name as Product interface
[02:27] itself.
[02:28] Now on the right hand side inside the parentheses, I need to mention the parameter names like name,
[02:33] price followed by lambda symbol.
[02:36] After the lambda symbol inside the lambda body, I need to create the object of Product.
[02:42] So how to create it,
[02:43] we need to type new Product.
[02:45] And this Product has a constructor which is going to accept two parameters as an input.
[02:50] So we can pass the same parameters which are name, price here.
[02:54] So with that we have a lambda expression ready which is going to help us to create the object of Product
[02:59] based upon the input that we are going to send.
[03:01] So using these lambda expression I'm going to invoke the method which is getProduct().
[03:07] And to this method I'm going to pass the product name as Apple Mac with the price as 2000.
[03:14] So let me try to print out the output that we are going to get from these lambda expression invocation.
[03:20] So if I try to execute this program, you will be able to see the product related information on the
[03:27] console.
[03:27] So if you see here my lambda expression is simply creating the object of Product class.
[03:33] In this kind of scenarios we can leverage the constructor reference.
[03:38] So let me show you how to do that.
[03:40] So this time what I'm going to do is I'll copy these two lines of code.
[03:43] And here the variable name I'm going to mention as constructorReference.
[03:48] So these are the variable name. On the right hand side,
[03:51] instead of writing this lambda expression we just have to type the class name which is Product followed
[03:57] by
[03:58] we need to type two colons followed by new.
[04:01] So new is the operator that we need to mention.
[04:04] So the new should not have any parentheses and it should not have any input parameter details as well.
[04:10] It should be a simple newword.
[04:12] So this is very similar to the staticMethod reference.
[04:15] Just in the place of staticMethod you're going to mention the new.
[04:19] So why we are mentioning the new new is the operator inside Java, which is going to help us to create
[04:25] an object of a class.
[04:26] So that's why we can follow this syntax.
[04:28] So now using this ConstructorReference I can invoke the getProduct() method.
[04:33] And this time I'll mention the product name as iPhone followed by price.
[04:38] I'm going to mention $1,000.
[04:39] So if I execute this program this time, you'll be able to see another product
[04:43] details with the details
[04:44] Apple iPhone and the price as $1,000.
[04:47] I'm assuming you're clear on how to use the ConstructorRreference and under which scenarios you need
[04:53] to use this.
[04:54] All the details that we have discussed around the constructor reference I have mentioned in this slide
[04:59] for your reference.
[05:00] Along with the example code, you can also see a few other examples I'm trying to mention here.
[05:05] If your lambda expression responsibility is to create the object of a String, or an integer or
[05:11] ArrayList or UserDetail, it can be any class object.
[05:15] In all these kind of scenarios, you can follow the constructor reference like you can see here.
[05:21] So if I want to create an object of String, I don't have to stress out about it.
[05:25] I can simply leverage the constructor reference by using the class name, which is String, followed
[05:30] by two colons followed by new.
[05:32] I hope this makes sense to you.
[05:33] Before I try to close this lecture, let me show you an image which is going to show you the power of
[05:39] Method Reference concept.
[05:40] Like you can see here
[05:41] this is the evolution of Java program right from day one to Java 8 version.
[05:46] Initially, when a developer want to display all the elements inside a list, the developer used to
[05:52] follow a traditional for loop using the index values later on
[05:56] this has been enhanced with the help of for each and this is further simplified with the help of lambda
[06:02] expression, and even this lambda expression is further simplified with the help of method reference.
[06:09] So do you see the power of lambda expression?
[06:11] So the very first two approaches, they look very complex or they may look very in detail.
[06:16] But if someone knows lambda expressions and method references, they can write the code in a single
[06:21] line like you can see here
[06:23] under the third example we have a lambda expression example, whereas under the fourth example we have
[06:29] a method reference example.
[06:31] I hope you're clear about all the four approaches that we have discussed around the method references.
[06:36] Thank you and I'll catch you in the next lecture, bye.


########################################

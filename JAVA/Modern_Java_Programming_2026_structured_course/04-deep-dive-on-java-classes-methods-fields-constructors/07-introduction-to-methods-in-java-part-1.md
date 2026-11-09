# 4.7 — Introduction to methods in Java - Part 1

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] So far we have created classes and inside the classes we have declared that Java fields.
[00:05] As a next step, we should try to define methods as well inside the Java class.
[00:11] Before we try to do that, let's try to understand what is a method in Java.
[00:15] Why should we write methods inside Java?
[00:18] We already wrote a main() method in the previous section when we were trying to execute the hello world
[00:24] example.
[00:24] So you have a basic idea on how to write a method.
[00:28] Let's try to revise the same in detail inside this lecture.
[00:32] A method which we are going to define within a Java class represents the behavior of the objects belonging
[00:38] to that particular class or the behavior of the class itself.
[00:42] In other words, these methods, they are going to serve as a named blocks of code that can be invoked
[00:49] to execute its specified actions.
[00:52] I can handle a particular business use case with a Java logic inside a method, and whatever use case
[00:59] that we are trying to handle with the method, it has to be associated with the given class at the given
[01:04] object of a particular class.
[01:06] Inside a Car class, I can define methods which are going to handle the logic related to the Car.
[01:13] I should not write the logic related to the Person or a Customer inside the Car class, though technically
[01:19] it is possible and your Java compiler is not going to complain anything about that, but it is always
[01:25] a good practice to define the business logic related to of a class or an object inside its own body.
[01:33] So that's why we are going to follow the same standards throughout this course and in the same process
[01:37] I'm assuming you will also get used to the standard.
[01:40] Once we define a method inside a class, any other class, or any other entity, they can invoke our
[01:47] method.
[01:47] In such scenarios, whatever business logic we have written inside a method will be executed.
[01:53] So the entity or the component who are initiating our method execution, we can refer them as a caller.
[01:59] And when we define a method, our methods may receive input parameter values from the caller, and in
[02:07] return they can also return a value to the caller.
[02:10] So there is always a possibility for your method to accept the input and to send the output,
[02:15] whoever is invoking the method by sending the output and receiving the input is completely optional,
[02:22] which means we can write a method with zero input parameters indicating that it is not going to accept
[02:28] any input, and very similarly, we can also mention the return type as void, which means the method
[02:35] is not going to return any output.
[02:37] And inside Java, the methods we should always encapsulate them within the body of a class or an interface.
[02:44] Where to talk about interface.
[02:46] But if you talk from class perspective, we are always allowed to define our methods inside the body
[02:52] of a class.
[02:53] We cannot really write an method independently without a class.
[02:58] This encapsulation ensures that the behavior defined by the method is closely associated with the structure
[03:06] and purpose of the class to which it belongs.
[03:09] That's what we have discussed previously
[03:10] in the very first point.
[03:12] The return type of a method represents the data type of the value that the method is going to return
[03:18] whenever the method execution is completed, and this return type can be a simple primitive data type
[03:24] like int, float, double or it can be a reference data type like Car or a String.
[03:30] In cases where a method does not going to return any output to the caller.
[03:35] In such scenarios like we discussed, we need to mention the return type as void, indicating that the
[03:41] absence of a return value to the invoking entity.
[03:44] And when we are trying to define a Java method, we should also give a name to the Java method.
[03:51] Otherwise how the invoking entity is going to invoke our method.
[03:55] That's why we should always give a name to our method and the naming standards that we need to follow
[04:01] while we are trying to define a method name is very similar to the standards that we followed while
[04:07] declaring the variable names our field names.
[04:10] This means even if our method names, they should follow the camel case style.
[04:14] The very first letter of your method should always start with a small letter, and post that every subsequent
[04:21] word that you are trying to add to your method name should start with a capital letter.
[04:26] For example, here I have defined a method names like moveVehicle(), applyBreak(), getSpeed() and stopVehicle()
[04:33] .
[04:33] So these are all the valid method names which are following the Java standards.
[04:38] Whereas if I try to define a method name like moveVehicle() vehicle with a random capital letters or small letters
[04:45] like you can see here, this is still going to be a valid method name from your Java compiler perspective,
[04:50] but with this, you're not going to follow the standard of camel case naming conventions, which will
[04:56] make your code as a bad code in front of other developers.
[04:59] Now, since we talked enough details about what is a Java method, let's try to understand how we can
[05:05] declare methods in a Java class, and what is the syntax that we need to follow.
[05:09] Like you can see here, whenever we are trying to define a method, the very first information that
[05:15] we should provide is modifier.
[05:16] Just like how your class and Java field have a modifier.
[05:20] Very similarly, your method also can optionally have a modifier.
[05:25] This modifiers indicates who can invoke your method.
[05:28] If you start your method declaration with the private, then no one can invoke your method from outside
[05:34] of your Java class.
[05:35] Only the methods which are present in the same class can invoke.
[05:39] So we're going to talk about modifiers in detail
[05:42] for now, we are going to go with a modifier which is public for all our methods.
[05:47] Even if you don't mention this modifier, your compiler is not going to complain anything because this
[05:53] is completely optional.
[05:54] After the modifier, you need to mention what is the return type of your Java method?
[06:00] The return type means what is the data type of the output that your method is going to return.
[06:05] If you are trying to return an int value, you should mention the return type as int
[06:09] or if you are trying to return an String, then you should mention the String as an return type.
[06:14] After the return type, you should mention a method name like we discussed previously
[06:18] the method name should follow the CamelCase style, and while you are trying to give a method name,
[06:23] please make sure you are giving a name which is very meaningful.
[06:27] Your method name should give an high level information to the other developers.
[06:31] What exact logic your method is going to execute.
[06:34] So such high level summary
[06:36] your method name should hold.
[06:38] After the method name you should have a parentheses, opening and closing parentheses.
[06:42] Inside these parentheses only you can provide your input parameter details like what is the data type
[06:49] of your parameter and what is the parameter name.
[06:52] These parameters can be zero or it can be more than 1 or 2.
[06:56] There is no restriction on how many input parameters that your method name can accept.
[07:01] You can define any number of parameters based upon your business requirement and after the parameter
[07:07] list
[07:07] you can also mention the Throws class.
[07:09] This Throws class represents what kind of exception your method may throw.
[07:15] Like always, we should not assume, like our method and the business logic that we write inside the
[07:20] methods will execute without any problems.
[07:23] Sometimes errors are exceptions may happen.
[07:26] That's why to represent such information we can use the Throws class.
[07:30] And this will give you enough heads up to the invoking parties or entities that these so on
[07:36] so method can throw so-and-so exception.
[07:39] And I should be ready for such kind of exceptions.
[07:42] We are going to discuss in detail about the exceptions in the coming sections for the next few lectures,
[07:47] we are not going to worry about the Throws class.
[07:49] This Throws class also is completely optional.
[07:52] After the Throws class, your method is going to have opening and ending curly braces, just like how
[07:58] your Java class has very similarly, every Java method should have a opening and curly braces and whatever
[08:05] business logic that we want to write, we should write within these curly braces only. The content
[08:11] that we are going to write within these curly braces
[08:14] in other words, we can also call it as body of the method.
[08:17] And at the end, if your method is going to return some value, you should have a return statement at
[08:23] the end.
[08:24] If your method is not sending any details as an output, then this return statement is completely optional
[08:31] for your reference.
[08:32] I also mentioned all the points that we have discussed in the next slide.
[08:36] What is the purpose of each of the component inside the method
[08:40] syntax declaration.
[08:41] You can always have the slide as a reference.
[08:44] I hope you are clear with this quick introduction.
[08:46] Let's try to continue the discussion around the methods in Java in the next lecture as well.
[08:51] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

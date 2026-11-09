# 25.4 — Demo of Instance Method Reference

> Section 25: [JAVA 8] Building Lambda expressions using Method References

[00:00] In the previous lecture we saw the demo of staticMethod reference.
[00:04] All the details that we have discussed, along with the example I have mentioned inside this slide for
[00:09] your reference.
[00:10] Now inside this lecture, let's try to discuss about the instanceMethod
[00:15] reference.
[00:16] I think based upon our staticMethod reference discussion, you should be able to implement
[00:23] instanceMethod reference very easily.
[00:24] I request you to pass the video and try the instanceMethod reference by taking the same scenario that
[00:30] we have discussed in the previous lecture.
[00:33] Instead of staticMethod, you need to have an instanceMethod.
[00:36] I hope you are successful, otherwise don't worry, I'm there for you.
[00:40] I'm going to explain how to leverage instance methods to implement lambda expressions very quickly.
[00:47] To show you the demo, I'm going to copy these class inside the same package, but this time the class
[00:53] name I'm going to mention as instanceMethod reference post that I'm going to convert these staticMethod
[01:01] into an instanceMethod or non staticMethod by removing these static keyword.
[01:07] With that you can see I'm getting a compilation here saying that non static method cannot be referenced
[01:12] from a static context.
[01:13] So whenever we want to invoke a non static method or an instance method, what we need to do, we need
[01:19] to first create the object reference of the given class.
[01:24] So that's why just above this line I'm going to create the object of InstanceMethodReference with
[01:30] the variable name as instanceMethodReference post that I'm going to type new InstanceMethodReference().
[01:37] With this line I successfully created an object reference.
[01:40] Now let me use these object reference to implement the instance method.
[01:46] References.
[01:47] So here in the place of class name I'm mentioning the object reference.
[01:50] And with that you can see we have our new lambda expression ready based upon our logic.
[01:56] Similarly, if you have some other instance method which is going to perform the subtraction, you can
[02:02] simply leverage that as well.
[02:05] So here I'm trying to create a instance method which is going to perform the subtraction.
[02:10] And the result is going to be stored inside a variable name with the name diff.
[02:15] The same I'm trying to return here.
[02:16] So now using this instance method also I can try to build a new lambda expression.
[02:22] So what I'm going to do here is, I'll try to copy these two lines of code and paste it here.
[02:27] But this time I'm going to mention the lambda expression variable name as methodReferenceSub sub means
[02:34] subtraction. On the right hand side,
[02:36] instead of performAddition, we need to mention the performSubtraction() method name.
[02:40] So only make sure you are mentioning the method name.
[02:43] There is no need of parentheses and there is no need of mentioning any input parameters.
[02:47] And after making this change, we need to make sure we are using these lambda expression variable here
[02:52] to invoke the only abstract method that we have, which is performOperation().
[02:57] Now let me try to execute this class.
[02:59] And you can see we are getting the output 5, 5 and -1 like we expect.
[03:04] I hope you are clear on how to use the instance method reference.
[03:08] Here we are trying to invoke our own instance method, but it is not mandatory to invoke your own instance
[03:14] method.
[03:14] You can invoke instance methods available inside the JDK libraries or inside any other API classes like
[03:21] a String.
[03:22] So the requirement can be anything.
[03:24] If you are logic that you are trying to implement inside your lambda expression is already available
[03:29] inside a method, then please try to leverage the staticMethod reference or instance method reference.
[03:35] I hope you are clear.
[03:36] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

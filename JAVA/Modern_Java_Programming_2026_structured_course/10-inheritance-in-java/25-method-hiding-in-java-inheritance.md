# 10.25 — Method hiding in Java Inheritance

> Section 10: Inheritance in Java

[00:00] Just like how we have concepts of method overriding and overloading, we also have a concept of method
[00:07] hiding inside Java inheritance.
[00:10] Very few Java developers knows about these method hiding concepts.
[00:14] By the end of this lecture, you will be comfortable with these concepts and you will join the a lite
[00:21] group of few Java developers who know about this concept.
[00:25] So be proud of yourself.
[00:26] So what is a method hiding?
[00:28] To understand first about method hiding,
[00:30] first, we need to understand what is going to happen inside inheritance
[00:35] for the static methods. We know a class inheritance all non-private static methods from its superclass.
[00:42] That means if you have a static method inside your superclass, the same is going to be inherited by
[00:47] your subclass as well
[00:49] as long as your static method is not a private method.
[00:53] Once the subclass inherits the static method from the superclass, if it is going to define the same
[01:00] kind of static method inside the subclass, then such concept we are going to call it as method hiding,
[01:07] but not the method overriding.
[01:09] Why
[01:10] it is not going to be method overriding because method overriding only applicable for the instance methods,
[01:16] which belongs to the specific object of a class, whereas static methods they belong to the class,
[01:23] but not to the object.
[01:25] That's why whenever we are trying to define the same static method like we have inside the superclass,
[01:31] we are going to call that concept as method hiding.
[01:34] I can also show you an example here.
[01:36] So here you can see I have a super class with the name Vehicle.
[01:40] And inside this Vehicle superclass I have a static method which is public static void start().
[01:47] And inside the static method I have a statement which is Vehicle starting.
[01:51] Now this superclass I am going to inherit with the help of extends keyword inside my subclass
[01:58] which is Car.
[01:59] If you closely look at my subclass class body, my subclass also have same static method with the same
[02:06] name,
[02:07] with the same method signature like public static void start().
[02:11] But the println() statement that I have inside this method is Car starting.
[02:15] So the start() static method that we have inside the subclass Car,
[02:19] it is an example of method hiding.
[02:22] I hope you are clear about what is a static method.
[02:25] As a next step, let's try to implement the same inside our IntelliJ and try to see the demo of
[02:31] method hiding.
[02:32] As of now, inside the base package, I already have a class with the name Vehicle inside this class
[02:39] now I'm going to define a static method by using public, followed by static, followed by void and
[02:47] after the void
[02:47] I'm going to mention the method name, which is start(), and inside this method I'm going to have a System.out.println()
[02:55] which is going to print vehicle starting.
[02:59] So this is the statement that I want to maintain inside this method.
[03:02] As a next step, let me try to create a new package.
[03:06] The package name is going to be com.eazybytes.marvel.Vehicle.
[03:12] So inside these vehicle related package I'm going to create all the implementation classes of Vehicle
[03:19] superclass.
[03:20] So here let me try to create a new Java class.
[03:23] The class name is going to be Car.
[03:25] And this Car subclass is going to extend the superclass which is Vehicle.
[03:30] So as soon as we try to extend we are going to inherit the static method available inside the Vehicle.
[03:37] Superclass the same
[03:39] we can confirm by pressing command F12
[03:42] in my case, and if you are using windows it will be control F12.
[03:46] So here if I try to type start, you can see I have a method with the name start which is of type static
[03:53] and it is getting inherited from the Vehicle superclass. As a next step
[03:58] let me try to create the same static method inside my Car subclass.
[04:03] Now here instead of Vehicle I'll just mention Car starting.
[04:07] I can't put Override annotation on top of this, because override annotation we can only use in the
[04:14] concept of method overriding while we are trying to performing overriding of an instance method in the
[04:21] superclass.
[04:21] But this is a static method
[04:23] that's why in this kind of scenarios we call this concept as method hiding.
[04:28] So this is how you're going to perform the method hiding.
[04:31] Now you may have a question which is how can I invoke the start() method present inside the subclass,
[04:39] or the start method present inside the Vehicle class.
[04:43] So how can I perform that?
[04:44] So it's a very valid question.
[04:46] Let's try to see an example around the same.
[04:48] So here under the app package I'm going to create a new Java class with the name TestMethodHiding,
[04:58] inside this class as usual
[05:00] first we need to create the main() method inside this method
[05:04] first I'm going to create the object reference of Vehicle.
[05:07] To this I'm going to assign the object of subclass which is new Car.
[05:13] So this is perfectly fine.
[05:14] This is called Upcasting like we discussed.
[05:17] So in the next line I'm going to create the object of Car subclass by using the new operator and the
[05:26] default constructor of Car subclass.
[05:28] So this is a normal object creation.
[05:31] We know inside Java we can invoke a static method with the help of the class name or with the help of
[05:37] object reference as well.
[05:38] So the recommendation is always to use the class name to invoke the static methods.
[05:43] But sometimes developers, they'll also use object reference to invoke the static method.
[05:49] So let's try to take both of these scenarios and try to understand how the method hiding invocation
[05:54] is going to work.
[05:55] So first I'll write a statement which is with the help of class name of Vehicle
[06:00] I'm going to invoke the start method very similarly with the help of Car class
[06:05] also I'm going to invoke the static method which is start().
[06:09] So in this kind of scenarios there won't be any confusion because we are directly calling the static
[06:16] method using the Vehicle name itself.
[06:19] So my compiler straightaway is going to invoke the static method available inside the Vehicle class.
[06:26] And here it is going to invoke the static method available inside the Car class.
[06:30] So the output we are going to get is whatever we have mentioned here.
[06:34] So let me copy the same and mention here for your reference.
[06:38] Similarly, I'm also going to mention the second output which we are going to get which is Car starting.
[06:44] So we can validate this by executing these Java class.
[06:48] You can see first I'm getting Vehicle starting followed by Car starting.
[06:52] So now let's try to make it more complicated.
[06:55] This time I'm going to invoke the start() method with the help of object references that we have.
[07:01] So I have one object reference which is Vehicle.
[07:03] So if I try to type dot I'm not going to get any method recommendation with the name start().
[07:10] You can see I'm getting a compilation error.
[07:12] But if I try to complete this statement it is going to eventually compile successfully.
[07:17] Very similarly, let me try to invoke the start() static method with the help of Car object reference.
[07:23] What I can do is I can try to copy this immediately next to the first statement.
[07:29] Similarly, I'm also going to keep this just below the Car.start() invocation that we have tried previously.
[07:35] Even in this kind of scenarios
[07:37] also, the Java is going to invoke the static method available inside the Vehicle class only.
[07:43] The reason is though, we are assigning the object of Car object the Java
[07:48] in the scenario of method hiding, it is not going to worry about which object we are storing inside
[07:53] an object reference, because this is not an instance method, this is a static method.
[07:59] So for all static methods, Java always going to look for the what is the data type of the object reference
[08:07] that we are trying to use here.
[08:08] So what is the data type.
[08:10] It is going to be Vehicle.
[08:11] That's why we are going to get the output as Vehicle starting.
[08:15] The same is going to happen here for Car.start()
[08:18] also here also we are going to get Car starting as an output.
[08:21] So what I can do is, I can try to copy the same output here and this output also I can copy but instead
[08:28] of one here I'll keep it as two followed by I'll keep this as three followed by four.
[08:34] So let's try to execute this program and validate whether we are getting the same output.
[08:38] You can see we are getting Vehicle starting, Vehicle starting, Car starting, Car starting.
[08:43] Now let me show you another flavor.
[08:45] So what I can do is I can try to copy this fourth line.
[08:49] And just before invoking the start() method, I'm going to typecast my Car object reference to the Vehicle
[08:57] class.
[08:58] So let me do the same by using the casting symbol.
[09:01] So within the parentheses I'm going to mention Vehicle class and entire expression
[09:08] I'm going to surround it with the parentheses.
[09:11] So you can see I'm trying to appcast my Car object reference to the Vehicle superclass.
[09:19] So in this scenario, which static method are you thinking is going to be invoked?
[09:24] Off course it is going to invoke the start() method available inside the Vehicle superclass, because we
[09:31] are changing the reference data type from Car to Vehicle.
[09:35] So that's why here when I try to print this statement we are going to get the output as Vehicle starting.
[09:43] So let me try to execute this program.
[09:45] And you can see at the end we are getting Vehicle starting.
[09:48] Let me show you more flavors also here.
[09:50] So I'll try to assign Car object to the Vehicle object reference.
[09:57] So this you can think like line
[09:59] number 6.
[10:00] Now using the object reference of Vehicle, I'm going to invoke the start() method.
[10:07] In this scenario, the compiler will never try to look what object
[10:10] right now my Vehicle object reference is holding.
[10:14] It is not going to look for that information anytime because you're trying to invoke a static method.
[10:20] Since we are trying to invoke the static method, it will only worry about to which data type this Vehicle
[10:26] object reference belongs.
[10:27] So this is belongs to the Vehicle class.
[10:30] So that's why at line number seven we are going to get the output which is Vehicle starting.
[10:37] So let me execute this program.
[10:39] And at the end you can see we're again getting the Vehicle starting.
[10:43] As a last step I can try to downcast this Vehicle object reference to the Car subclass.
[10:49] So how to do that
[10:50] First let me try to copy this entire line followed by I'm going to downcast this Vehicle object reference
[10:57] to Var and surround this entire expression with parentheses.
[11:02] So now with this, my Vehicle object reference is going to be downcast it to the Car object reference.
[11:10] With that, the start method present inside the Car subclass is going to be invoked.
[11:15] That's why we are going to get the output as car starting.
[11:18] So let me validate the same by invoking this program.
[11:22] At the end you can see we are getting the Car starting as an output.
[11:27] I hope you are clear.
[11:28] The thumb rule is very simple
[11:29] when you are using the class name to invoke the static method, the compiler is not going to worry about
[11:36] anything since you are directly using the class name
[11:38] the static method present inside that particular class is going to be invoked, but you're going to
[11:43] make the compiler task tough when you start using the object references to invoke the static methods.
[11:51] In such scenarios, compiler is not going to worry a lot.
[11:55] It will simply look at the what is the class type or data type of the object reference.
[12:01] So based upon the type, the static method is going to be invoked, whereas inside the method overriding
[12:08] the compiler or the Java, always look at the which object we are trying to assign to the object reference.
[12:14] Using the same object, the instance method is going to be invoked.
[12:19] I hope you are getting the difference between method hiding and method overriding invocations.
[12:24] Everything that we have discussed along with the method hiding example I have highlighted inside this
[12:30] slide.
[12:30] Please refer the same for more details.
[12:33] Thank you,
[12:34] bye.

----------------------------------------

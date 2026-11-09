# 29.8 — [JAVA 24] Getting to know the basic syntax of using Gatherer interface

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] There is a new interface with the name Gatherer introduced as part of Java 24.
[00:06] Let me open the same.
[00:07] We're going to explore this interface in detail.
[00:10] To check the same interface inside your IDE as well, you need to make sure you have downloaded the
[00:15] JDK 24 and configure the same for your project.
[00:18] For example, inside my IntelliJ I have configured JDK 24.
[00:23] I can confirm you the same as well.
[00:25] Let me right click on this project and select Open Module Settings.
[00:31] Inside this settings first I'll go to project and this SDK.
[00:35] I make sure I have configured the JDK 24. In your case
[00:39] also, you need to make sure first you're downloading the JDK 24 by using this download JDK option,
[00:45] followed by
[00:45] you need to select the same under this SDK.
[00:48] Coming to the language level, you need to select the 24 stream gatherers.
[00:53] You will see these options only if you are using the latest version of IntelliJ.
[00:57] Please make sure you also updated your IntelliJ to the latest version. After the project you should also
[01:03] go to the modules and under the modules please select the language level as project default.
[01:09] This setting it will set the SDK 24 as a dependency, the same we can confirm under these dependencies
[01:17] as well.
[01:17] Let me click okay.
[01:19] Whenever we want to define our own custom intermediate operation with the help of gatherer API, we
[01:25] need to make sure we are defining our business logic by implementing these Gatherer interface.
[01:32] This Gatherer interface implementation, it is going to accept three input parameter. The T indicate what
[01:39] is the type of input element that your upstream is going to provide to your gather intermediate operation.
[01:46] Whereas the second parameter, a, represents a mutable state.
[01:51] For the next few minutes, we are not going to focus on this mutable state.
[01:55] For now, let's ignore the same.
[01:56] The third parameter, which is R,
[01:58] it is representing the type of output element that you are
[02:01] Gatherer is going to push to the downstream.
[02:04] This gatherer is a functional interface.
[02:07] There is only a single abstract method available inside this interface.
[02:12] If you try to look for the list of methods inside this interface, you'll be able to see there is a
[02:17] single abstract method with the name integrator().
[02:20] How can I say this is an abstract method?
[02:22] If you see the method icon just before this integrator() name, it is not completely closed.
[02:29] It has some open space.
[02:30] This means this is an abstract method, the same we can confirm by looking at the signature of the method,
[02:36] whatever core logic that we want to define as part of our custom intermediate operation that we are
[02:43] going to build with the help of gatherer API, the same needs to be defined under these integrator.
[02:49] The name itself is self-explanatory.
[02:51] This integrated method
[02:53] it is going to act as a integration piece between the upstream and downstream.
[02:58] The return type from these integrated method is Integrator interface.
[03:03] Let me open this interface.
[03:04] This is one other functional interface which means to define our business logic
[03:09] with the help of integrator we need to provide an lambda expression.
[03:12] So this integrator also it is going to accept to three input parameters.
[03:17] The first parameter which is a mutable state.
[03:20] The second parameter represents that the type of the element that you are integrator is going to receive
[03:26] as an input from the upstream.
[03:28] And the third parameter represents the type of the element that you are integrator can produce and push
[03:33] into the downstream.
[03:34] Please make a note that parameters are exchanged here for your integrator
[03:39] always
[03:39] the mutable state is the first parameter, whereas for your Gatherer interface, the first parameter
[03:45] is always the type of input element followed by the mutable state.
[03:49] And at last we have that type of element that we are going to push to the downstream.
[03:53] Don't get confused.
[03:54] Please make sure you are clear on the order of the elements for these Gatherer interface and for the
[04:00] Integrator interface.
[04:01] Apart from Integrator component
[04:04] inside the Gatherer interface, we also have other important components like initializer, combiner and
[04:11] finisher.
[04:11] These three highlighted components, they are optional.
[04:15] They are created as default methods inside the Gatherer interface. They're going to have some default logic.
[04:22] These three optional components
[04:23] also they're going to play an important role while we are defining the business logic with the help
[04:29] of integrator.
[04:30] It is completely possible to define our intermediate operation by simply implementing the integrator
[04:36] component alone.
[04:37] But there are some common scenarios where you need to leverage this initializer, combiner and finisher.
[04:44] We're also going to discuss about them in a few minutes.
[04:47] But before that, let's try to understand how to create a simple intermediate operation with the help
[04:54] of Stream Gatherers API by leveraging these integrator component alone.
[04:58] Before I try to write some code, let me show you the methods corresponding to the initializer, combiner
[05:05] and finisher.
[05:06] Inside the Gatherer interface, there is a method with the name initializer().
[05:10] This is a default method.
[05:13] In the similar lines we also have combiner as well.
[05:17] This component is also implemented with the help of this default method.
[05:21] And at last we have finisher() default method as well.
[05:25] Since these are optional, there is some default logic defined inside these methods.
[05:29] But if a developer wants to leverage the full power of gather API, the developer should definitely
[05:34] understand the purpose of these components and how to define the logic inside them.
[05:38] We're going to explore them
[05:39] don't worry.
[05:40] For now, what I'm going to do is, I'll try to create a new package with the name com.eazybytes.java24
[05:48] inside this new package
[05:51] first I'm going to create a new class with the name A_HelloGatherer
[05:56] .
[05:58] Inside this class, let me create a main() method.
[06:01] Inside this main() method I want to define my own custom intermediate operation with the help of Gatherer
[06:07] interface.
[06:08] First let me type Gatherer to this gatherer, I need to pass.
[06:13] What are the data types of the elements that I'm going to receive from the upstream, and the data type
[06:18] of the element that I'm going to push to the downstream from my intermediate operation.
[06:23] For now, I'm going to mention string as a very first data type.
[06:27] So this string represents the elements that my intermediate operation is going to receive from the upstream,
[06:32] followed by I'm going to mention question mark.
[06:34] Second parameter represents the mutable state.
[06:37] We are going to talk about this mutable state in the upcoming parts.
[06:41] For now, let's keep it as wild card, which means I'm telling to the compiler that this mutable state
[06:45] data type can be of any data type.
[06:48] And the last parameter I'm going to mention as string itself.
[06:52] Since I want to push a string objects to the downstream, I'm trying to mention string here.
[06:56] It is not mandatory to define same data type for the upstream and downstream.
[07:02] We can define completely different data types as well.
[07:05] For now, let's go with the same data type, followed by.
[07:08] I'm going to mention a variable name as Gatherer.
[07:12] And to this variable we need to assign the implementation of Gatherer interface.
[07:18] This Gatherer interface,
[07:19] it is a functional interface because it has a single abstract method with the name integrator().
[07:25] In this kind of setups we can define the implementation logic with the help of lambda expression.
[07:31] Let me define a lambda expression.
[07:34] From the logic of my lambda expression, I should return an object or implementation of these Integrator,
[07:41] whatever lambda expression that I have returned right now.
[07:44] This is an implementation for this integrator() method.
[07:48] Since these integrator() method is trying to return an object of Integrator, I need to make sure I'm
[07:54] returning the same from my lambda expression.
[07:57] Let me open this Integrator.
[07:59] This Integrator is again an another functional interface.
[08:03] This interface also has a single abstract method with the name integrate this integrate() abstract method
[08:08] it is accepting three input parameter.
[08:10] The first parameter is the mutable state and the second parameter represents the element that we are
[08:15] going to receive from the upstream, followed by
[08:18] the third parameter is the entire downstream object.
[08:21] Since I can't create an object of this integrated directly here, what I had to do is I have to define
[08:27] an another lambda expression matching these abstract method signature.
[08:33] And the second lambda expression that I'm going to define it should return a boolean.
[08:37] There is a very important concept around this boolean.
[08:40] I'll explain that in a few minutes.
[08:42] But before that let's try to define the second lambda expression.
[08:46] So inside a lambda expression I'm trying to define another lambda expression.
[08:50] This second lambda expression it is going to accept to three input parameter.
[08:54] The first one is state followed by element followed by downstream.
[08:58] Since the second lambda expression, it is going to expect a boolean as an output.
[09:02] I'm going to simply return true.
[09:05] Let me type true here and followed by semicolon.
[09:09] You don't need these outer brackets as well.
[09:11] I can simply remove them.
[09:13] So this is how we can create the implementation with the help of Gatherer.
[09:17] So first I have define a lambda expression.
[09:20] And since this lambda expression is expecting an object, our implementation of Integrator I have defined
[09:26] another lambda expression which is going to accept three input parameters state element and downstream.
[09:32] For now, under the business logic that I have written under these integrate() method of Integrator,
[09:37] I'm simply trying to return true boolean value.
[09:40] I know this is very complex.
[09:42] There are some developer friendly approaches also available to us.
[09:45] We are going to definitely explore them.
[09:47] The reason why I'm trying to show these harder or complex approaches is,
[09:51] I want you to be very clear on how things are working under the code
[09:55] when you are using the gatherer API, these gatherer variable, right now it is representing an intermediate
[10:02] operation.
[10:03] Let's try to use the same inside a stream data pipeline just above this line.
[10:07] What I'll do is, I'll try to create a list which is having all the string values.
[10:13] So these strings variable, it is going to represent a List object.
[10:16] With the help of the strings, I'm going to invoke the stream() method, so this will be my upstream.
[10:23] After the upstream, I need to invoke the gatherer() method, which is going to allow me to define my
[10:29] own terminal operation.
[10:31] To this gatherer() method, we need to pass the Gatherer interface implementation.
[10:35] We have the same already here.
[10:37] Let me mention gatherer as an input here.
[10:40] After this intermediate operation, we can define another intermediate operation based upon our requirements,
[10:45] or we can also invoke an terminal operation.
[10:48] Let me try to invoke a terminal operation with the name to list the output.
[10:52] From this terminal operation, I'm going to catch with the variable name
[10:55] as result, the same I'll try to print out with the help of a System.out.println().
[11:01] If I try to execute this program, the result is going to be empty.
[11:06] The reason is inside my intermediate operation.
[11:09] I'm not doing anything.
[11:10] I'm not even passing the same to the downstream.
[11:13] I'm receiving the element from the upstream, but I'm not passing them to the downstream.
[11:17] How to pass the elements to the downstream.
[11:19] If you try to understand the integrate() method, the downstream is going to be represented with the help
[11:25] of this third parameter.
[11:26] Let me open this downstream, which is an another functional interface.
[11:30] Inside this functional interface there is a abstract method with the name push().
[11:35] As a developer, whenever you want to push your element to the downstream, you need to invoke this
[11:40] method.
[11:41] So this method is also going to return the boolean as an output, which is also matching with the return
[11:47] type of the integrate() method.
[11:49] What I can do is, with the help of the downstream, I'm going to invoke the push() method.
[11:55] To this push() method, we can pass the element that we have received from the upstream.
[12:00] The same I'm trying to mention here, since this push is also returning a boolean variable which is
[12:06] matching with my integrate abstract method signature.
[12:09] I'm not getting any compilation error.
[12:11] If I execute this program right now, you will be able to see the output list is matching with the input
[12:18] list that we have inside our program.
[12:21] This is because we are not doing anything other than simply pushing the upstream element to the downstream,
[12:28] with the help of our gatherer intermediate operation.
[12:32] Maybe before we try to push the element, we can try to transform the element.
[12:36] Here, let me try to invoke the toUppercase() method, which is going to transform all the String objects
[12:44] into uppercase values.
[12:45] If I try to execute this program this time the output list, it is going to have all the String objects
[12:51] in and completely uppercase letters.
[12:54] I hope you are clear on how to define an a basic intermediate operation
[12:59] with the help of the syntax that we have discussed so far.
[13:01] This may looks very complex because inside a lambda expression we are trying to write another lambda
[13:06] expression.
[13:07] As you try to implement more and more complex business logic.
[13:11] This syntax may not be developer friendly.
[13:13] That's why, as a next step, let's try to understand how to define an Gatherer implementation with
[13:19] some developer friendly approaches.

----------------------------------------

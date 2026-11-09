# 11.10 — [JAVA 8] How to build static methods in interfaces

> Section 11: Interfaces in Java

[00:00] This is the feeling of static methods to the Java team.
[00:05] They requested a lot
[00:07] please allow us as well.
[00:09] So these kind of requests made by the static methods.
[00:12] That's why from Java 8 we can also write static methods inside an interface.
[00:17] So these are a funny note Java team didn't introduce static methods inside interface
[00:24] just like that.
[00:25] There is a strong reason.
[00:26] So let's try to understand the same.
[00:28] When you start writing lot of business logic inside your interface with the help of private methods,
[00:33] or with the help of default methods.
[00:36] Obviously at some point of time you will have some utility logic which is specific to your interface.
[00:42] Before Java 8, all the utility logic related to an interface they used to maintain in a separate
[00:49] class with the multiple static methods, but from Java 8, since we can define business logic within
[00:56] the interface, there is a strong need came for the utility methods
[01:00] also, are the static methods also to be allowed inside the interface?
[01:04] That's why from Java 8, Java team also allowed static methods inside an interface.
[01:10] I can also show you a demo here.
[01:12] I can try to create a static method.
[01:15] I don't have to mention public because by default all methods inside an interface are public except
[01:22] the private methods,
[01:23] because for private methods we are going to mention the access modifier as private.
[01:28] After static, I'm going to mention the String as a return type from the static method and the method
[01:34] name I want to keep it here is common characteristics.
[01:37] So from this method I want to return list of common characteristic of any superhero.
[01:44] So let me mention the same with the help of return keyword.
[01:48] After the return keyword I can mention a String, and inside this String I can mention all the characters
[01:54] like superhuman abilities, willingness to sacrifice.
[01:57] This way we can mention any number of characteristics using comma separated value.
[02:02] So if you see the purpose of this static method is to send the list of characteristics of a superhero.
[02:08] So it's a kind of utility method which can be used to buy my other implementation classes or by my private
[02:16] or default methods.
[02:18] So this is how we need to create
[02:20] when we create a static method, all your implementation classes, they will be able to access the static
[02:26] method either by directly using the static method name, or they can also try to access with the help
[02:32] of interface name followed by dot operator, and after the dot operator they can mention the static
[02:38] method name.
[02:39] Apart from your implementation class, any other classes also can invoke these static methods.
[02:45] For example, here, with the help of SuperHero interface name, I can try to invoke the static method
[02:52] which is commonCharacteristics().
[02:54] So this is how you can invoke from other classes as well.
[02:58] Let me remove this.
[02:59] If there is a scenario for one of your implementation class of an interface to define exactly same kind
[03:06] of static method like defined inside an interface, they can obviously define their own static method.
[03:12] For example, I can take the static method and paste it inside the SpiderMan.
[03:18] And here I can also mention public just to make sure I'm having the same copy of interface.
[03:25] Here I'm able to define the same static method which is defined an interface, but I should not call
[03:31] this as an override.
[03:33] Like we discussed inside previous section, whenever we are dealing with the static methods and static
[03:39] fields, override will not come into picture.
[03:42] Only method hiding will come into picture.
[03:45] So this is called method hiding.
[03:47] I can also show you by putting an Override annotation
[03:51] on top of this method.
[03:52] You can see we are going to get a compilation error saying that static methods cannot be annotated with
[03:58] override, because for static methods, we can only do the method hiding, but not the method overriding.
[04:05] I hope you are clear before I try to close this lecture, I want to share an very, very important point
[04:11] around the static methods inside an interface.
[04:14] So now I said, since the static methods are allowed inside an interface, can I create a main() method
[04:20] and execute my interface to get some output?
[04:24] Let's try to validate the same.
[04:25] For the same, I'll go to the Person interface,
[04:28] inside my Person interface I'm going to create a main() method which is of type static.
[04:33] And you can see we are getting a warning saying that modifier public is redundant for interface members.
[04:39] So I can try to remove this and post that
[04:42] I will just simply mention a System.out.println() with an statement which is Hello World from interfaces.
[04:51] So let's try to execute this interface and see if we are going to get the same as an output.
[04:57] Hooray!
[04:57] we are getting Hello world from interface.
[05:00] So this gives a confidence to us that we should be able to create a main() method inside an interface
[05:06] and execute the business logic.
[05:08] So this can be a tricky question inside your introduce.
[05:11] So that's why please make a note of it and answer correctly inside your interviews.
[05:17] All the points that we discussed around the static methods
[05:20] I have mentioned the same in these two slides for your reference.
[05:23] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

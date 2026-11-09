# 11.13 — Interface defines a new type

> Section 11: Interfaces in Java

[00:00] Whenever we define an interface inside a project, it is going to create a new data type, which you
[00:08] can use inside your Java programming logic.
[00:11] In other words, when a class implements an interface, it is going to establish a Supertype and subtype
[00:17] relationship.
[00:17] The class becomes a subtype for all the interfaces it implements, and conversely, all interfaces they
[00:26] are going to become super types of the class.
[00:28] I can also show you an example around this if you see here
[00:31] previously, inside this MarvelHeroDemo, we are trying to assign the object of the implementation
[00:38] classes to the type of interface which is SuperHero.
[00:42] So this is possible because the SuperHero interface is acting as an super interface for the class IronMan
[00:49] IronMan
[00:50] the same applies for the SpiderMan and the CaptainAmerica.
[00:52] So as long as you have this super type and subtype relationship, you can try to assign the objects
[00:59] of implement iron classes to the variable reference of super type, which is SuperHero.
[01:05] The same variable references of super type you can use in various contexts, like
[01:11] you can use an interface type to declare a variable, whether it can be an instance variable, static
[01:17] variable, or local variable, or you can also use
[01:20] these interface type variables or references as an method input parameter types.
[01:27] Additionally, if needed, you can also use them as an return type of a method.
[01:32] When you use your super type variable names inside your business logic, it is going to allow you to
[01:39] build the common utility logic that is going to work for all your implementation classes.
[01:45] That's what we also saw here previously.
[01:47] You can see here I have a static method to this method
[01:51] I'm trying to use the variable of super type which is SuperHero.
[01:56] Since I'm using the variable of super type, this method is going to work for all type of implementation
[02:04] classes like SpiderMan, CaptainAmerica, and IronMan.
[02:08] So there are certain rules and regulations that you need to be aware whenever you are trying to establish
[02:14] the super type and subtype relationship as part of the variable declarations or object assignments or
[02:20] objects creation.
[02:21] So let's try to understand those rules and regulations.
[02:24] First
[02:24] like you can see we have three different implementation classes like IronMan, SpiderMan and
[02:30] CaptainAmerica.
[02:31] All these implementation classes, they have the super type relationship with the SuperHero and Person
[02:38] interface.
[02:38] So for this SuperHero and Person interface, all these classes, they are going to act as a subtype.
[02:44] So with this assumption let's try to discuss various code snippets.
[02:49] The very first example I have is,
[02:51] here I'm trying to create the object of Person, but do you think it is going to be allowed?
[02:56] off course not.
[02:56] This code compilation is going to fail because we cannot create an object of an interface.
[03:02] So Person is an interface
[03:04] and if I try to create an object of an interface, I'm going to get a compilation error.
[03:09] The same applies for the SuperHero as well.
[03:11] If I try to create the SuperHero interface object, the compilation is going to fail.
[03:16] Now let's see the next code snippet
[03:19] here,
[03:19] I'm trying to create an object of IronMan, and the same I'm trying to assign to the variable of type
[03:25] IronMan itself.
[03:26] So this is completely acceptable because you are trying to create an object of a class.
[03:31] The same kind of behavior applies for other classes that we have here, like SpiderMan and
[03:36] CaptainAmerica.
[03:36] But now coming to the interesting part, you can see on the left hand side, I'm trying to have an variable
[03:43] of type, IronMan, but on the right hand side, I'm trying to create the object of SuperHero, which
[03:49] is an interface.
[03:50] So this compilation is going to fail because we cannot create the object of an interface at any cost.
[03:58] The same applies for Person interface as well.
[04:01] But if I try to swap these expression like on the left hand side, I can have an variable of SuperHero
[04:08] inside this variable.
[04:09] I'm trying to assign the object of IronMan, and similarly, if I try to assign the object of SpiderMan
[04:16] and CaptainAmerica, it is going to be compiled successfully because we are trying to create an object
[04:23] of subtype, and the same we are trying to assign to the variable of super type.
[04:28] If you try to apply the common sense here, every IronMan we can call it as superhero, but every superhero
[04:35] we can't call as IronMan.
[04:38] So always apply your common sense.
[04:40] If it is not making sense, then you can assume the compiler is also not going to compile the given
[04:46] expression the same kind of behavior.
[04:48] You can also see if you try to use the Person super interface variable reference on the left hand side.
[04:55] The compilation is going to be successful because you are trying to assign the
[05:00] object of subtype class to the super type interface.
[05:04] Let's try to see more examples.
[05:06] If you see here
[05:07] this may look very similar to the Upcasting, but we should not consider this as an upcasting because
[05:13] in the scenario of upcasting, both on the left hand side and the right hand side, you're going to
[05:18] have class data types.
[05:20] But here you can see on the left hand side we have interface data type like SuperHero and Person the
[05:26] same we discussed in the previous slide as well.
[05:27] But I have highlighted one more time here saying that this may look like Upcasting, but don't consider
[05:32] this as an Upcasting this just an normal assigning of an object to the variable of super type interface.
[05:39] Now let's try to take one more example here.
[05:42] We know these expressions
[05:44] the compilations is going to fail because we are not allowed to create the objects of our interfaces.
[05:50] That's why the compilation is going to fail.
[05:53] And whenever you see these kind of expressions, please always check what do you have on the right hand
[05:59] side?
[05:59] Do you have an interface or do you have an implementation class?
[06:03] Accordingly, you can conclude whether the compilation is going to fail or successful, or you can also
[06:09] apply common sense in these kind of scenarios
[06:11] also can every Person be a SpiderMan?
[06:14] Oof course not.
[06:15] But we can say that every SpiderMan is a Person.
[06:19] The next example that we have here is you can see first, I'm trying to create the object of SpiderMan.
[06:24] Post that in the second line, I'm trying to assign the object of IronMan to the super type Person,
[06:31] using these variables like SpiderMan and Person.
[06:34] If I try to write an expression like SpiderMan is equal to Person.
[06:38] Oof course this is not going to be allowed because according to your compiler, Person is an interface
[06:45] data type.
[06:46] That is why it is not going to allow you to assign the interface variable type to the class variable
[06:53] type, whereas the vice versa is allowed because you are trying to assign the subtype of Person interface,
[07:01] which is SpiderMan, to the super type interface variable, which is Person.
[07:05] But if you see inside this third statement, this should also work.
[07:10] If we give an assurance to the compiler saying that though, I'm using the super type reference variable
[07:16] like Person, but inside this person I have an actual object of subtype.
[07:22] If you can give that kind of assurance to your compiler, then it is not going to throw any compilation
[07:27] error.
[07:28] So how to give that assurance by doing the manual casting.
[07:32] So let's try to understand how to do that.
[07:34] So if you take the same scenario I know that my Person variable is holding the IronMan object.
[07:42] So if I'm sure about this then I can do the manual casting like you can see at the last statement.
[07:48] So since I'm doing the manual casting in this scenario, the compilation error will not be throwed because
[07:54] we are manually giving an assurance to the compiler inside this Person variable, which is of type interface.
[08:01] I'm holding an object of type IronMan.
[08:04] That's why I'm trying to do the casting, so please allow it to are trying to request to the compiler,
[08:09] and the compiler is going to accept during the compilation time.
[08:13] But at the runtime, if it is not seeing an object of IronMan inside this Person variable, then it
[08:20] is simply going to throw an ClassCastEexception.
[08:23] This is going to work very similar to the superclass and subclass inheritance that we discussed in the
[08:29] previous sections.
[08:31] When we are discussing about the downcasting, we did the same kind of manual casting, and in the same
[08:36] process I also showed you a ClassCastExceptionDemo. The same kind of behavior you will also see
[08:43] in this example as well.
[08:44] That's why I'm not showing the demos again, in case if you want to avoid runtime surprises in the form
[08:50] of ClassCastException,
[08:52] just like how we use the instance of operator in the scenario of superclass and subclass.
[08:58] Even in this scenario
[09:00] also, we can use the instanceof operator.
[09:03] So before I try to do these manual casting, first I can check if my person variable is holding the
[09:10] object of type IronMan.
[09:12] If this is true, then only I'm going to perform the casting.
[09:16] Otherwise we are not going to perform the casting.
[09:19] Instead of instanceof operator, you can also use the pattern matching instance of operator as well,
[09:25] which is available from Java 16.
[09:28] So you can see I am trying to check if this person variable is holding the object of IronMan.
[09:35] If it is, then I'm trying to immediately cast this Person to the IronMan variable.
[09:41] So inside my if block I can directly start using these IronMan with the confidence that the object
[09:47] present inside this person variable is automatically casted into this IronMan variable by my compiler,
[09:55] because this time I'm using the pattern matching instanceof
[09:59] syntax.
[10:00] I hope you are clear around these concepts.
[10:02] So please note that whenever you are creating an interface, it is going to create a new type or new
[10:07] data type.
[10:08] You can use this new data type to hold the objects of your implementation classes or subtypes, but
[10:15] please follow all the rules and regulations that we have discussed.
[10:18] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

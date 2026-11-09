# 11.3 — How to create an interface

> Section 11: Interfaces in Java

[00:00] Inside this lecture, let's try to understand how to create an interface inside Java projects.
[00:07] Below is the syntax that we can use to declare our to create an interface.
[00:13] So first we need to mention what is your access modifier.
[00:17] And mentioning the access modifier is completely optional.
[00:20] After the access modifier we need to use the keyword interface, and after mentioning this interface
[00:26] keyword, we can give any interface name by following the same naming conventions of Java class and
[00:34] post that we need to mention the curly braces
[00:36] and inside these curly braces we can write all the logic related to an interface.
[00:42] So what are all the components that we can write inside an interface?
[00:45] Inside an interface we can define static fields, abstract methods, default methods, private methods
[00:54] and static methods.
[00:55] So there is a lot to discuss about interface.
[00:58] For now let's focus on how to create an interface and how to define abstract methods inside an interface.
[01:06] Just like an abstract class inside interfaces
[01:09] also, we can define abstract methods, and since interface also going to contain abstract methods,
[01:15] Java is not going to allow you to create or to instantiate an object of interface.
[01:22] When we create an interface, it can only be implemented by other classes or extended by other interfaces.
[01:29] So let's see an example on how to create an interface like you can see here I'm trying to create an
[01:36] interface with the name SuperHero.
[01:38] And inside this SuperHero interface I have defined and static constant with the name universe name.
[01:45] And similarly I also have other two abstract methods like usePower() and stopVillain().
[01:52] Both of these methods are going to return String as an output and coming to the method input parameters.
[01:58] The usePower() method is not going to accept any method input parameter, whereas the stopVillain() it
[02:04] is going to accept a char value as an input.
[02:07] So here using this interface, I'm trying to provide a specification or a contract or a guideline that
[02:14] all the Marvel superhero classes has to follow.
[02:19] So anyone who are trying to build a Java class related to a marvel superhero, they need to make sure
[02:25] they are implementing these interface.
[02:28] And when they implement these interface, they will be forced to overwrite the abstract methods with
[02:34] the same method signature and method input parameters.
[02:37] So this way we are going to bring some consistency among all the superhero Java classes, since interfaces
[02:45] are mean to provide more of abstract methods, mentioning the abstract keyword inside the method signature
[02:53] of abstract methods is completely optional, because by default, inside an interface, whenever we
[02:59] are trying to define a method without any method body, then it is going to be considered as an abstract
[03:06] method.
[03:07] I hope you are clear.
[03:08] Let's try to understand more details about an interface.
[03:11] Whenever we are creating an interface, we don't have to mention the abstract keyword inside the interface
[03:17] definition, because by default every interface is considered as abstract only.
[03:24] That's why if you try to create a interface with the definition like public abstract interface SuperHero
[03:30] or public interface SuperHero, they both are going to have the same effect.
[03:35] Since abstract is going to be provided by the Java compiler behind the scenes, the developers, they
[03:41] don't have to mention this keyword inside the interface signature, but for abstract classes it is mandatory.
[03:48] The next point that I want to highlight here is both the classes and interfaces
[03:53] they have some significant differences.
[03:55] Like inside a class we can define instance fields, whereas inside interfaces we can't define instance
[04:02] fields.
[04:02] On the similar lines
[04:03] we can create an object of an Java class by instantiating, whereas we can't do the same with an interface.
[04:11] You will find a lot of similarities between an interface and abstract class, but there are few differences
[04:17] between abstract class and interface, which I'm going to discuss in the coming lectures.
[04:22] Like we discussed previously, inside a interface body, we can write abstract, default, private and
[04:28] static methods.
[04:29] So these are the four different kinds of methods that we can define inside an interface.
[04:34] We're going to discuss in detail about each of these methods in the coming lectures.
[04:39] For now please note that whenever you are defining abstract methods, you don't have to mention the
[04:45] abstract keyword.
[04:46] You can simply mention your method signature followed by a semicolon instead of braces and a method
[04:52] body.
[04:53] And when you want to define default methods, you need to use the default modifier while static methods
[04:59] they are going to
[05:00] have the static keyword.
[05:01] The beauty of interface is inside interface
[05:04] whenever you are trying to define abstract, default and static methods, they are implicitly considered
[05:10] as public by default, so the public modifier can be completely omitted inside the methods that you
[05:18] are trying to define inside an interface.
[05:21] But when you want to create private methods, then in that scenarios you can mention the private access
[05:27] modifier, which will remove the default public modifier provided by the interface.
[05:33] I hope you are clear on how to create an interface, so let's try to create an interface very quickly
[05:38] inside IntelliJ.
[05:39] Since we are into the new section, which is section 11, I have created a Java project with the name
[05:45] section_11.
[05:47] Every example that we are going to discuss around interfaces, I'm going to create all of them inside
[05:53] these section_11 Java project.
[05:55] The same you can check inside the GitHub repo as well.
[05:58] So inside src folder as of now you can see it is empty.
[06:01] First I want to create a package.
[06:04] The package name that I'm going to give here is com.ezsybytes.madewell.zero.
[06:11] So inside this package only I'm going to create a new interface.
[06:16] So when you want to create a new interface, select the new Java class option and post that
[06:21] inside this dropdown, select the interface as an option so you can see the icon for the interface is
[06:27] going to be eye.
[06:28] So here I'm going to mention the interface name as SuperHero.
[06:32] So as soon as I press enter you'll be able to see a empty interface is created by my IntelliJ.
[06:39] So the syntax that we are following is public interface SuperHero instead of public
[06:44] you can also mention that default by just removing the public access modifier.
[06:49] So when you define an interface with the default package level access modifier, then it can only be
[06:56] inherited by the classes present inside the same package.
[07:00] Apart from public and default, we cannot provide any other access modifier.
[07:05] For example, I can't mention private,
[07:08] you can see I'm getting an compilation error in the similar lines
[07:12] I can't provide protected as well.
[07:15] So that's why always make sure you are either defining public or you are going with the default access
[07:22] modifier.
[07:22] So once you have defined the interface inside interface, we can create a static field and abstract
[07:29] methods and other types of methods.
[07:31] For now let's focus on creating only abstract method.
[07:35] So the abstract method that I want to create here is, public string usePower().
[07:41] So use power is a method name and post that we can mention the semicolon.
[07:45] So this is going to be abstract method.
[07:48] And like we discussed inside an interface we don't have to mention the abstract keyword because by default
[07:55] all the methods where they don't have any method, body or method logic, they will be considered as
[08:01] an abstract method by the interface.
[08:03] On top of that, we don't have to mention the public access modifier as well, because inside interface
[08:09] all methods are implicitly considered as public.
[08:12] That's why I'm getting an warning saying that modifier public is redundant
[08:17] for interface members. I can select this option, which is remove public modifier which which will
[08:22] remove the public access modifier from the method signature.
[08:26] In the similar lines, I can create one more abstract method with the name stopVillain().
[08:33] And to this method I want to send the method input parameter of type char.
[08:38] So it is going to accept a char, and based upon what I receive inside this char keyword, the SuperHero
[08:45] has to react accordingly.
[08:47] For example, if I send the char value as y, then he need to kill the villain, whereas if I send the
[08:54] char value as no, then in such scenarios the SuperHero should not kill the villain.
[09:00] Instead, he should stop him or he should arrest him.
[09:04] So let's try to update the same inside the method
[09:07] comments around this method.
[09:09] Here I'm going to mention the method comment, saying that if y received kill the villain.
[09:17] If n received, stop the villain.
[09:21] So these are my requirements.
[09:23] The same I'm trying to convey as part of my Java comments, so that whoever is trying to implement my
[09:29] interface, they will understand this requirement and accordingly, they are going to write the business logic.
[09:34] For the parameter,
[09:36] we can say @Param c indicates y or n.
[09:40] Similarly, @Return we can mention, returns the status.
[09:46] So these are the basic Java commands that I want to provide here.
[09:49] If needed, you can further optimize them based upon your understanding.
[09:53] This way we can successfully create any number of interfaces and inside the
[09:59] interfaces
[10:00] we can define a contract or a specification that all the implementation classes has to follow.
[10:06] I hope you're clear with this process.
[10:08] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

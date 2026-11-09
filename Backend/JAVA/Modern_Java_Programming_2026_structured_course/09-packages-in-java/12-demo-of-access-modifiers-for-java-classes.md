# 9.12 — Demo of access modifiers for java classes

> Section 9: packages in Java

[00:00] Let's see the demo of access modifiers inside this lecture.
[00:04] First, I'm going to show you how to use this access modifiers on top of a class definition.
[00:09] For the same
[00:10] let me open one of the class that I have, which is Employee.
[00:13] You can see I have defined my class definition with the help of public access modifier.
[00:19] Let me try using the private for my class definition.
[00:24] I should be getting a compilation error.
[00:26] So you can see whenever I try to use a private access modifier for the class definition, I'm going
[00:33] to get a compilation error.
[00:35] The reason is, if you make your class as a private, no one can access your class, including the JVM
[00:42] as well.
[00:43] That's why if you have only a single class inside your Java class definition, using of private and
[00:51] protected is not allowed.
[00:53] Similarly, I can also type protected here, so even if I try to use protected also, I'm going to get
[00:59] a compilation error saying that modifier protected not allowed here.
[01:05] Then you may have a question under which scenarios I can use private and protected for the classes.
[01:11] The answer is very simple.
[01:12] If you end up creating the inner class as part of this outer class, then for the inner class you can
[01:20] define the private and protected.
[01:22] I'm going to show you a demo of inner classes in a few minutes, but for now let's focus on outer class
[01:29] or the scenario where we are going to have a single class inside your source file.
[01:33] By now it should be pretty clear for you.
[01:35] Protected and private are not allowed for the outer classes, or if you have only a single class inside
[01:42] your source file, how about default.
[01:44] If I don't mention any access modifier, then behind the scenes JVM is going to consider the default
[01:52] access modifier.
[01:53] I hope this is clear.
[01:54] Let me bring back public to my Employee class.
[01:58] So as of now, since I have defined the public access modifier for this class, anyone can access my
[02:05] class and they can create an object, and after that object is created, they should be able to access
[02:11] all the fields and methods that my class may have the same.
[02:15] We can also see here.
[02:16] Inside the Main class we're able to create the object of Employee class, even though my Main class
[02:23] is present inside another package which is com.eazybytes.app.
[02:28] So this confirms whenever we use a public access modifier for a class.
[02:33] The same can be accessed from anywhere inside your Java project, even from outside of your package.
[02:39] Now let me remove these public access modifier.
[02:43] When we remove this public access modifier, this means we are telling to the JVM a Java.
[02:49] I want to allow my class to be accessed only within the same package, but not by any class outside
[02:55] of the package.
[02:56] Now if I go to the Main class which is present inside another package, you can see I'm getting a compilation
[03:02] error saying that it cannot be accessed from outside of the package.
[03:06] So IntelliJ Idea is recommending if we want to access this Employee class from the Main class, we need
[03:12] to make it as public.
[03:14] Otherwise this compilation error is not going to be resolved.
[03:17] Whereas if I try to paste the same Main class inside the model package this time, the compilation error
[03:25] will not be there.
[03:26] If you see the Main class right now is present inside the com.eazybytes.model where my Employee
[03:32] class is present.
[03:33] Here, you're not seeing any compilation error.
[03:36] The reason is you're trying to access this class from the same package.
[03:40] So that's a power of default access modifier.
[03:44] I hope you're clear.
[03:45] Now let me remove these Main class that I have copied just now post that I'm also going to make my Employee
[03:52] as public to resolve the compilation error that we have inside the main class of com.eazybytes.app.
[03:58] .
[03:59] Now, before I try to show you how to create the inner classes, let me go to my intelliJ preferences.
[04:06] In the previous lectures we have unchecked all these options.
[04:09] So let me check all those options and click okay.
[04:13] Post that my intelliJ can do some optimizations in terms of import statements.
[04:18] So now this looks good.
[04:20] As a next step, let me create a class inside my app package.
[04:24] So the class name that I'm going to give here is MyOuterClass.
[04:29] Like I said before, inside a class we can create another class.
[04:33] So let me try to create an inner class here.
[04:36] As of now, I'm not trying to teach you everything about the inner class.
[04:39] I'll just give a small demo of inner class and how we can change the access modifiers of the inner class
[04:46] to control the accessibility of the inner class, with the help of access modifiers that we have defined
[04:51] more details about the inner class we are going to discuss towards the end of the course.
[04:56] The reason is inner class are somewhat advanced in
[04:59] nature and complex to understand.
[05:02] On top of that, inner classes are rarely used by developers in real projects as well.
[05:08] Most of the times developers they'll only create a single class inside a source file.
[05:14] I hope you are clear now inside my outer class, let me try to create an inner class for the same inside
[05:20] the curly braces.
[05:22] I'm going to create a new class with the definition as public and after the public
[05:28] I'm going to mention static, followed by class and the class name I'm going to give as MyInnerClass.
[05:35] And inside this inner class I can create a method which is public void display().
[05:43] And inside this method I'm going to simply use a System.out.println(), which is going to print hello
[05:50] from inner class.
[05:52] So here you might be seeing some new syntaxes, which is
[05:56] as part of the class definition, I'm able to use a static keyword.
[06:00] So this is allowed in Java whenever you are trying to create an inner class.
[06:05] Whereas if you try to mention the same static keyword for the outer class, it is not allowed.
[06:11] So please make a note of it.
[06:13] When we discuss more details about the inner class, I'm going to share more details.
[06:17] For now, I'm assuming this code is super clear for you.
[06:20] There is a inner class as part of an outer class, and this inner class is marked as static
[06:26] and inside this inner class we have a method display().
[06:29] So my inner class is marked as public.
[06:32] Now I'll go to my Main class, and I'll try to create an object of my inner class. For the same,
[06:39] here I'm going to type my inner class name, which is my inner class.
[06:44] As soon as I type my inner class and press enter, you can see the syntax to access my inner class is
[06:51] first we need to mention what is the outer class, followed by my inner class.
[06:56] So we're able to access this my inner class without creating the object of my outer class, because
[07:02] we marked the inner class as static class.
[07:04] Post that, let me give an object reference name, which is myInnerClass, followed by new operator
[07:10] and at lost
[07:11] I'm going to mention my inner class default constructor.
[07:15] Now from this object of myInnerClass, I can access the method which is display() present inside the
[07:22] inner class.
[07:22] So if I try to execute this program, I'll be able to see an output which is hello from inner class
[07:28] inside my console.
[07:30] So up to this point I'm assuming you're clear.
[07:32] Now let me go to my my outer class this time
[07:35] if I try to make this private, there should be a compilation error here, even though my Main class
[07:42] is present inside the same package where my outer class is present.
[07:46] Still, it will not be able to access because we use the access modifier private for my inner class,
[07:54] whereas if I just mention the protected in this scenario, the compilation error is going to be resolved.
[08:00] The reason is when we mention the protected any class which is present inside the same package, they
[08:06] should be able to access your class.
[08:08] But if a class is present outside of your package, then that class should be a subclass of your class
[08:13] where you have defined protected.
[08:15] For example, if I try to create the same Main class inside the model package inside this Main class
[08:21] which is present inside the model package, I'm going to get a compilation error.
[08:24] The reason is we mentioned the access modifier of my inner class as protected.
[08:30] Since my Main class, which is present inside the model package, it is present outside of the package
[08:35] and it is not a subclass of my class.
[08:37] That's why it is not able to access my inner class.
[08:40] I hope you're clear.
[08:41] Let me delete this Main class that I have copied inside the model package.
[08:45] Post that I'll go to my my outer class and here
[08:49] this time I'll just remove all the access modifier.
[08:52] That means behind the scenes, my JVM is going to use the default access modifier.
[08:58] With this they should not be any compilation error.
[09:01] The reason is when we use the default access modifier, any class inside your package should be able
[09:07] to access your class.
[09:09] I hope you're clear.
[09:10] Now let me show you another important point, which is this time I'll just try to make private
[09:16] as soon as I try to make private.
[09:18] you can see I'm getting a compilation error here and I will not be able to access the display() method
[09:23] even though it is marked as public.
[09:25] The reason is, whenever we want to access a method or a field present inside a class definition, first
[09:32] we need to be able to access the class.
[09:35] Without able to access the class, we cannot access any method or a Java field even though they marked
[09:41] as public.
[09:42] I hope you are clear about this important point here
[09:45] I'm going to simply remove these private access modifier and I'm going to keep this code like this for
[09:50] your reference.
[09:51] I hope you are clear on how to use the access modifiers inside your class definitions.
[09:56] In the next lecture, let's try to understand how to mention
[09:59] access modifier on top of the Java fields and Java methods.
[10:03] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

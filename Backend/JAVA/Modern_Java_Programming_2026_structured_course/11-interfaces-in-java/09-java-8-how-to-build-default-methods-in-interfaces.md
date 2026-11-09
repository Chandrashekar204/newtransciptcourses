# 11.9 — [JAVA 8] How to build default methods in interfaces

> Section 11: Interfaces in Java

[00:00] Think like, I want to introduce a new abstract method inside my SuperHero interface.
[00:06] So here I'm going to type String and the method name is going to be trackLiveLocation().
[00:13] Using this abstract method I want to tell to all my subclasses are implementation classes.
[00:19] To override this method and mention the business logic indicating about the live location of a specific
[00:26] hero.
[00:27] So as soon as I try to add these abstract method, this may look very simple on my side, but with that
[00:34] all the implementation classes they are going to get an compilation error.
[00:38] That means immediately all your subclasses are implementation classes
[00:44] they will be forced to override your abstract method in real projects.
[00:50] The development and the decisions will not happen so quickly.
[00:54] People will need years and years of time to build an enhancement by properly testing it and integrating
[01:01] with other components.
[01:03] That's why we should never force the implementation classes about the new feature that is trying to
[01:10] be introduced inside an interface.
[01:12] So to resolve this issue, we can go with the default methods.
[01:16] So whenever we want to write a default method inside an interface, we need to start the method signature
[01:24] with the word default.
[01:25] So as soon as I mentioned default, you can see now my Java is forcing me to define business logic inside
[01:32] the method body.
[01:33] That means each and every default method, which we are trying to define inside an interface, should
[01:39] definitely have a method body our implementation logic.
[01:44] That's why I'm trying to mention the curly braces.
[01:46] And inside these curly braces I'm going to write the logic like String liveLocation is a variable.
[01:55] And to this I want to assign a value, which is USA, because most of the superheroes they stay inside
[02:03] USA.
[02:03] So that's why I want to go with this default value followed by I want to mention System.out.println()
[02:09] and to the println()
[02:11] we can pass a statement which is I am in followed by
[02:16] I can try to append the live location, and at last we can try to return the variable which is
[02:22] liveLocation.
[02:23] So this is the default method that we have created.
[02:26] As soon as I changed my abstract method into a default method
[02:30] now if you go to the implementation classes, all the compilation errors will get resolved.
[02:35] On top of that, each of my implement class they are also going to inherit the default method from the
[02:42] interface like TrackLocation.
[02:44] So if needed my individual implementation classes, they can override the default method, or they can
[02:52] live with the default behavior, or they can completely ignore and do not make any changes inside the
[02:59] implementation classes.
[03:00] Whenever you're trying to define a default method, please make sure we can't define default method
[03:07] as abstract because it is going to always have the implementation logic or the business logic.
[03:13] And apart from abstract, we are not allowed to mention static as well
[03:18] like I can't create a static default method, it is not allowed.
[03:22] Now let's try to understand how to override these default methods, which are available inside an interface
[03:28] inside any of the implementation class.
[03:31] For example, if I want to override these default method inside my SpiderMan subclass, I can directly
[03:38] go to my SpiderMan and I can try to mention the same method
[03:43] on top of that, I can mention the Override annotation.
[03:46] But before you try to override, please make sure you are removing these default keyword.
[03:52] Because default methods are only allowed inside an interface instead of default, we should make sure
[03:59] we are mentioning the public.
[04:01] And with that, you can see now I should be able to write whatever logic inside my trackLiveLocation()
[04:08] method with the business logic related to SpiderMan.
[04:12] For example, think like if SpiderMan is in London, so he can simply mention London and the same he
[04:19] can return whoever is trying to invoke this
[04:22] trackLiveLocation() method.
[04:23] I hope you are clear on how to override a default method.
[04:26] The thumb rule is the default methods we can't create in any of the classes.
[04:31] Default methods are only allowed inside the interface.
[04:35] That's why you need to make sure you are removing this default keyword inside your implementation classes.
[04:41] On top of that, if needed, you can mention this Override annotation, but this is completely optional,
[04:46] but I would always recommend you to maintain this annotation for better readability.
[04:52] The next point that I want to highlight here is, when Java team decided to allow the default methods
[04:57] inside Java 8.
[04:58] They
[04:59] end up writing a lot of default method in many of the interfaces.
[05:04] When a developer is writing a lot of default methods, which is going to have a lot of business logic,
[05:10] at some point of time, they are going to hold some common business functionality, which needed by
[05:16] multiple default methods inside the same interface.
[05:19] So to avoid that repetition of the business logic in multiple default methods, Java team provided a
[05:26] flexibility to define private methods in interface from Java 9, for example
[05:33] I can also show you a demo here.
[05:34] So here you can see as of now I have a default method.
[05:38] Very similarly, I will be able to create the private methods inside an interface by mentioning private
[05:45] access modifier along with the proper method name.
[05:49] Maybe I can try to change this method name to method1().
[05:52] And you can see now my interface is going to have this method1().
[05:56] And inside this method1() I can define a common logic that can be shared by multiple default methods
[06:04] inside my interface.
[06:05] So whatever private methods that you are going to define inside your interface, they are not going
[06:11] to be inherited by your implementation classes.
[06:14] These private methods are strictly for your default methods
[06:18] common business logic. I hope you are clear at this point of time
[06:22] since we have only single default method, it is not going to make sense to have this private method.
[06:27] So let me remove this.
[06:29] All the important points that we discussed around the default methods in interface I have mentioned
[06:34] in these two slides.
[06:36] So please read them whenever you want to quickly revise about the default methods in interface.
[06:42] With this we left only with the static methods, so let's try to understand the same in the next lecture.
[06:48] Thank you,
[06:49] bye.

----------------------------------------

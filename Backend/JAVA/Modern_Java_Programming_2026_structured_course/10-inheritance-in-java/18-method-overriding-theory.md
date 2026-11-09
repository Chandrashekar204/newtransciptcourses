# 10.18 — Method Overriding - Theory

> Section 10: Inheritance in Java

[00:00] Before I try to explain you about what is a method overriding inside Java inheritance, first let me
[00:07] ask you a question.
[00:08] Think like you have inherited a property from your parents.
[00:13] Are you going to keep that property forever without making any changes?
[00:18] Off course you're not going to do that
[00:21] maybe at some point of time, if you have your own requirements or if you want to change it, you will
[00:27] go ahead and change the property.
[00:29] Maybe you will go for repainting or renovation based upon your taste, though the property is inherited
[00:36] from your parents. Very similarly inside Java,
[00:40] also, if a subclass is inheriting a method from the parent class, it is not mandatory to accept the
[00:48] same method and to follow the same logic given by the parent forever.
[00:53] If a subclass has a requirement to override the behavior provided by the superclass method, then it
[01:01] is perfectly allowed inside Java.
[01:04] So this concept we call it as method overriding.
[01:07] So what is a method overriding?
[01:09] Method overriding is a feature of Java inheritance that allows a subclass to provide its own implementation
[01:18] of a method that is already defined in its parent class.
[01:22] So this is the simple definition that you can tell if someone is asking what is a method overriding?
[01:28] While we are trying to perform the method overriding inside a subclass, we need to make sure we are
[01:33] defining a method with the same method name, same return type, and same method parameters,
[01:40] as mentioned in the parent class method, the access modifier or
[01:45] the access level of the overriding method can be different from the superclass method, but you need
[01:52] to make sure the access modifier is not more restrictive than the method being overridden. In few minutes
[02:00] I'm going to show you a demo around this, so don't worry if something is not clear for you.
[02:04] So when you have a method both in the parent class and a subclass, and if you're trying to invoke the
[02:11] method name with the object reference of the parent class like we discussed in the Upcasting in such
[02:18] scenarios, first your JVM is going to look if there is any method in the subclass which is overridden.
[02:25] If yes, the same is going to be invoked at the runtime.
[02:29] Otherwise, whatever method defined inside the superclass or the parent class is going to be invoked.
[02:35] So the concept of method overriding inside Java provides great flexibility and customization in the
[02:41] behavior of objects in the subclass.
[02:44] If we don't have method overriding concept inside Java, then inheritance is not going to be a great
[02:50] feature, because if you inherit something, then you have to live with that.
[02:54] There is no option of changing.
[02:56] Are you going to accept such kind of behavior?
[02:59] Off course not.
[02:59] Each one of us, we always want our own freedom, our own thinking
[03:04] though we inherit the properties or the characters from our parents.
[03:09] Very similarly, inside Java, also, with the help of method overriding, we are giving the flexibility
[03:14] to the subclasses.
[03:15] If they want, they can override the business logic provided by a method inside the superclass.
[03:22] But whatever method overriding that we are discussing right now, this applicable only to the non-static
[03:29] methods.
[03:29] Static methods
[03:31] we can't override them because static methods are only applicable at the class level.
[03:36] It is not belongs to a specific object.
[03:39] With that reason, we cannot perform the method overriding.
[03:42] Instead, whenever we are dealing with the static methods, we can call that concept as method hiding.
[03:48] We are going to talk about what is method hiding in the coming lectures, but for now, please note
[03:53] that method overriding concept is applicable only for the non-static methods and obviously the private
[04:00] methods which are present inside the superclass.
[04:03] They can't be overridden by a subclass because the private methods present inside the superclass, they
[04:10] are going to be never inherited by the subclass.
[04:13] So let's try to take an example around method overriding.
[04:16] Like you can see here, I have a parent with the name Person.
[04:20] So that's why I'm trying to extend the same Person superclass inside my IronMan subclass.
[04:26] So inside my Person superclass we created a method with the name walk().
[04:31] But the IronMan, he's not going to walk like other persons.
[04:36] He's walking style is going to be something different, maybe due to his iron suit.
[04:41] So since he has his own style of walking, it makes very sense to the IronMan to override the method
[04:49] that he's inheriting from the Person.
[04:51] Whereas for the CaptainAmerica, you don't need to override the walk() method, because CaptainAmerica
[04:57] is going to walk very normally like
[04:59] humans, whereas for the IronMan, since he has iron suits, sometimes he's going to fly and sometimes
[05:06] he's going to walk.
[05:07] And when he's walking, we're going to get a lot of sound like tuck, tuck, tuck.
[05:12] So since he has his own walking style, I'm trying to overwrite the walk() method inside the IronMan
[05:19] class.
[05:19] So when we are overriding, we need to make sure we are mentioning the same method name, same method
[05:25] return type, and same method parameters along with the access modifier.
[05:30] So that's why I'm trying to mention the same, which is public void walk().
[05:34] And inside this method I can write my own business logic and whenever we are trying to do a method overriding,
[05:40] it is always advisable to mention an annotation which is @Override on top of your overridden
[05:49] method inside your subclass.
[05:50] So here I have mentioned an annotation which is at symbol followed by Override.
[05:56] Inside Java all annotations
[05:58] they are going to be represented with the help of this at symbol.
[06:02] With that you may have a question here,
[06:04] why should I mention this annotation?
[06:06] Because I said it is an optional.
[06:08] But the question you may have is since if it is optional, then why should I mention this annotation?
[06:14] What is the advantage that I get?
[06:15] So I perfectly understand your question.
[06:17] Let me try to answer that.
[06:19] Whenever we mention these Override annotation on top of your overridden method, your compiler understands
[06:26] that you are trying to override the walk() method present inside the superclass, and if you try to miss
[06:34] one of the rule of method overriding, maybe you're trying to give a different return type
[06:38] or maybe you're trying to accept a different method
[06:41] parameters,
[06:42] in all such scenarios, since your Java compiler knows that you're trying to override a superclass method,
[06:48] it is going to throw a compilation error and it is going to warn you saying that hey, you didn't follow
[06:54] so-and-so rule while you are trying to override so on and so method from the superclass.
[06:58] Whereas if I don't have these Override annotation, then my compiler does not know and it will simply
[07:05] treat it as a normal method, and it is not going to guide me in the process of method overriding.
[07:11] On top of that, one more advantage we have with the @Override annotation is,
[07:16] if you mention these @Override annotation on top of a overridden method, and if there is
[07:21] no method with the same name inside the superclass in such scenario
[07:25] also you're going to get a compilation error saying that hey buddy, you're trying to override a method
[07:31] with a so and so name, but I don't find such method inside the superclass, so please do check your
[07:37] method name.
[07:38] So this kind of guidance is going to be provided by the compiler when we follow the Override annotation.
[07:45] I hope you're clear.
[07:46] Now the next question you may have here is I'm hearing the annotation very first time from you,
[07:53] can you please share more details about what is an annotation in Java?
[07:58] Let me try to answer the same inside Java, annotations are a form of metadata that provides information
[08:06] about a program's code, particularly its classes, methods, fields, and parameters.
[08:12] I know this definition does not make any sense, but let me try to make it more simple to you.
[08:18] So whenever you are using an annotation inside Java, we are going to convey an information to the compiler
[08:25] or runtime or other tools that process the program.
[08:29] For example, here I have a method and this is going to be processed by my compiler, by my JVM or other
[08:36] tools of Java.
[08:37] So if I mention these @Override annotation,
[08:40] so there'll be a meaning assigned to this annotation behind the scenes.
[08:44] So using the same meaning, my compiler can guide the developers on how to override a method.
[08:51] So very similarly we have lot many annotations inside Java.
[08:55] So inside Java,
[08:56] please note that all these annotations they are going to start with at symbol.
[09:01] So whenever you see an annotation being used inside Java programming language, first you need to understand
[09:07] what is the purpose of that annotation and under which scenarios we need to use that annotation.
[09:12] So throughout this course we are going to talk about lot many annotations.
[09:16] So if you are clear about these most commonly used annotations you should be good.
[09:21] Once you become an advanced Java developer, maybe after five years or six years of Java programming
[09:26] experience, you can also create your own annotations.
[09:30] So that is also possible inside Java.
[09:32] But for now, since you are getting started just now, I would advise you to get comfortable with the
[09:38] most commonly used annotations, which I'm going to discuss throughout this section.
[09:43] I hope you are clear about what is a method overriding inside Java inheritance.
[09:47] In the next lecture, let me show you a demo of method overriding.
[09:52] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

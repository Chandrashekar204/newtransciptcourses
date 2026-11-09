# 9.14 — access modifiers real life analogies

> Section 9: packages in Java

[00:00] With all the demos that we saw in the previous lectures about the access modifiers, it should be pretty
[00:05] clear for you when to use these access modifiers and how to use them.
[00:09] But if you have still confusion, or if you have challenges to remember them, I want to solve them
[00:15] by providing a real life example or analogy.
[00:19] The example that I want to share is about the toilets that we use on our day to day basis.
[00:25] Whenever someone says public, please always think like
[00:29] these are very similar to the public toilets that governments maintain throughout the city or throughout
[00:35] the country.
[00:36] So how these public toilets work, anyone can enter into these public toilets and use them at free of
[00:43] cost or with a minimum fare.
[00:45] Very similarly, when you make your class or Java fields or Java methods as public, anyone can access
[00:52] them.
[00:52] I hope you are able to correlate between the public toilets and the public access modifier that we have
[00:58] discussed.
[00:58] Moving on to the next access modifier, which is private.
[01:02] When someone says private access modifier, always think about the toilets that you have inside your
[01:08] own house.
[01:09] So who can access the toilets inside your house?
[01:12] Only the members of your family are only the persons who are staying inside the house,
[01:18] they can only access the private toilets.
[01:21] Very similarly, if you define Java fields and Java methods and Java classes with the help of private
[01:29] keyword, they will be accessible only within the same Java class.
[01:34] I hope you are liking this analogy.
[01:36] Moving on to the next access modifier, which is default, inside the default scenario, think like the
[01:43] toilets that you are going to have inside an office building.
[01:46] You might be working inside an office and inside your office you may have toilets.
[01:51] So who can access these toilets?
[01:53] Only the employees who are working in that office
[01:56] they can only access these toilets.
[01:59] No other public
[02:00] they can walk in into your office toilets.
[02:03] So this is very similar to that default access modifier.
[02:07] So when we define default members inside our Java classes, we should be able to access those default
[02:13] fields or default methods only from the within the same package.
[02:19] And at last we have protected scenario regarding protected access modifier
[02:24] if there is a toilet inside the shared apartment, you can use yourself or the guest who are visiting
[02:30] you
[02:30] they can also use the shared apartment toilet.
[02:33] So this is very similar to the protected when we use the protected keyword, any class which is present
[02:39] inside the same package, it should be able to access the protected variables and protected methods.
[02:46] So this is similar to anyone who are staying inside the same apartment
[02:50] they can access the shared toilet, apart from the classes present inside the same Java package, the
[02:56] subclasses present inside other packages, they can also access the protected members.
[03:01] So this is very similar to that guest visiting to your apartment.
[03:06] So any authorized guest who are visiting your apartments, they should be able to access the shared
[03:12] toilets available inside the apartment.
[03:15] I hope you are clear with this analogy for your reference
[03:18] I also provided a detailed table.
[03:21] Here inside this table on the left hand side I have mentioned various scenarios like same class subclass
[03:27] inside the same package,
[03:28] non subclass in the same package,
[03:30] subclass in different package,
[03:32] non subclass in different package.
[03:34] If you see for public all type of classes, they will be able to access your Java fields, Java methods
[03:42] and inner classes.
[03:43] But coming to the private only the same class should be able to access the private methods, private
[03:50] classes and private variables, whereas for that default only the classes and subclasses present inside
[03:57] the same package, they will be able to access all the subclasses or non subclasses in different packages,
[04:04] they will not be able to access your fields and methods and inner classes.
[04:09] And at last for the protected all type of classes except these non subclasses which are present inside
[04:15] different packages.
[04:16] All the remaining classes or subclasses
[04:19] they will be able to access your protected variables and protected methods.
[04:24] So if you closely observe these access modifiers.
[04:27] So the thumb rule that you need to follow whenever you are trying to define an access modifier for a
[04:32] field or for a method or for a Java class is first start with the private access modifier.
[04:38] If you feel there is a requirement where another class has to access your Java field or Java method,
[04:45] then upgrade that private to default.
[04:49] But even with the default, if you have some challenges where one of the subclass present inside the
[04:55] outside of the package needs to be access, then in such scenarios, you can upgrade the access
[05:00] modified to the protected and a class
[05:02] if the protected also is not solving your problem and you want to go with the public access modifier,
[05:07] you can go with the same.
[05:08] So always start with the private followed by default, followed by protected
[05:12] and at last you can consider the public.
[05:15] I'm assuming now you have better clarity around the access modifiers.
[05:18] Now, before I try to close this lecture, let me answer a burning question that you may have.
[05:23] The question that you may have here is, can we use these access modifiers for the local variables?
[05:29] We are going to create lot many local variables inside if blocks, for loops, while loops.
[05:34] So can we define this access modifiers for the local variables.
[05:38] Let's try to understand the same by quickly trying to create a local variable inside one of the method.
[05:43] Here I'm inside a public method, and inside my method I'm going to create a local variable which is
[05:49] int num = 9.
[05:51] So this is how we need to always create the local variables.
[05:55] Regardless whether you are trying to create inside a method or inside a for loop or while loop, or
[06:00] if block, if you try to provide the access modifiers to your local variables like I can try to provide
[06:05] private, I'm going to get a compilation error.
[06:08] The same will be happen if I try to use public or protected.
[06:12] So this confirms we're not allowed to use any access modifiers for all the local variables.
[06:19] So always please, please make sure you are providing the access modifier only for the class level instance
[06:25] variables or static variables like you can see on the screen.
[06:29] I hope this answers your question.
[06:31] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

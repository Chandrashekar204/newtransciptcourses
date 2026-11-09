# 9.13 — Demo of access modifiers for methods, fields in classes

> Section 9: packages in Java

[00:00] He not to show you the demo of access modifiers on top of Java fields and Java methods.
[00:05] Here I'm going to create a new Java class under the app package.
[00:10] So the Java class name I'm going to keep it as access modifiers demo inside this class
[00:17] first, let me create multiple variables or multiple Java fields with various access modifiers.
[00:24] First, let me mention private, followed by int and the variable name as privateVariable.
[00:31] So these are the name that I want to give to my int variable that I'm trying to create.
[00:37] So here it should be pretty clear for you.
[00:39] Whenever we want to create a Java field with the private access modifier, we just need to mention the
[00:45] private keyword.
[00:46] Very similarly, we can also try to create other kinds of variables for protected.
[00:52] We need to mention protected keyword and the variable name
[00:56] I'm going to change it to protectedVariable on the similar lines I can also mention public as well.
[01:04] So when we mention public keyword as part of the field declaration, the same can be accessed by anyone
[01:11] from any package as long as they're able to access my class.
[01:16] And at last, I can remove the keyword that will make my variable to have that default access modifier.
[01:22] So let me rename to default variable. On the similar lines
[01:26] I'm going to create multiple methods like public void.
[01:30] And to these I'm going to mention the method name as publicMethod().
[01:35] To keep this method simple, I'm not going to write any complex logic, just I'm going to print the
[01:41] statement which is hello from public method.
[01:46] Very similarly, I'm also going to create multiple other methods by using various access modifiers.
[01:53] So here I'm going to mention private and the method name
[01:56] I'll keep it as privateMethod().
[02:00] And I'll change the value inside the System.out.println() to hello from private method.
[02:06] Now as a next step, I'm going to remove this public and mention protected post that I'm going to rename
[02:12] this method to protectedMethod(), followed by
[02:17] I'll update the System.out.println() to hello from protected method.
[02:22] And at last I'm going to remove these access modifier, which will make my method to have that default
[02:28] access modifier.
[02:29] So let me change the method name to defaultMethod() and the System.out.println() statement to hello from
[02:37] default method.
[02:38] So this way you can create any number of methods and fields based upon your requirements by using the
[02:44] correct or valid access modifier.
[02:46] Now, as a next step, let's try to access all these fields and methods from another class
[02:52] and in the same process, we can try to understand the behavior of these fields and methods based upon
[02:58] the access modifiers that we have defined for the same
[03:01] I'll go to the Main class inside the Main class
[03:04] first, I'm going to create an object of my access modifier.
[03:08] Once the object of the access modifier class is created with the help of these access modifier, we
[03:15] should be able to access methods like defaultMethod(), public method().
[03:20] But you can see I'm not able to access privateMethod().
[03:24] If I type private, I don't have any recommendations.
[03:28] The reason is we will not be able to access any private methods or private fields from another Java
[03:34] class.
[03:35] So my Main class is able to access the access modifier demo, and it is able to create the object of
[03:40] this class.
[03:41] Still, I'm not able to access the private methods and private fields, whereas I'm able to access the
[03:47] publicMethod(), publicVariable.
[03:49] And similarly, I should be able to access the defaultMethod() and defaultVariable.
[03:54] And on the similar lines, I should be able to access the protectedMethod() and protectedVariable.
[03:59] So this confirms if your Java class is present inside the same package where your accessModifierDemo
[04:05] is present
[04:06] in such scenarios, you will be able to access all type of methods and fields except the private methods
[04:13] and private fields.
[04:14] I hope you are clear.
[04:15] Now if I try to keep these Main class inside another package like model package, this time I will have
[04:23] some restrictions.
[04:24] For example, using the accessModifiersDemo object, I will not be able to access the default methods
[04:32] and protected methods.
[04:34] I will be able to access only the public variable and public method, since right now my Main class
[04:41] is present inside another package.
[04:43] If your Main class is a subclass of your access modifier class, then in such scenarios you should be
[04:49] able to access the protectedVariable and protectedMethod.
[04:52] But as of now, we are ready to discuss about inheritance and how to make a class as a subclass of another
[04:58] class.
[04:58] When we talk about
[05:00] inheritance.
[05:00] In the coming sections, I'm going to show you the demo of the protected variables and protected methods
[05:06] and how to access them.
[05:07] But I'm assuming with all the discussions that we have done so far, you are pretty clear on how to
[05:13] define access modifiers on top of your classes, methods and fields, and how to use them based upon
[05:19] your use case or business requirements.
[05:21] Always make sure you are using the correct access modifier.
[05:26] Don't try to unnecessarily expose your methods and variables by using public access modifier.
[05:32] That is not a recommended approach or a standard.
[05:35] When you start working in a real project, first try to understand how the senior developers are tech
[05:40] leads inside your project
[05:42] they are using these access modifiers on the very similar lines
[05:46] you should also follow the same standards that are being followed inside your Java project.
[05:51] With the help of this course, I can only teach you the concept and the syntax on how to define these
[05:57] access modifiers.
[05:58] Since I can't teach each and every scenario inside your real projects, I strongly recommend you first
[06:04] observe the code written by the senior developers or tech leads, and if needed, you can ask their
[06:10] inputs while you are trying to build your business logic with the help of access modifiers.
[06:15] I hope you are convinced with my inputs.
[06:17] Now let me delete this Main class inside the model package and I'm going to keep these access modifiers
[06:24] demo class for your reference inside the GitHub repo, please refer to this class whenever you have
[06:29] some questions around the access modifiers.
[06:32] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

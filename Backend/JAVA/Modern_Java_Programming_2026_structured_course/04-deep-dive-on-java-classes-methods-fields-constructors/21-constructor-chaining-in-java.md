# 4.21 — Constructor chaining in Java

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's try to discuss the concept of constructor chaining.
[00:05] So what is a constructor chaining.
[00:07] It is a technique that is used inside the object oriented programming to invoke one constructor from
[00:14] another constructor, which is present in the same class.
[00:17] Like, you know, inside the same Java class
[00:20] we can write any number of constructors which accept different types of input parameters.
[00:26] We call that concept as constructor overloading.
[00:28] So when we have multiple constructors defined inside a Java class, it is perfectly possible to invoke
[00:35] one constructor from another constructor.
[00:37] So this concept or this technique, we call it as constructor chaining.
[00:42] For example, if you take the same Employee Java class that we have as of now, we have two constructors
[00:47] inside this Java class, one constructor, which is similar to default constructor.
[00:52] It is not going to accept any input parameters, whereas the other constructor that we have, it is
[00:58] going to accept for input parameters like firstName, lastName, age and gender.
[01:03] So here we have two constructors, and I want to invoke the parameter constructor from my default constructor,
[01:10] or from the constructor where I'm not accepting any parameters. I want to give a chance for you
[01:15] think about it for a second and imagine what should be the solution for this.
[01:20] What is the syntax that we need to follow when we want to invoke a constructor from another constructor?
[01:26] As a new Java developer or a naive developer, you might be thinking like to invoke
[01:32] like you can see here from the first constructor, we are going to invoke the second constructor
[01:37] and in the same process we are going to provide the values like John, Doe, 30, and M.
[01:42] But this is not going to work and you are going to get a compilation error.
[01:47] Do you want to see this in demo?
[01:48] So here inside my Employee class I have an constructor which is not going to accept any input parameters.
[01:55] So let me delete all this code so that as of now you can see my Employee constructor does not have any
[02:01] code other than this println() statement.
[02:03] Whereas the second constructor that we have this is going to accept four input parameters.
[02:09] Now like we discussed, let's try to invoke these second constructor from the first constructor that
[02:15] we have here.
[02:16] So just after the curly braces I'm going to mention Employee
[02:20] and to this Employee I'm going to pass multiple values the same we have done inside the EmployeeMain.
[02:27] So let me copy these values and mention the same here inside these employee constructor invocation.
[02:34] So do you think it is working.
[02:35] You can see here it is not working.
[02:38] We are getting an compilation error.
[02:40] The correct approach to invoke and constructor from another constructor is with the help of this keyword.
[02:46] You can see here
[02:47] first, I'm mentioning that this keyword and post that I'm passing for input parameters like John, Doe
[02:54] 30 and M. Based upon the number of input parameters that I'm trying to populate, but that this keyword,
[03:00] the corresponding constructor will be invoked inside your Java class.
[03:04] So whatever I have mentioned here, like John, Doe, 30 and M, these are matching with the parameters
[03:11] of the second constructor that we have which is Employee.
[03:14] So this will tell to my Java to invoke the second constructor from the first constructor.
[03:20] So this is the approach that we should always follow.
[03:23] Always, always please use that this keyword whenever you want to invoke another constructor which is
[03:29] present inside that same Java class.
[03:31] Let's see this in the demo as well.
[03:33] So here what I'm going to do is instead of this Employee I'm going to simply mention this keyword.
[03:39] So with that you can see the compilation error is resolved.
[03:43] So now what happens.
[03:44] So whenever someone is trying to invoke this Employee default constructor, this default constructor
[03:50] is going to invoke the another constructor that we have here.
[03:54] I can also show you this in the demo as well.
[03:56] Let me copy this System.out.println() and mention inside another constructor.
[04:02] I can change the sentence here like object is getting created in default constructor.
[04:09] After mentioning this default constructor, I can try to copy the same here into the another constructor
[04:16] as well, but I will change the sentence to Object is getting created in overloaded constructor.
[04:24] I'm also going to keep a breakpoint here.
[04:26] As a next step, I'll go to the EmployeeMain and here I'm going to create a new Employee object
[04:33] for the same
[04:33] let me mention Employee and the variable name is going to be employee3.
[04:38] And here I'm going to invoke the default constructor without passing any input values.
[04:44] So with this whenever I'm trying to invoke this default constructor here with the help of this keyword,
[04:49] we are trying to invoke the other constructor.
[04:51] Maybe what we can do here is instead of John, Doe, which is similar to employee1, we can give it
[04:57] different values inside that default
[05:00] constructor.
[05:00] I can mention something like Will and the last name as smith and the age as 55 and gender
[05:08] I'll keep it as M only.
[05:09] So let me save this now.
[05:11] I'll try to execute my class in a debug mode as soon as I start the program
[05:16] you can see the first breakpoint stopped inside the overloaded constructor with the values like John,
[05:23] Doe, because inside the EmployeeMain, the very first object that we are trying to create is John, Doe
[05:28] with the help of this overloaded constructor.
[05:31] So if I try to release next time, it is going to stop with the details of Max Steve.
[05:36] So from where this invocation is happening from the EmployeeMain class.
[05:40] Now if I try to release this breakpoint this time you will be able to see this overloaded constructor
[05:47] is getting invoked from the default constructor.
[05:49] So let me release this breakpoint.
[05:51] This overloaded constructor is getting invoked from the default constructor.
[05:56] That's what you can see here.
[05:58] As soon as I try to release the breakpoint which is present inside the overloaded constructor, it is
[06:04] going to stop inside my default constructor, because first we are trying to invoke this overloaded
[06:10] constructor.
[06:11] Later on we are trying to pass the execution at this point, which is System.out.println() where
[06:17] it is going to print this statement.
[06:19] Now if I try to release this breakpoint, it will stop inside my EmployeeMain.java program.
[06:25] Let me release this breakpoint as well.
[06:27] Let me go to the Java console.
[06:29] And here you can see first two objects are created with the help of overloaded constructor.
[06:35] Whereas the third object is created with the help of two constructors
[06:40] one is overloaded constructor and the second one is default constructor.
[06:44] So why do we have the output from the overloaded constructor as a very first statement here?
[06:49] Because if you go inside the Employee.java inside the default constructor, the very first statement
[06:55] that we have here is, to invoke the overloaded constructor.
[06:58] That's that's why we are going to have this statement printed first.
[07:02] After that, whatever statement we have inside the default constructor will be invoked.
[07:07] I hope with this it is clear for you how to invoke other constructors from a given constructor inside
[07:13] the same Java class.
[07:14] As a next step, let me tell you the other rules that we need to follow whenever we are trying to perform
[07:20] constructor chaining inside our program, the set of rules that we need to follow is,
[07:24] the call to another constructor must be the very first statement inside your constructor.
[07:30] If you try to invoke the other constructor as a second statement or a third statement, then it is not
[07:36] going to work.
[07:37] You are going to get a compilation error.
[07:39] And the second rule is a constructor cannot call itself.
[07:43] And the third rule is the same constructor cannot be called more than once.
[07:48] So if you try to do the same, you're going to get the compilation errors like you can see here
[07:52] I have some screenshots.
[07:54] The very first Java statement that I have here is System.out.println() and post that I'm trying
[08:00] to invoke.
[08:00] The other constructor, but this is not allowed.
[08:03] The thumb rule that we need to follow is always
[08:06] the constructor invocation should be the very first statement inside your constructor.
[08:11] Now if you see the last screenshot that I have here, so this constructor, which is the default constructor
[08:17] it is trying to call itself with the help of these and without any input parameter.
[08:22] And this is also not possible because like we discussed, a constructor cannot call itself.
[08:28] Let's validate these rules inside our Java program as well.
[08:31] So here as of now you can see we have this statement as a very first statement where I'm trying to invoke
[08:37] overloaded constructor from my default constructor.
[08:41] If I try to move the position of my Java statements, like if I try to put the System.out.println()
[08:47] as a very first statement, you can see I'm getting a compilation error saying that call to this must
[08:53] be the first statement inside your constructor body.
[08:57] So that's why always follow this rule.
[08:59] Let me roll back the code changes so that this compilation error will be resolved.
[09:04] The other rule that we discussed is we cannot invoke the constructor more than once.
[09:09] For example, if I try to copy the same code one more time, you can see I'm getting the compilation
[09:15] error.
[09:16] .
[09:16] So this also confirms you cannot invoke the same constructor multiple times.
[09:20] Let me delete these error line of code.
[09:23] The last check that I want to show you here is, a constructor cannot call itself.
[09:28] For example, I can remove this code and I can mention simply this with empty parentheses.
[09:34] And you can see I'm getting a compilation error saying that recursive constructor invocation.
[09:40] So this is not allowed.
[09:41] A constructor is trying to invoke itself.
[09:44] Since this is not valid and getting a compilation error.
[09:48] I hope you are clear.
[09:49] Let me remove this and roll back to the previous this statement.
[09:53] And with this our constructor chaining should work without any issues.
[09:57] I hope you are clear with the concept of constructor
[10:00] chaining as we make progress with the advanced concepts inside the Java.
[10:04] This constructor chaining is going to be very important, just like how we are invoking the constructors
[10:09] from another constructor.
[10:11] Very similarly, we can also invoke methods from another methods.
[10:15] We're also going to discuss about method invocations as well in the coming lectures.
[10:21] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

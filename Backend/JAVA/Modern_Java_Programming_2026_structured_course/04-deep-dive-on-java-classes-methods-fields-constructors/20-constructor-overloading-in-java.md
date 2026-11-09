# 4.20 — Constructor Overloading in Java

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now, we are facing a problem with the constructor, which is similar to the default constructor.
[00:06] So this constructor that we have written previously, it is not accepting any input parameters.
[00:11] And it is also always hardcoding the values like John, Doe 30 and M for all kind of objects that we
[00:19] are going to create.
[00:20] So to overcome this problem, I'm going to create one more constructor which is going to accept all
[00:27] these firstName, lastName, age and gender as an input parameters.
[00:32] We discussed previously on a high level.
[00:34] We call this concept as constructor overloading.
[00:37] We can create any number of constructors inside a Java class, as long as they are accepting different,
[00:43] different parameters as an input, the compiler is going to accept without any issues.
[00:48] Let me create the constructor here.
[00:51] To create the constructor, first we are going to mention the public keyword, very similar to the modifier
[00:56] that we have defined for the class here.
[00:58] After that, I need to mention the name as same as my Java class name.
[01:04] So what is our Java class name?
[01:06] It is Employee followed by
[01:08] I'm going to mention the parentheses and curly braces.
[01:11] So this is a default constructor. Since I have the same kind of constructor here, I'm getting a compilation
[01:17] error.
[01:18] Now to resolve this issue, I can add few input parameters to my new constructor.
[01:23] So the first parameter that I want to accept as an input for my constructor is, firstName.
[01:29] So what is the data type of the firstName String?
[01:31] That's why we need to mention String space,
[01:34] what is the variable name?
[01:35] I want to maintain the variable name as firstName itself, followed by String lastName, which is
[01:41] the second input parameter that I want to accept after the last name
[01:45] I want to mention byte and the variable name as age followed by comma char and the variable name as gender.
[01:53] It is always a good practice to maintain the input parameter names, same as your field names inside
[01:59] your class.
[02:00] This will improve the readability of your code.
[02:03] Now with this, when we try to create an object of Employee, instead of calling this default constructor,
[02:09] we can call this constructor which is accepting four input parameters.
[02:13] Let me show you that how to invoke these new constructor that we have written. For the same,
[02:18] I'm going to the Employee main
[02:20] first, I'll try to comment this code for your reference.
[02:23] After that I'm going to write the logic which is Employee and the variable name
[02:30] I'll keep it as employee1 is equal to new, after the new operator, our new keyword, I'm going to
[02:37] type the Employee and after you type the Employee this time you have an option to pass the four parameters
[02:45] as an input. For the same,
[02:47] I'm going to pass the values here.
[02:49] The first value that I want to pass is John
[02:52] and the second value that I want to pass is Doe.
[02:55] And the third value that I want to pass is age of the employee.
[02:59] So I'll keep it as 30.
[03:01] And the fourth parameter that I want to pass is gender of the employee, which is M.
[03:06] With this we are invoking the Employee constructor which is accepting four parameters like you can see
[03:14] here.
[03:14] These are the four parameters it is accepting.
[03:17] But we are getting an compilation error.
[03:19] Let me see
[03:20] what is this error.
[03:21] It is telling me 30 is an integer, but my constructor is going to accept the byte data type.
[03:27] Since I'm trying to downgrade my into to bytes, I need to do the casting.
[03:32] So to perform the casting, I'm going to mention byte just before my int value.
[03:37] With this, the compilation error is resolved.
[03:40] You may ask a question here, then why we have not received this casting error when we try to directly
[03:46] assign a value here.
[03:47] This is because my compiler, based upon my initialized value, it can understand 30 falls in the range
[03:54] of byte.
[03:55] That's why it is not going to throw an any error.
[03:58] Whereas whatever code we have written here, this is an expression that is going to be executed at runtime.
[04:06] Since my compiler does not know what value that I'm going to pass at runtime, it is throwing an error.
[04:12] That's why I have to do the manual casting or explicit casting. Very similarly
[04:17] let me create one more object with the name employee2.
[04:21] For these employee2 object, I'll give the name as Max and the last name as Steve, and the age as
[04:31] and I'll change the gender to F.
[04:33] This way we are trying to create two objects with the help of new parameter constructor that we have
[04:38] created here.
[04:39] Now at runtime, whatever values that we are trying to pass here, the same will be binded to these
[04:44] parameters that we have defined here.
[04:47] As a next step, I need to accept them and assign to the fields available inside the object.
[04:53] For the same
[04:54] we are going to copy these code.
[04:56] So let me paste the same here, but here instead of hard coding
[05:00] the value.
[05:00] I'm going to simply the variable name that we have mentioned in the parameters.
[05:05] So let me mention the firstaName.
[05:07] Now I'll copy this lastName field and mention here by deleting the doe value.
[05:13] Let me mention the same under age.
[05:15] Let me do the same for gender as well.
[05:18] So with this, what we are trying to do here is we are accepting the values from the people who are
[05:25] is trying to create the object.
[05:27] So those values are available inside these variables like firstName, lastName, age and gender.
[05:33] The same values I want to assign to the current object that right now I'm trying to create.
[05:38] So how to refer to the current object with the help of ' this '.
[05:42] So when you try to use these you're going to refer to the current object.
[05:46] After these we are going to mention these firstName, lastName age and gender.
[05:51] And for these variables we are going to assign the values that we are going to receive inside these
[05:56] variables that we have defined as an input parameters.
[06:00] It is always advisable to use the same variable names,
[06:03] you can see the field names are always matching with the constructor input parameter names.
[06:08] It is a standard that we need to follow if needed
[06:11] you can change this to some to different value, but we need to make sure you are mentioning the same
[06:17] here.
[06:18] This
[06:18] the mapping between your constructor parameters and your object fields is going to work, but please
[06:24] avoid these as it is not a standard.
[06:27] Let me revert back now with this we should be good.
[06:30] Let me save this and go to the Employee main() and start my program in a debug mode.
[06:36] The breakpoint that we have put inside the constructor is not stopped, because right now we are not
[06:41] invoking this constructor.
[06:42] We are invoking a constructor which has parameters.
[06:46] That's why the execution not stopped at the line 13.
[06:49] It stopped directly at the line 16 inside the EmployeeMain.
[06:53] The important information that I want you to observe here is if you can go to these employee1 and
[06:59] employee2 objects, you will be able to see the values that you passed to your constructor during
[07:05] the object creation.
[07:06] So the firstName, lastName
[07:08] and very similarly for the employee2 the first name is going to be Max and the last name is going
[07:13] to be Steve
[07:14] and the age and genders
[07:15] also, we have respect to fields that we have mentioned inside the object creation code.
[07:21] So let me release this breakpoint so that we can see the complete output.
[07:25] So we are getting 30 M and 25 F.
[07:28] We are not getting these output which is object is getting created because this constructor is never
[07:34] invoked.
[07:35] I hope this is clear. For your reference
[07:37] I also mentioned the details about what is constructor overloading with the code screenshots.
[07:43] Please always refer them for any questions.
[07:45] I also mentioned the details about the purpose of this keyword, and I also mentioned a note,
[07:50] whenever we are trying to define our own custom constructor inside a Java class, the Java or the JVM
[07:57] will not generate a default constructor automatically in such cases, if you still need a default constructor,
[08:04] the developer must explicitly create it inside the Java class.
[08:09] I hope you are enjoying the course.
[08:11] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

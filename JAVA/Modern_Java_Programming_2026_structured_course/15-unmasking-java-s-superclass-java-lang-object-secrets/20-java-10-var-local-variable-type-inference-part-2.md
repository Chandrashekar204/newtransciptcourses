# 15.20 — [JAVA 10] var (local variable type inference) - Part 2

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Let's try to understand how VAR is going to work in the scenario of inheritance.
[00:05] Think like inside an inheritance scenario
[00:07] you have two subclasses Student and Artist.
[00:10] They both are extending a superclass with the name Person.
[00:14] With this inheritance setup, if you try to write the code, which is where's is equal to new Student,
[00:20] do you think that's is going to be inferred as a Student or a Person?
[00:25] The answer is very simple.
[00:27] VAR is always going to infer the s variable based upon the type of the object that you are trying to
[00:33] create on the right hand side.
[00:35] So on the right hand side, since we are trying to create the object of Student, the s is going to
[00:41] be inferred as a Student data type, but not the Person superclass.
[00:46] The same applies for Artist as well.
[00:49] Like if you try to write var s is equal to new Artist.
[00:52] In such scenario, the s is going to be interpreted or inferred as Artist data type.
[00:58] But like I said before, once the initialization is completed, you can't assign a different object
[01:05] to the same variable that you have created with the help of var.
[01:08] So here I'm trying to assign a new object to the same s variable by writing new Artist.
[01:16] So this is going to result into the compilation error, because my s is already interpreted as Student
[01:23] based upon the code that we have here.
[01:25] But later on, if I try to change that data type to the Artist, the compiler is not going to accept
[01:31] in Java. This is how var is going to work in the scenario of inheritance, always note that the var
[01:37] is going to interpret the variable as the object that you're trying to create
[01:42] on the right hand side.
[01:43] You might be super happy with the VAR, and you may be thinking to use in a lot many places, but I
[01:49] want to stop your thought there where we can only use while we are trying to create the local variables
[01:55] so there are good amount of restrictions or limitations that you need to be aware whenever you are trying
[02:02] to use the VAR.
[02:03] So let's try to understand what are those?
[02:05] The very first restriction is we can't use the var as part of the method arguments.
[02:11] Here you can see I'm trying to create the method with the name Sam, and to this method I'm trying to
[02:16] pass two input variables like var a and var b.
[02:20] This will result into a compilation error because var is not allowed to use with the method arguments.
[02:27] The same applies for return type of the method.
[02:30] So whenever you're trying to define a method, we are not allowed to mention the var as the return type
[02:37] inside the method, we are going to get a compilation error, and the next limitation that we have is
[02:42] we can't assign a null value to the variable that we are trying to create with the help of var.
[02:48] It is also going to result into a compilation error, and the next important limitation is we can't
[02:54] use the VAR while we are trying to create the class level fields like instance fields or static fields.
[03:02] The reason is we can only use the var while we are trying to create the local variables.
[03:07] So what are local variables?
[03:09] The variables that we are trying to create inside a method, or inside a loop, or inside a if block.
[03:15] All such variables, we can call them as local variables.
[03:18] And the last limitation you already know we can't use a var to create the variables without any initialization
[03:25] or without any assignment value.
[03:27] So these are the limitations that you need to be aware whenever you are trying to use a var feature
[03:33] inside your Java program.
[03:35] I hope you understand the purpose of var.
[03:37] Thank you and I'll catch you in the next lecture, bye.


########################################

# 7.6 — Assignment Operator in Java - Part 2

> Section 7: Operators in Java

[00:00] Based upon our previous discussion about the assignment
[00:03] operator, it should be pretty clear for you right now.
[00:06] Always hour is equal to operator is going to expect two operands.
[00:12] On the right hand side
[00:13] you need to mention one operand, and on the left hand side you need to mention other operand.
[00:18] So whatever operand that you are mentioning always on the left hand side it should be a variable name
[00:24] always.
[00:24] For example you can't assign 98 is equal to 98 like this because it is not going to be a valid compilation
[00:32] statement.
[00:32] That's why always make sure on the left hand side you have a variable name on the right hand side,
[00:38] it is up to you whether you want to hardcode a literal value, or whether you want to mention other
[00:44] variable name on the right hand side.
[00:46] Let's see a demo about how to mention a variable name on the right hand side.
[00:51] For the same, I'm going to create a double variable which is dNum1.
[00:57] So d, indicates double num indicates number.
[01:00] So this short name I'm trying to use to represent double number one was that I'm trying to assign a
[01:06] value which is 3.14.
[01:08] After that I'm going to copy the same line of code into the next line.
[01:12] And here I'm going to change the variable name to dNum2 and to this variable
[01:17] this time I'm going to assign a double value which is 4.48.
[01:23] Now what I can do is I can try to write an expression which is dNum1 = dNum2.
[01:31] So you can see this is a completely valid statement on the right hand side
[01:36] this time I'm trying to provide a variable name instead of a literal value.
[01:41] With this
[01:42] whatever value that we have right now storing inside the dNum2, the same is going to be assigned
[01:48] to the dNum as well.
[01:50] We can confirm the same with the help of System.out.println()
[01:54] and to this I'm going to pass dNum1.
[01:57] So if I try to execute this program at the end you're going to get the output 4.48.
[02:03] This indicates that whatever value that we stored inside the dNum2 is successfully assigned to the
[02:10] operand, which is available on the left hand side.
[02:13] So what is the operand here
[02:14] it is dNum1.
[02:16] Now let's try to complicate this further more.
[02:19] This time what I'm going to do is, I'm going to assign a different value to the dNum2.
[02:25] The value is 6.58.
[02:28] So do you think whatever I stored here is going to be reflected inside dNum1 as well?
[02:34] Let's see how that is going to work.
[02:36] So what I'm going to do here is I'm going to print the value of dNum1 again by taking the variable
[02:43] name.
[02:44] So let's see what is output we are going to get.
[02:46] If I try to execute this program you can see two times I'm getting the same value which is 4.48.
[02:52] That means when we change something inside a variable dNum2, it is not affecting the dNum1
[02:58] because this line is already executed right now my dNum1 one is holding the value which is 4.48 at this
[03:06] point of time.
[03:07] Later on, when I change the value inside the dNum2, it is not going to affect dNum1.
[03:13] This is because both the dNum1 and dNum2 are variables of type primitive data type.
[03:19] Inside primitive data type, always the actual values will be stored inside the variables.
[03:26] That's why any change that we are doing on dNum2 is not getting reflected in dNum1 because the
[03:33] statement is already executed and right now dNum1 and num2 they are holding two different values.
[03:39] Later on
[03:39] if I execute this line of code, only the value inside dNum2 is going to be overridden, but you
[03:46] will not be able to see the same behavior if you try to use the assignment operator on top of reference
[03:53] data types.
[03:54] So as of now these dNum1 and dnum2.
[03:57] They are simple variables which are representing a primitive data type of type
[04:03] double.
[04:04] But if you try to use the same assignment operator between two object references are two reference data
[04:10] types, then like I said, the behavior is going to change.
[04:13] So let me show you that behavior by taking an example.
[04:16] So to create an object of a class first I need to create a class.
[04:21] So the class that I'm going to create here is person.
[04:24] So let me create a person class.
[04:26] Once the class is created inside this class I'm going to create a field name of type String and post
[04:33] that
[04:34] I'm going to create an constructor for this class, which is going to accept the name as an input parameter.
[04:41] And inside this constructor I'm simply going to execute the code which is
[04:46] this.name = name.
[04:48] So whenever someone is trying to create an object of this class, they're going to invoke this constructor
[04:53] with a name value and the same name value I want to assign to the current object
[04:58] name field.
[04:59] That's why I have used this
[05:01] this.name.
[05:02] I hope you are clear.
[05:03] Now let me go to the AssignmentOperatorDemo.
[05:06] And here I'm going to create two Person object.
[05:09] So the very first person is going to have an object reference which is person1
[05:15] and after this object reference I'm going to invoke the constructor of the Person.
[05:20] And to this constructor I'm going to pass a name which is Madan.
[05:23] And similarly I'm going to create one more person with the object reference or variable name as person2,
[05:30] this time for the person2, I'm going to assign the name, which is Saanvi.
[05:35] So right now you can see we have two different objects person1 and person2, with two different
[05:40] names.
[05:40] Very similar to this line of statements.
[05:43] I'm going to use assignment operator between two object references or between two reference data types.
[05:50] For the same
[05:51] I'm going to simply write a Java expression which is person1 is = person2.
[05:57] So with these both these person1 and person2, they are going to point to the same memory location
[06:04] where we are storing these person2 object.
[06:06] That's why if I try to print out the name of the person1 with the help of person.name will
[06:15] be able to see the name which is Saanvi.
[06:17] So let me try to execute this program and you can see we are getting a name Saanvi.
[06:21] But let's try to make some changes on person2 object and see whether the same is getting reflected
[06:27] on person1 or not.
[06:29] So for the same, I'm going to invoke the name variable with the help of person2.name and to
[06:36] this name field.
[06:37] This time I'm going to assign the Saanvi name in complete capital letters. Based upon our previous discussion
[06:44] when we make some changes on dNum2 the same is not reflected to that dNumb1, because those are
[06:50] primitive data types.
[06:52] But when we try to do the same for object reference data types, whatever changes that you have done
[06:58] on the person2 is going to reflect on the person1 as well, because both these objects are pointing
[07:05] to the same memory location where the person2 object is stored.
[07:10] So I can confirm the same by executing the same System.out.print() statement one more time.
[07:16] So if I execute this program one more time, you will be able to see the Saanvi in complete capital letters.
[07:23] So we made the change inside the person2.
[07:25] But the same is getting reflected in the person1 object.
[07:28] How this is possible.
[07:30] This is because when we use assignment operator between two objects, they both are going to point to
[07:36] the same memory location.
[07:38] I can also prove you this one more time by making some changes inside the person1.
[07:42] So if I make some changes inside person1, the same is going to be reflected in person2 as well.
[07:48] For the same, I'm going to copy this line of code and mention again here and post that
[07:54] I'm going to rename this variable person2 to person1.
[07:58] And this time I'll give some random name, which is John.
[08:01] So with this now we are setting the name John into the person1 object.
[08:07] But if you try to print the name from person2, you are going to get the same value, which is John.
[08:13] So let me try to execute this program this time, and you will be able to see the name John from the
[08:19] person2 object.
[08:20] So this confirms any change that you are trying to do on any of the object is getting reflected on the
[08:27] other object as well.
[08:29] So that's why please be very careful whenever you are trying to use this assignment
[08:33] operator
[08:34] on top of object references, you're not going to have the same effect if you try to use assignment
[08:40] operator on top of primitive data type variables.
[08:43] I hope this is clear for your reference
[08:45] I have mentioned all the details that we have discussed just now inside this slide.
[08:49] So in future whenever you are reading these slide, please recall all the discussions that we have done
[08:55] around the Person objects.
[08:57] Now before I try to close this lecture, let me try to clarify about three important jargons that you
[09:03] may hear whenever you are trying to use the assignment operator.
[09:07] These jargons are declaration, initialization and assignment.
[09:12] Declaration is very simple,
[09:14] whenever you're simply trying to declare an variable, we can call that as an declaration.
[09:19] Here I have declared a variable age with the primitive data type as an int.
[09:24] So here I'm just declaring the variable.
[09:27] But I have not assigned or initialized any value.
[09:30] So these kind of process of introducing a variable to the Java compiler, we can call it as declaration.
[09:37] Whereas initialization is a process of assigning a value to a variable at the time of declaration itself.
[09:44] So if I write a Java statement which is int age = 25, this is going to be considered as both
[09:51] declaration and initialization.
[09:53] Then what is an assignment?
[09:55] Assignment is a process of assigning a value
[09:58] to a available after it has been declared.
[10:01] If you see here first I'm trying to assign a variable which is int age.
[10:06] With that, I have done only the declaration.
[10:08] In the next Java statement.
[10:10] I'm trying to assign a value with the help of assignment operator.
[10:14] So these kind of behavior or process
[10:18] we call it as assignment.
[10:20] I hope you are clear with these jargons.
[10:22] If needed, we can also declare multiple variables in a single statement by separating them with the
[10:29] help of comma.
[10:30] Previously I showed you how to declare multiple numb's like num1, num2, num3 inside the Java code.
[10:37] So very similarly, if you want to declare multiple variables of int with the name x, y, z, you can
[10:44] simply declare them by writing a Java statement which is int x, y ,z.
[10:49] So here we are only doing the declaration of three variables.
[10:52] Whereas if you try to see the other flavors that I have here, you can see in this statement I'm trying
[10:59] to do the initialization for x and z, whereas for the y I have done only the declaration.
[11:06] And in the next statement I'm doing both declaration and initialization for all the variables like x,
[11:11] y, z.
[11:12] So this way based upon your requirements, you can simply declare or you can do both declaration and
[11:18] initialization as well with the help of assignment operator.
[11:23] But one thing that we need to take care as a developer is, your assignment operator
[11:28] it is always going to do a check whether you are assigning a literal value of the same data type that
[11:35] you have declared on the left hand side.
[11:37] If this compatibility is not met, your assignment operator is going to throw an compile time error.
[11:43] So here you can see I have declared int x = 56.
[11:47] So instead of int value, if I try to assign a float value or double value or a string value, my assignment
[11:54] operator is not going to accept it, and it is going to simply throw an compilation error.
[12:00] With this, we discussed everything about the assignment operator, so it looks very simple.
[12:05] It has some special scenarios which we also discussed.
[12:08] I hope you are clear about all the special scenarios.
[12:11] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

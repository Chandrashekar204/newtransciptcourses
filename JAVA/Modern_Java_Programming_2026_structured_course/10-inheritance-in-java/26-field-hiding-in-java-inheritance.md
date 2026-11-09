# 10.26 — Field hiding in Java Inheritance

> Section 10: Inheritance in Java

[00:00] As of now, we're talking a lot about method overriding, method overloading, and method hiding.
[00:06] But let's try to understand what is going to happen to the instance fields and static fields as part
[00:13] of the inheritance process for the same inside my parent class, which is Vehicle, I'm going to create
[00:19] few instance fields just to save some time
[00:22] I'm trying to paste a few lines of code here.
[00:25] You can see here I have created three different instance variables with the public access modifier.
[00:32] Ideally, inside real applications we're not going to use the public access modifier.
[00:37] We are going to use the private access modifier.
[00:39] And we are going to expose our instance variables with the help of getter and setter methods.
[00:45] But to make our discussion easy, for now, I'm just giving the public access modifier for all the fields
[00:51] that I have created just now.
[00:53] So the first field name is horsepower, followed by color and turning radius.
[00:57] Now I'll go to the Car subclass, and here I'll try to look for the list of methods and variables available
[01:06] for my subclass.
[01:07] You can see here
[01:08] my subclass is inheriting all the instance variables that I have declared public like color, horsepower,
[01:17] and turningRadius.
[01:19] All of them
[01:19] they are getting inherited from the Vehicle superclass.
[01:22] And here you may have a question
[01:24] how about these engine variable name.
[01:26] So this is not going to be inherited because it has a default access modifier.
[01:32] And since this Vehicle and the Car they are present inside different packages, the engine related variable
[01:40] is not going to be inherited by my subclass.
[01:43] I hope that makes sense.
[01:44] Now we got a confirmation that that the instance fields are also going to be inherited by the subclass.
[01:51] The same is going to be applicable for the static fields as well.
[01:55] If you want, you can also create a static field and confirm the same.
[01:58] But now let's try to understand what is going to happen if I try to define the same variables are same
[02:07] instance fields are static fields inside my subclass.
[02:11] So let's try to understand the same for the same.
[02:13] This time I'm going to copy few lines of code inside my Car subclass.
[02:19] Here you can see in total I'm trying to create four different variables like horsepower, color, turningRadius
[02:26] radius, and automatic.
[02:28] Now, if I try to look for the list of methods and variables inside my class, you can see right now
[02:34] I have all the fields from superclass and the subclass also.
[02:39] My superclass has a color value white, whereas my subclass has the color value black.
[02:46] The same for horsepower
[02:47] you can see the superclass has 120, whereas subclass has 150.
[02:52] Coming to the turningRadius, the superclass has 5.23, whereas subclass has 6.23.
[02:59] And this variable, which is isAutomatic.
[03:01] This is a new field that I'm trying to create inside my subclass.
[03:06] There is no field inside the superclass with the same name.
[03:10] With that we can say this is automatic is a field specific to my subclass alone.
[03:15] So the question right now you may have is I'm able to see all the fields both from superclass and subclass,
[03:22] then how this is going to work in real time.
[03:25] If I'm trying to invoke one of the field using an object reference, whether my compiler is going to
[03:31] invoke the field present inside my subclass or in the superclass, you may have such questions.
[03:36] The answer to your question is very simple, just like how we saw inside the method hiding even in these
[03:43] scenario also,
[03:43] your compiler or Java always is going to look at what is the object reference data type.
[03:52] Using the same, it is going to invoke the fields present inside that class data type.
[03:57] It is not going to worry about which object we have assigned to the object reference.
[04:03] I'll show you a demo in a few minutes, but before that I want you to highlight that whatever we have
[04:08] done right now, like defining the same fields inside the subclass, like in superclass.
[04:14] This concept is also called as field hiding.
[04:17] We can't say it as a field overriding.
[04:20] And one more important point that you need to be aware
[04:23] whenever we are performing field hiding is as long as the variable name is same, we can still consider
[04:30] it as a field hiding.
[04:32] Regardless of what data type you are trying to use, or what data value or what access modifier you
[04:38] are trying to use.
[04:39] Still, if the variable name is same, it is going to be considered as a field hiding.
[04:44] For example, here for the turningRadius inside my Vehicle superclass, I have defined that data type
[04:50] as double, whereas in the Car subclass I have defined the turningRadius data type as String.
[04:57] Still, this turningRadius is
[04:59] going to be considered as a field hiding, because we have given the same name that we are trying to
[05:06] maintain inside the superclass.
[05:08] I hope you are clear.
[05:10] Now let's see the demo on how to invoke these variables and how the invocation is going to taken care
[05:16] by your Java or compiler.
[05:19] For the same, I'm going to create a new class inside the app package.
[05:23] The class name is going to be TestFieldHiding.
[05:26] So inside this TestFieldHiding class I'm going to create a main() method.
[05:31] And inside the main() method
[05:33] first let me try to create a simple Car object by using
[05:40] Car car = new Car().
[05:42] Now using the Car object reference which is car, I'm going to print out all the fields that we have
[05:49] created.
[05:50] So let me type Car.color.
[05:53] You can see as soon as I type color I have only one option to invoke it.
[05:57] Let's see which color it is going to print when we run this program.
[06:01] Similarly, I'm going to print all other variables
[06:05] also, I'll try to invoke other variables.
[06:08] This time I will invoke horsepower followed by turningRadius followed by isAutomatic.
[06:15] So these are the four variables that I have declared inside my car.
[06:19] And we have these three of them with the same name inside the Vehicle superclass as well.
[06:24] Let's see what is output we are going to get.
[06:26] We are going to get all the values that we have defined inside the subclass.
[06:31] The reason is it is very simple.
[06:33] You are sending the car object reference which is pointing to the Car data type.
[06:40] That's why my compiler, it is going to simply consider the fields and its values defined inside the
[06:47] Car subclass.
[06:48] This time I will try to create the Upcasting.
[06:52] So here first I'll try to create an object reference of Vehicle and to the same I'm going to assign
[06:58] the Car object to that we have created at the line number nine.
[07:03] But this time I'll try to print all these fields with the help of Vehicle object reference by simply
[07:09] mentioning Vehicle.color, Vehicle.horsepower and Vehicle.turningRadius.
[07:15] And I will not be able to invoke isAutomatic with the help of Vehicle because according to the compiler,
[07:22] when I pass an object reference of Vehicle, it is simply going to look if there is any field with this
[07:28] name inside the Vehicle
[07:29] superclass. Since I don't have it, is throwing an compilation error
[07:32] that's why we need to remove this.
[07:34] Now
[07:34] if I try to execute this program, you can see we are going to get all the values from the superclass
[07:41] which is white 120 and 5.23.
[07:44] The reason is this time we are simply passing the object reference of Vehicle class data type.
[07:51] So this confirms even in the field hiding also the Java or the compiler, they are always going to look
[07:58] what is the object reference data type that we are passing.
[08:02] They're not going to worry about what is the object that we are holding inside these object reference
[08:08] the same kind of concept applicable for the static variables as well.
[08:13] As of now we are trying to explore the example with the help of instance
[08:17] fields are non static fields, but like I said the same applicable for the static fields as well as
[08:24] a next step, I want to show you the usage of super keyword to invoke the fields present inside the
[08:30] super class from the subclass.
[08:33] Think like from my subclass, which is Car
[08:36] I want to invoke one of the variable available inside the Vehicle super class.
[08:42] So how to do that?
[08:43] The clue is super keyword during the method overriding
[08:46] I already told you that from the subclass
[08:49] if you want to invoke the same overridden method present inside the super class, then in such scenarios
[08:55] you can use the super keyword
[08:57] the same rule applies here as well.
[08:59] For example, inside my Car I'm going to create a new method which is public void print Car details.
[09:08] Inside this method
[09:10] first, I'm going to write down a print out statement where I will try to display the color value because
[09:17] the color field present inside the same class.
[09:19] But now if I have a scenario, if I want to invoke the same color field present inside the super class,
[09:26] then in such scenarios I can simply try to mention super.color.
[09:33] With that, the field inside the super class is going to be invoked the same we can confirm by going
[09:38] to that test field hiding.
[09:40] And here, with the help of this Car object reference, I'm going to invoke the method which is
[09:47] printCarDetails().
[09:48] So if I try to execute this program you can see here we have black and white.
[09:53] So black is the color which we are displaying from the field of subclass whereas a white
[09:59] is a color value which we are printing using the super.color code that we have written here inside
[10:06] this printCardDetails().
[10:07] I hope you are clear.
[10:09] Everything that we discuss around the field hiding
[10:12] I have mentioned inside the slide for your reference.
[10:15] So whenever we are talking about static fields or instance fields, there is no concept of overriding
[10:21] and overloading.
[10:22] There is only a single concept called field hiding.
[10:25] And in order to perform field hiding, if you use the same field name inside your subclass, it is going
[10:31] to be considered as a field hiding.
[10:33] Regardless whether you are using the same data type or a different data type.
[10:37] As long as you use the same field name, it is going to be considered as a field hiding in Java.
[10:43] I hope you are clear.
[10:44] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

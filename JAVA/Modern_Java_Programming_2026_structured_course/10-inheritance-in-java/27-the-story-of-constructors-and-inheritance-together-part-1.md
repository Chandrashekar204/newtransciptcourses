# 10.27 — The story of constructors & Inheritance together - Part 1

> Section 10: Inheritance in Java

[00:00] There is a special story that you need to be aware about how constructor invocation is going to be impacted
[00:08] due to the inheritance.
[00:10] To show you a demo around this topic, first let me try to create a constructor inside my parent class
[00:16] and subclass.
[00:17] We know by default there will be a default constructor which is going to be created by the compiler
[00:23] or by Java.
[00:24] But to make our things more clear, I'm going to create my own constructor.
[00:28] And inside the constructor which I'm going to define, I'm going to initialize all these variables.
[00:34] As of now, I'm trying to do the initialization and declaration in a single step, but ideally inside
[00:40] real applications we are not going to do that.
[00:43] We're always going to do the initialization of the class variables with the help of constructor.
[00:48] That's why first let me try to create a constructor.
[00:51] So to create a constructor I can simply type public
[00:55] and what is the class name which is Vehicle.
[00:58] Since I want to first develop a default constructor, I'm not going to accept any input parameters to
[01:05] my constructor.
[01:06] Now, inside my Vehicle constructor I'm going to initialize all the fields like horsepower
[01:11] I will initialize to 120, and with that we no more need to initialize the horsepower field here.
[01:19] So let me remove this.
[01:20] Very similarly, I'm also going to assign a value to color which is white, followed by I'm going to
[01:28] assign a value to that turningRadius also
[01:30] the value is going to be the same which is 5.23.
[01:34] And after this turningRadius this time you can see I have created a new variable inside my Vehicle
[01:40] class which is made for and this field I'm not going to define again inside my subclass.
[01:47] So there is a story behind it.
[01:48] For now, let's try to initialize this made for as well inside the constructor by using a value which
[01:55] is road.
[01:56] So the vehicle is made for the road purpose.
[01:58] So this is the initial values that I want to assign inside my vehicle constructor.
[02:03] And with that we can remove all these initialization that we have done previously.
[02:08] So let me remove for turningRadius and made for as well.
[02:12] Apart from these initialization I also want to have an System.out.println() statement where I'm
[02:19] going to print a statement which is inside Vehicle default constructor.
[02:26] So the very similar constructor I want to define inside my Car subclass as well.
[02:33] So let me do the same here by copying the same constructor.
[02:36] But here instead of Vehicle, we need to mention Car and post that
[02:40] I'll update this System.out.println() to inside Car default constructor and the horsepower
[02:46] I will change to 150, followed by black, followed by,
[02:51] for the turningRadius, we need to assign the value in a String format.
[02:55] The value is going to be 6.23 and the madeFor
[03:00] I'm not going to define or hide again inside my subclass.
[03:04] I'm fine with whatever default value that I am going to inherit from the superclass.
[03:08] So now let me take these isAutomatic, which is specific to my subclass, and assign a value which
[03:14] is true.
[03:15] After this we can remove all these initialized values.
[03:19] So let me do the same for remaining fields as well.
[03:23] So once we are done you can see as of now we have our constructors ready in both of the classes.
[03:30] Now I'll show you the magic here.
[03:32] To show you the magic, I'm going to create a new class Inside App Package.
[03:37] The class name is going to be ConstructorDemo.
[03:41] So inside this ConstructorDemo class I'm going to create a main() method.
[03:46] And here I'm simply going to create the object of the Car class using the new operator and the Car default
[03:54] constructor.
[03:54] Now if I execute this statement, you can see we are getting two different statements.
[03:59] First, the statement which is present inside the superclass constructor, the same is getting printed,
[04:04] followed by the statement that we have inside the subclass constructor.
[04:08] So who is invoking our superclass constructor?
[04:11] Do you know the answer?
[04:12] It is the Java, which is taking care of invoking the parent constructor as well.
[04:18] Do you know the reason why Java is doing this?
[04:20] Because the Car is going to inherit all the properties from the superclass, which is Vehicle.
[04:26] That's why while we are trying to create the object of Car, we should also make sure the variables
[04:32] of the Vehicle are also initialized properly.
[04:36] So since the initialization needs to happen properly by default, Java always is going to invoke the
[04:43] superclass constructor before it is trying to invoke the subclass constructor.
[04:48] I can also show you one more small demo here.
[04:51] I'll try to print out the variable that we have inside the superclass with the help of Car object.
[04:57] So you can see I'm trying to print out.
[05:00] and you will see I'm getting the output as road so I know where have the madeFor related logic inside
[05:06] my Car subclass, I only initialized it inside the constructor of my Vehicle superclass, and since
[05:13] the same is getting invoked, I'm able to print the road value using the System.out.println().
[05:20] I hope you are clear.
[05:21] So how the Java is going to invoke the superclass constructor?
[05:24] Every time a constructor is being returned inside a subclass behind the scenes, it is going to add
[05:31] a super keyword followed by parentheses.
[05:34] So this is the syntax to invoke the super class default constructor.
[05:40] Since I'm not passing any input parameters to the super, my Java is always going to invoke the super
[05:46] class default constructor in this scenario, and this is always inbuilt or default to behavior by Java.
[05:53] This also should give a confidence to you that whenever you are trying to create an object of subclass,
[05:59] the subclass object is also going to store the variables of the super class along with their initialized
[06:05] values.
[06:06] Because behind the scenes, Java is taking care of invoking the default constructor of the super class
[06:13] from the constructors of the subclass.
[06:15] So this is going to work automatically as long as you have default constructors.
[06:20] But if you start defining the constructors that accepts the input parameters, then this default behavior
[06:27] may not sufficient.
[06:28] In such scenarios
[06:29] you as a developer, it is going to be your responsibility to use the super keyword and to invoke the
[06:36] parent constructor.
[06:38] I hope you are clear with this initial discussion.
[06:40] Let's try to discuss about more complex scenarios around this in the next lecture.
[06:45] Thank you,
[06:45] bye.

----------------------------------------

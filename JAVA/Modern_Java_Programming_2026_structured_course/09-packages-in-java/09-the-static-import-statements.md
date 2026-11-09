# 9.9 — The static import statements

> Section 9: packages in Java

[00:00] Inside this lecture, let me talk about a special flavor of import statement that we need to follow
[00:07] whenever we are trying to deal with the static methods or static fields.
[00:11] To show you a demo about the static import statement, first I'm going to create a class inside my utility
[00:17] package and the class name
[00:19] I'm going to keep it as MyConstants.
[00:22] Inside this class, I'm going to create a couple of static fields for the same
[00:27] I'm going to mention public static final double TAX_RATE.
[00:33] So to this TAX_RATE I'm going to assign a value which is 0.07.
[00:38] Similarly I'm going to create one more static final variable of type double with the name SHIPPING_COST.
[00:47] And to this variable I'm going to assign the value which is some random 5.95.
[00:53] So this is the SHIPPING_COST and this is the TAX_RATE.
[00:56] So these are the two static final fields that I have inside my class.
[01:01] MyConstant which is present inside the utility package.
[01:05] Think like I want to access them from my Main class.
[01:08] So here inside my Main class first I'm going to use the System.out.println() and to this println()
[01:15] method
[01:15] I'm going to pass the static fields that I have defined inside the MyConstant.
[01:20] So how to access the static fields with the help of the class name itself, like MyConstants.TAX_RATE.
[01:27] .
[01:28] And similarly I can define one more System.out.println() statement.
[01:32] And here instead of TAX_RATE I can mention SHIPPING_COST.
[01:37] So these are the two static variables I'm trying to access.
[01:40] If I try to execute this program you'll be able to see inside my console I have these values like 0.07
[01:47] and 5.95.
[01:49] So till this point everything looks good.
[01:51] You know about all the story.
[01:53] But here you can see whenever I'm trying to access these static fields, I need to mention the class
[01:59] name like MyConstants, MyConstants multiple times.
[02:03] So instead of defining MyConstants multiple times, I can simply mention an import statement which
[02:10] is import static
[02:13] so after the import I need to mention the static keyword.
[02:16] After the static keyword, I need to mention the package name of my MyConstants like which is
[02:23] com.eazybytes.utility.MyConstant.
[02:28] and after this final dot, if I press control space, I have an option to import SHIPPING_COST or
[02:36] TAX_RATE.
[02:36] So first let me try to import the shipping cost.
[02:39] But as soon as I try to import, my intelliJ is trying to do some optimizations.
[02:43] So let me go to my preferences.
[02:46] And here under the auto import I'm going to uncheck these options just for some time.
[02:54] Now this time I'm going to type the package name one more time like import static
[02:59] after the static I'm going to mention the package name which is com.eazybytes.utility.MyConstants.TAX_RATE
[03:05] followed by semicolon and post that I'm going to mention one more constant name
[03:12] which is SHIPPING_COST.
[03:14] So here I have imported the static fields itself with the help of these import static statement.
[03:21] With this
[03:22] now I don't even have to mention the class name.
[03:24] I can directly mention the TAX_RATE and SHIPPING_COST, and the effect is going to be the same.
[03:30] You can see I'm also going to get the same output, which is 0.07 and 5.95.
[03:36] The same kind of strategy we can use even for the static methods as well.
[03:42] So let me remove these unused import statements.
[03:45] Post that I'll go to the MyConstants.
[03:47] And here I'm going to create a method which is public static double.
[03:53] After the double I'm going to mention the method name as calculateTotalCost().
[03:58] And to this method I'm going to pass the output which is double price.
[04:03] So if someone provides the price of the product to this method, it is going to provide the total cost
[04:10] by adding the TAX_RATE and SHIPPING_COST.
[04:13] So here I'm going to write the return statement followed by price.
[04:17] To this price I'm going to add amount which I'm going to get based upon the calculations which is price
[04:24] asterisk TAX_RATE.
[04:25] And after the TAX_RATE I'm also going to add the SHIPPING_COST.
[04:29] So these are total amount that I want to return from my calculateTotalCost() static method.
[04:35] So now here if I want to access the static method inside my Main class there are two options.
[04:42] The very first one is I can try to access it with the help of class name like MyConstants.calculateTotalCost()
[04:51] and to this I can pass an amount which is 9.9 $9.
[04:57] So if I try to execute this program, I'll get the total
[05:00] cost, which is 16 .6393.
[05:02] But you can see we're trying to invoke the method with the help of class name.
[05:07] Instead, we can use the import static method here as well.
[05:11] This time, instead of importing the static field, I'm going to import the method itself which is calculateTotalCost.
[05:17] .
[05:18] Now I can simply remove these MyConstants class name.
[05:22] And with that you should be able to have the same behavior.
[05:26] So this is the power of static import statements.
[05:29] So the same kind of static import statements,
[05:32] you can also mention whenever you are trying to access something from the JDK library.
[05:37] For example, there is a cde Jlass insiDK library which is Math.
[05:42] Inside this Math class, which is present inside the java.lang package, we have so many static
[05:49] methods and static variables.
[05:51] For example, I have a static variable here with the name pi.
[05:55] So this pi static variable has a value of pi.
[05:59] If I want to use the same inside my Main class, I have a couple of options.
[06:04] One is with the help of Math class, I can invoke the pi constant.
[06:10] The other option that I have is just like how I have imported the static fields from the MyConstants
[06:16] Java class
[06:17] very similarly, I can also import the pi static variable from the java.lang Math class, and inside
[06:26] the Math class we have pi constant.
[06:29] Here I can simply try to pass the pi value.
[06:32] So if I try to execute this program, I'm going to get the same output.
[06:36] So this way, regardless where you are, static variables and static methods are available, you can
[06:42] always use these static import statements.
[06:45] But please use this flavor of static import statements only if you are trying to refer a static variable
[06:52] or a static method multiple times inside your business logic for 1 or 2 times, you don't have to do
[06:59] this.
[06:59] Maybe if you're trying to access more than ten times or 20 times in such scenarios, only you can use
[07:05] these static import statements.
[07:07] All the points that you have discussed so far about the static import statements I have mentioned in
[07:12] these two slides, so please refer them for any questions.
[07:16] I hope this is clear.
[07:17] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

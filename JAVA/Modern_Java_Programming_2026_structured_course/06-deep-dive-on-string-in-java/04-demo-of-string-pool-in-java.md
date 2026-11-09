# 6.4 — Demo of String Pool in Java

> Section 6: Deep dive on String in Java

[00:00] Now let's see the demo of two approaches that we have discussed in the previous lecture.
[00:05] To get started, first, I want to create a Java class inside this section6 Java project that we
[00:11] have created previously.
[00:13] For the same, I'm going to right click on the src folder and select the new Java class option.
[00:18] And the Java class name that I want to give here is StringPoolDemo.
[00:24] Once the class is created, I want to create a public static void main() method.
[00:29] So let me type the shortcut which is psvm and press enter.
[00:34] Once this method is generated, let me save this file.
[00:37] To save the file, we need to use the shortcut command S inside mac operating system.
[00:43] If I press this shortcut, you can see in the down you're able to see a message which is I have used
[00:48] the command S shortcut.
[00:50] If you want to use the same shortcut inside Windows or Linux, you need to use Ctrl + S.
[00:56] So from now onwards, anytime if I try to use a shortcut you are going to see a message in the down.
[01:02] How I'm achieving this is with the help of a plugin.
[01:06] Behind the scenes
[01:06] what I have done is I have installed a plugin.
[01:09] Let me show you the same here inside the IntelliJ Idea, I'm going to press on these preferences and
[01:15] inside the preferences
[01:16] If you can go to the plugins under the installed,
[01:19] this time you should be able to see a new plugin that I have installed, which is Presentation Assistant.
[01:25] Whenever you install this plugin inside your IDE, whatever shortcut that you are using, the same is
[01:32] going to be visible as a message at the down, and it is also going to show you the equivalent shortcut
[01:38] in other operating system as well.
[01:40] Since I'm going to use lot many shortcuts throughout the course, I don't want to spend time separately
[01:45] every time explaining you
[01:47] what is the equivalent shortcut in other operating system.
[01:49] That's why I'm trying to leverage this plugin.
[01:51] I would also recommend you to install inside your IntelliJ.
[01:55] The reason is every time you use the shortcut, it's going to show you a message in the down.
[02:00] And if you see this kind of message multiple times throughout your development career, at some point
[02:05] of time, all these shortcuts will be embedded into your subconscious memory.
[02:10] And with that, any time if anyone asks you what is the shortcut, you can answer them on the fly.
[02:15] So how to install this plugin?
[02:17] You just have to go to the marketplace option here and search for Presentation Assistant.
[02:24] As soon as you try to search for Presentation Assistant, you'll get a result inside the search results.
[02:29] So please select this presentation Assistant and with that you will have an option to install this plugin.
[02:35] As of now, since I already installed for me it is showing me the disable option, but for you it should
[02:40] show the install option
[02:42] so please click on that to enable this plugin inside your intelliJ as well.
[02:47] I hope you like this plugin and you are going to use this.
[02:49] Let me click on this okay button.
[02:51] Now we have our main() method ready.
[02:54] First I'm going to create few String objects with the help of first approach or the String literal approach
[03:00] that we have discussed.
[03:01] So let me type String and the object name is going to be hello.
[03:05] Inside this hello object I'm going to store that data hello itself.
[03:09] Next I'm going to create another variable or another object.
[03:13] The object reference name is going to be h i, hi.
[03:16] And inside this hi object I'm going to store the same data which is hello.
[03:21] And at last I'm going to create the last object with the name hey.
[03:26] And inside this hey object I'm going to store the data,
[03:30] hey.
[03:30] So now since we are using the String literal approach behind the scenes, my JVM is going to leverage
[03:36] the String pool space to optimize the String objects creation.
[03:41] With the String pool concept that we have discussed, both these first two objects should get stored
[03:46] or referenced to the same memory location. Because they both have same content.
[03:51] Let me confirm the same with the help of System.out.println() method.
[03:55] So I can use the shortcut s o u t and you can see I have a System.out.println() statement inside
[04:02] the println() method I want to compare if two objects are same.
[04:06] So whenever we want to compare two objects, we need to use the double equal to operator inside Java.
[04:13] So whenever we are using these expression behind the scenes, my Java is going to tell me whether both
[04:20] these objects are referring to the same memory location.
[04:24] So if I try to execute this program, you can expect we are going to get an output as true.
[04:29] Now I want to change this content of the second object to hello one.
[04:33] With this, the content of the second object is going to be different.
[04:37] And now we should get the output as false because they get stored at two different memory locations.
[04:44] Let me revert back to hello so that both these objects will refer to the same memory location.
[04:50] I'm also telling in the previous lecture there is also a method called hash code, using which we can
[04:55] try to understand what is the memory location where the object
[05:00] stored inside the heap memory or inside the string pool memory.
[05:04] Let me show you the demo of hash code method.
[05:06] Whenever you create an object inside Java, the object can be of any data type.
[05:12] It can be an object of String, or a person, or a customer, regardless of whatever the data type of
[05:17] the object.
[05:18] Using the object reference variable, we can invoke the hash code method to understand what is the hash
[05:25] code value of the given object.
[05:27] This hash code method is going to give some hash code value, which may look like a memory location,
[05:33] but that is not an actual memory location.
[05:36] I'll share more details about this in few seconds. Before I try to share more details
[05:40] first, let me show you the demo on how to invoke these hashcode method. To invoke the hash code method,
[05:45] like I said, we can always use the object to reference variable like hello and use the dot operator.
[05:51] And there'll be a hashcode method which you can invoke.
[05:55] And with this now I am invoking the hashCode() method, which is going to give me the hashcode value
[06:01] of my memory location where this hello object is stored.
[06:04] But I want to print this hashcode value onto the screen.
[06:07] That's why I am going to use a System.out.println() and mention this hello.hashCode().
[06:13] So let me mention the same inside println() method.
[06:16] Very similarly, I'm going to copy these statement multiple times and replace this hello with hai object
[06:23] variable reference.
[06:24] And at last I want to invoke the same hash code with the help of hey object reference.
[06:29] If I try to print out these hash code values for the first two objects, you'll be able to see they
[06:35] have the same hash code value, whereas for the third object, the hash code value is different.
[06:41] If you see these numbers, they're looking like a memory location representation.
[06:45] You may think this is the memory location where the JVM stored these objects, but please note that
[06:51] hash code never represents actual memory location.
[06:55] Java is never going to expose you where these objects actually stored inside the JVM.
[07:01] That is for the security reasons.
[07:03] Then what is this hash code value based upon the content that you are trying to store inside your object?
[07:09] This hash code value is going to be calculated.
[07:12] If I press my command button and hover on this method, I'll be able to see a hyperlink.
[07:17] If I click on that, I'll be taken to the Java library where this hashCode() method is declared.
[07:23] So you can see inside the String.java class we have a hashCode() method.
[07:27] On top of this method, there are some documentation explaining on how the hashcode value is going
[07:33] to be calculated.
[07:34] The hash code value for a String object is going to be computed with the help of this formula.
[07:39] s[0] means that is the first character, s[1]means there is a second character.
[07:44] So using this formula, the hashcode value of the String object is going to be calculated.
[07:50] If the data inside the string object is empty, we are going to get the hash code value as zero.
[07:54] This confirms whenever the content is same, the hashcode value is going to be same, but that doesn't
[08:00] mean they are stored at the same memory location.
[08:04] Then how to know whether the two objects are stored at the same memory location?
[08:08] Like I said, with the help of this double is equal to operator (==).
[08:11] We can always know whether the two objects are referring to the same memory location.
[08:16] I hope you are clear with the first approach that we have discussed.
[08:19] Now, very quickly, let me create the objects of String with the second approach that we have discussed.
[08:24] This time, I'm going to use a new operator and constructor of the String for the same
[08:29] I'm going to mention String obj,
[08:31] obj means object is equal to new String and to this string constructor
[08:36] I'm going to pass the data, which is
[08:39] hello.
[08:39] Very similarly, I'm going to create two more objects with the name obj1 and obj2.
[08:46] For the second object I'm going to pass the same data, whereas for the third object I'm going to pass
[08:52] the data, which is hey, now if I try to print the hash code value of these objects, obviously we
[08:58] are going to get the same hash code value for the obj and obj1 because they have the same content,
[09:04] which is hello.
[09:05] Let me show you that demo of the same.
[09:07] So here I'm going to first mention obj,
[09:10] next I'll mention obj1,
[09:12] next I'll copy the obj2 and mention here.
[09:15] With this
[09:16] now I'm going to get the hashcode values of these three objects that we have created with the help
[09:21] of new operator.
[09:23] You can see the hash code value is same for the first two objects.
[09:27] And in fact these hashcode values are matching with the hash code values of the first two objects that
[09:32] we have created with the help of String literal approach.
[09:36] But like I said before, whenever the hashcode value is same, that doesn't mean the objects are referring
[09:40] to the same memory location.
[09:43] We can use this hashcode value to perform the initial check.
[09:46] When the hash code values are different, we can confimly say that they are two different objects,
[09:52] but if the hash code values are same, they may are same objects or they may not.
[09:58] So to confirm if my
[10:00] and obj1 are stored at two different locations.
[10:03] I can try to compare them with the help of double is equal to
[10:07] operator.
[10:08] So here I'm trying to compare obj, obj1.
[10:12] If I try to run this program, we are going to get false,
[10:16] though the hashcodes are same
[10:17] we are getting false.
[10:18] That means they are stored at two different memory locations.
[10:23] With this I'm assuming you are clear about the two approaches that we have discussed.
[10:27] Always please use the first approach to create the objects of String, because it is going to save some
[10:34] memory and it is going to make your program to run fastly.
[10:37] You can go for the second approach only if it is required based upon your business scenario, sometimes
[10:43] based upon your business scenario
[10:45] maybe you want to create brand new object every time you try to store the data with the help of String class.
[10:51] In such scenarios, definitely you can go with the second approach, but those scenarios will
[10:57] be very rare inside your real projects.
[10:59] I hope you are enjoying the course.
[11:01] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

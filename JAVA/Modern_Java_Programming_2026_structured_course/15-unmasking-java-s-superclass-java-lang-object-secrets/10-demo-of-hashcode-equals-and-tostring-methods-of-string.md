# 15.10 — Demo of hashCode(), equals() & toString() methods of String

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Inside this lecture, let's try to understand how the methods of hashCode(), equals() and toString() are
[00:07] implemented in one of the famous data type that we have inside Java.
[00:12] Do you know what is this famous data type?
[00:14] Yes, you are correct.
[00:16] It is String.
[00:17] String is our best friend.
[00:19] Inside Java, whenever we want to store any kind of data inside String, we can store alphanumeric values,
[00:26] special characters.
[00:27] There is no restriction on what kind of data that we can store with the help of String data type.
[00:32] Since a String is a special data type, let's try to understand how these methods are implemented
[00:39] or overrided inside the String class.
[00:43] Here first, let me search for the String class which is present inside the java.lang package.
[00:48] Post that first we can look for the method toString().
[00:52] Let's try to understand what is present inside these toString() method.
[00:55] So you can see they simply overrided this method by mentioning
[01:00] return this.
[01:01] So when they say return these, what is going to happen?
[01:04] This method, it is simply going to return the same String object that you are using to invoke that
[01:10] toString() method.
[01:11] So the method comments also conveying the same like this object which is already a String is itself
[01:17] return.
[01:18] That's why you don't have to specifically invoke the toString() method whenever you want to print the
[01:23] String object.
[01:25] We can also see that demo of this very quickly.
[01:28] For the same, I'm going to create a new Java class.
[01:31] Inside this package and the class name I'm going to give as StringDemo.
[01:36] Inside the StringDemo, I'm going to create a String with the name str1, and by using the new keyword
[01:43] and the string constructor to the string constructor, I'm going to pass the name, which is John.
[01:49] After defining the String object, I can try to print the same onto the console by invoking the
[01:56] toString() method.
[01:56] You can also see I'm also getting a warning from the IntelliJ saying that friend, why are you trying
[02:02] to unnecessarily invoking this toString() method?
[02:05] Even if you don't invoke it, the method is going to be the same.
[02:09] That's what IntelliJ is trying to alert us.
[02:11] But that's fine
[02:12] just for demo, we can try to execute this method and see what we are going to get.
[02:16] You can see we are getting the same content that we are storing inside the String object.
[02:21] That's why whenever you are trying to print the String object, you don't have to invoke these toString()
[02:26] method because the toString() method which is present inside the String class, it is going to return
[02:32] the same String object.
[02:33] I hope you are clear.
[02:34] Now let's go to the hashCode() method and let's try to understand what is implemented inside these hashCode()
[02:42] method.
[02:43] So inside these hashCode() method there is lot of logic written by the Java team.
[02:47] But we don't have to put lot of efforts to understand what is happening with this code.
[02:52] Instead, we can simply read the method comments on how the hash code is going to be calculated.
[02:57] You can see the method comments there very clear this method
[03:01] it is going to return the hash code for the String.
[03:03] The hash code is going to be calculated with the help of this formula.
[03:07] So whatever first character available at the index zero inside your String, it is going to be fetched
[03:14] with the help of this s index of zero.
[03:17] And to the same
[03:18] the multiplication is going to happen with this value, and the same is going to be continued till the
[03:24] end of the characters available inside your String.
[03:27] So this also should give a confirmation to you if the content of the String object is same.
[03:33] We're always going to get the same hash code.
[03:35] Even though we created two different String objects inside the heap memory.
[03:40] I can also confirm you the same inside our StringDemo class.
[03:43] What I can do here is, I can try to create one more String object with the name str2 , and inside
[03:51] this str2 object
[03:53] also I'm going to store the same content which is John.
[03:56] So since we are using the new operator along with the constructor of the string behind the scenes,
[04:01] there will be two physical string objects will be created inside the heap memory.
[04:05] But we are going to get the same hash code value as an output, because inside the String class, the
[04:11] Java team, they have overrided the logic of hash code to generate the hash code value based upon the
[04:16] content, but not based upon the memory locations.
[04:19] So this is very important point.
[04:21] I hope it makes sense to you.
[04:23] I can also show you by printing the hash code values of str1 by invoking the hashCode() method.
[04:30] Similarly, I can do the same for str2 object as well.
[04:34] Now let me try to execute this program, and you'll be able to see that two different string objects,
[04:40] which are stored at two different memory locations, they have the same hash code value because the
[04:46] content is same.
[04:47] This time I'll try to change the content of the str2.
[04:51] Since the content of this str2 is different from the str1 object, obviously we are going to get
[04:57] that different hash code
[04:59] values.
[04:59] Here you can see we are getting a negative hash code value.
[05:02] This should also confirm another important point to you around hash code, which is hash code can be
[05:08] a negative value as well.
[05:09] So don't be under the assumption that hash code value will always be a positive value.
[05:15] Hash code value can be any value within the range of int data type.
[05:19] I hope this is clear.
[05:20] Now let's go to the String class.
[05:23] And this time let's try to understand what is present inside the equals() method.
[05:28] Inside the equals() method you can see they have written some logic.
[05:32] Let's try to understand what this logic is going to do by reading the method
[05:37] comments.
[05:37] The method comment says compares the String to the specified object.
[05:42] The result is going to be true if and only if
[05:46] the argument is not null, and is a String object that represents the same sequence of characters
[05:52] as this object.
[05:53] That means if both the given String objects, if they have same characters as a content, then always
[05:59] equals() method is going to return that true as an output.
[06:03] Let's confirm the same inside the String demo.
[06:06] So first I'm going to invoke the equals() method by using this str1 and passing these str2 as an
[06:13] input.
[06:14] Since we have different content inside them, we should get the output as false.
[06:20] We can also confirm the same by running this program.
[06:24] You can see we are getting the output as false.
[06:26] This time let's make the content as same and see if we are going to get the output as true.
[06:31] Hooray!
[06:32] We are getting the output like we expect.
[06:35] I hope you are clear how these important methods implemented inside the String class.
[06:40] Don't be under the assumption that if you try to create two different String objects, since the memory
[06:46] location is going to be different, the hash code will always be different.
[06:50] So don't be under that impression.
[06:52] The hash code value is always going to be same as long as the content is same, even though they stored
[06:57] at two different memory locations.
[06:59] So whenever someone is trying to trick you by asking questions around the hashCode() and equals(), you
[07:04] don't have to worry much.
[07:06] You just have to understand how the equals() and the hashCode() methods are implemented in a respective
[07:13] Java class.
[07:14] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

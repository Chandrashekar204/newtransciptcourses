# 19.6 — Collections with out Generics - Demo

> Section 19: Generics in Java

[00:00] Sometimes inside interviews, people may try to trick you by asking a question like create an array,
[00:06] List object or any Collection object and store different types of objects like a String object, Integer
[00:14] object, Boolean object, Float object.
[00:17] This kind of peculiar requirement they may try to give to you, to confuse you, and you might be under
[00:23] the impression that we can use collections only with the generics, and it may not be possible to store
[00:29] multiple data type objects around this scenario.
[00:33] I want to provide a clarity, which is we can use the collections without generics as well.
[00:39] That is perfectly possible inside Java.
[00:42] In fact, when Java started, all collections are not developed with generics.
[00:48] Generics came into picture in the later versions.
[00:50] So to provide that backward compatibility, even today, Java allows you to create the collection objects
[00:57] like ArrayList, LinkedList or any other collection object without any generics as well.
[01:03] Let me show you a demo around this.
[01:05] For the same, I'm going to create a new Java class which is WithoutGenericsDemo. Inside this class,
[01:12] first let me create the main() method, followed by
[01:15] I'm going to create an ArrayList object here the variable name
[01:20] I'll keep it as List followed by new operator followed by ArrayList constructor.
[01:25] You can see here I'm not using any generics.
[01:29] With this now,
[01:29] my collection is capable of storing any kind of objects.
[01:34] So this is one more difference between an array and a collection.
[01:39] With array we can only store the elements belong to a particular primitive data type or a particular
[01:44] object.
[01:44] Whereas with collections, if you don't use generics, you will get a flexibility to store any kind
[01:50] of object elements here inside this List, first I'm going to add a String object, which is hello,
[01:57] followed by next time I'm going to add into value.
[02:01] When I invoke the add() object, you can see it is trying to accept an object as an input parameter.
[02:08] Whenever we are not defining an generic while we are trying to create an ArrayList object or any
[02:13] List object, by default, all the methods are going to accept a object of type Object class.
[02:20] So that's what happening here.
[02:21] Now here let me try to send an input value which is 1, 2, 3.
[02:26] So though I'm sending the input data in a int primitive data type format, this is going to be converted
[02:32] into an Integer wrapper object with the help of Autoboxing.
[02:35] Next I'm going to add one more element which is Boolean value true.
[02:41] This way we can add any data type object into this ArrayList.
[02:45] But the problem with this approach is though, you are getting a flexibility to store any kind of object
[02:51] while you are trying to read these objects, you need to typecast them
[02:55] otherwise, you can't use these elements inside your business logic.
[02:58] For example, from this List, if I try to get the element which is present at the first index by mentioning
[03:06] zero on the left hand side, if I just mention object greeting as a variable name, you'll be able to
[03:12] see that I'm not going to get any compilation error, but with this object, I will not be able to invoke
[03:18] any String related methods, because as of now I got an object which belongs to Object class.
[03:24] But I know at the zero index I stored a String object.
[03:28] That's why I should be doing String typecasting.
[03:32] In order to convert this object as a String object. Post that I will be able to use a String related
[03:39] methods like toUppercase() or toLowercase().
[03:42] It's up to me what business logic I want to write.
[03:45] Similarly, let me try to copy the same code inside the second element
[03:49] we know we stored the Integer object.
[03:52] That's
[03:52] why I'm trying to typecast to Integer.
[03:55] And on the left hand side I'm going to mention int and the variable name as number.
[04:00] Similarly, in the next line I'm going to typecast this to boolean and the data type I'm going to mention
[04:06] as boolean
[04:07] on the left hand side. The variable name I'm going to mention as flag.
[04:11] So this way you need to do the manual typecasting instead of boolean.
[04:16] If you try to mention double, you are going to get a ClassCastException on the left hand side
[04:22] also, let me change this to double.
[04:24] If I execute this program, definitely I'm going to get a ClassCastException.
[04:29] So with this it should be pretty clear for you though
[04:31] generics
[04:32] they are giving an advantage or power to you to store any kind of objects.
[04:37] Along with this power, you're also going to get a drawback, which is around the casting.
[04:42] Whenever you are trying to do this casting, you need to be very careful and you need to do the proper
[04:47] casting.
[04:47] Otherwise you're going to get a ClassCastException.
[04:50] Whereas if you try to use generics in the same code, you can see it is going to be super safety and
[04:57] clean.
[04:58] So here after the
[04:59] ArrayList I'm going to mention String.
[05:02] And on the right hand side I'm going to mention a diamond operator and the variable name.
[05:06] I'm going to change it to List one, the same list one I'm going to mention in the next set of lines.
[05:12] This time you can see when we are trying to add the Boolean object and the Integer object, we are getting
[05:18] a compilation error.
[05:19] We are getting this compilation error due to a concept called type safety.
[05:24] Whenever you are using generics inside your code, the compiler will make sure that no other data type
[05:31] objects are being added into your Collection object or into any other object.
[05:36] So if anyone asks you what is the advantage that we are getting with the generics?
[05:39] The very first answer that you need to tell is type safety or compile time check, which is going to
[05:45] save us from manual casting and ClassCastExceptions.
[05:48] So let me comment these two lines of code just for your reference post that I'm also going to comment
[05:55] the last two lines.
[05:56] Now here I don't have to do these casting.
[05:59] I can directly read the element.
[06:02] Let me rename this variable name to greeting one here.
[06:05] Instead of List, I need to mention List one so that this compilation error is going to get resolved.
[06:10] If I try to execute this program this time, you can see I'm still getting a exception.
[06:14] Let me see what is the problem here?
[06:16] We are getting a ClassCastException at this line of code because we forget to update this index to
[06:23] 2.
[06:23] So this time they should not be any problem.
[06:26] Let me execute this program.
[06:27] You can see this time the program executed without any issues.
[06:31] I hope you got a clarity around the point, which is we can build a Collection object even without generics
[06:38] as well, and that is going to give an advantage to store any data type objects.
[06:43] But this power comes with a responsibility, which is you need to do a lot of casting, and you need
[06:49] to be very careful around the ClassCastException.
[06:52] The details that we discuss inside this lecture I have mentioned in this slide for your reference.
[06:56] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

# 19.10 — Unbounded Wildcards

> Section 19: Generics in Java

[00:00] Let's try to discuss about the last flavor of generics, which is unbounded wildcards.
[00:06] As of now, we saw the Upper bound and lower bound wildcards.
[00:11] But what is these unbounded wildcards?
[00:13] Let's try to understand the same.
[00:15] Whenever we want to use the unbounded wildcards, we just have to mention question mark inside the angle
[00:21] brackets. Like you can see here,
[00:22] list angle brackets inside the angle brackets I'm mentioning the question mark.
[00:27] So this is referred to as unbounded wildcard or unknown type.
[00:31] With this syntax we are telling that my List object is capable of storing any data type objects.
[00:38] With that you may have a question which is the same kind of functionality we are able to achieve with
[00:42] the simple generics as well.
[00:44] Instead of question mark, I can mention the char which is E representing an element.
[00:49] So with the List off E as well, we are able to add any kind of data type.
[00:54] Then why we should use these unbounded wildcards.
[00:57] So this can be your question.
[00:58] That's a great question.
[00:59] But I would request you to wait for a couple of seconds.
[01:02] I'm going to clarify your question.
[01:03] But before that let me clarify you under which scenarios we need to use these unbounded wildcards.
[01:09] We can't use these unbounded wildcards in all kinds of scenarios.
[01:13] The very first scenario is whenever you are trying to build a method that relies on the Object class
[01:19] functionality, like inside the Object class, we have various methods like hashCode(), equals(), toString().
[01:25] So whenever you are trying to deal with a method that will leverage the features provided by the Object class.
[01:30] In such scenarios, you can write a generic method with the help of unbounded wildcards.
[01:36] In the similar lines, if you are trying to build a generic class or a generic method independent of
[01:42] the type parameter in such scenarios, also you can use unbounded wildcards.
[01:47] For example, think like you're trying to build a logic.
[01:50] Inside this logic, you're going to rely on the methods like List.size(), List.clear().
[01:56] So in this kind of scenario, you're not going to use any logic to the specific data type.
[02:01] Instead, you are relying on the collection library methods like clear(), size().
[02:07] So regardless of whatever kinds of objects you're going to store inside the List object, the code is
[02:13] going to be the same when you try to invoke the size() and clear().
[02:16] So whenever you are trying to build these kind of logic, which is going to work irrespective of what
[02:22] data type objects you are trying to store, in all such scenarios, you can use the unbounded wild card.
[02:29] Now let's try to answer the question that you have.
[02:32] Think like I have built a method which is printList(), which is going to print the list of elements
[02:38] available inside a List object.
[02:40] Here, instead of the unbounded wild card, I have used the object as a data type.
[02:46] Similarly, I can mention character like E or T to use the normal generics. In the scenarios where you're
[02:52] trying to declare object or some generic character like E or D.
[02:58] In all such scenarios, the goal of printList() is going to fail, because we can only invoke this method
[03:05] with the help of List of object, but not with the List of integer or list of String or List of double
[03:12] or any other List.
[03:13] Storing a subtype of Object class.
[03:16] This is not allowed because List of Integer is not going to be considered as a subtype of List of object.
[03:23] We know collections don't use the covariance concept.
[03:27] That's why whenever you are trying to build a logic which is going to work for any kind of data type,
[03:32] always use the unbounded wildcards.
[03:35] Let's try to see how to build the same method with the unbounded wildcards like you can see here,
[03:40] this time inside the List angle brackets I have mentioned the question mark and with this anyone can
[03:45] invoke this printList() method.
[03:47] They can invoke with an List of integer or list of String, regardless of the data type object that
[03:53] they are trying to store inside the List object.
[03:55] Still, my method is going to work because with the help of these unbounded wildcards at runtime, this
[04:02] Integer is going to be replaced as Integer here.
[04:06] Similarly, here this String is going to be replaced as a String.
[04:09] Here let's see the example of Unbounded wild cards. Inside my IntelliJ
[04:14] I'm going to create a new Java class with the name UnboundedWildCardDemo. Inside this class
[04:22] first I need to write the main() method,
[04:24] after this main() method, let me try to create a method which is public static void and the method name
[04:32] I'm going to mention as printList().
[04:35] First, I'm going to create a List of object with the parameter name as List, and inside this method
[04:42] I can write some generic code like object with the variable name as obj that I'm going to iterate from
[04:49] the List object inside this,
[04:51] for each loop, I'm going to display the each element inside the List object. If needed,
[04:57] I can also try to display the size of
[05:00] the List by invoking the List.size() method.
[05:04] Now, since my printList() method is ready, let me try to invoke the same from the main() method.
[05:10] To this printList() method.
[05:11] I need to pass a List object which is only capable of storing an Object data type.
[05:17] That's why while I'm trying to invoke this printList() method, I'm going to send an ArrayList object
[05:23] which is only capable of storing Object class objects.
[05:28] So you can see there is no compilation error.
[05:30] But in the case of object, if I try to mention String and getting a compilation error
[05:35] similarly, if I try to mention integer and getting a compilation error.
[05:40] So we are trying to provide ArrayList of integer, but the method is expecting List of object.
[05:45] We are getting this compilation error because collections does not support covariance.
[05:50] To resolve these kind of issues, we need to use the Unbounded wild card.
[05:55] With this
[05:56] now we should be able to send any kind of List object to my printList() method.
[06:01] Let me try to create couple of List objects here.
[06:05] First one is going to store the Integer objects.
[06:08] To this,
[06:09] I'm going to assign a List by invoking the asList() method from the Arrays class. To this asList() method,
[06:16] and passing the values one, two, three.
[06:19] Similarly, let me try to create one more List, which is capable of storing the String objects with
[06:25] the variable name as ls.
[06:27] And here, instead of Integer objects, I need to pass String objects like one, followed by two followed
[06:35] by three.
[06:36] Let me try to send these toList() as an input to this printList() method.
[06:41] So I'm trying to first send the li as an input, followed by ls .
[06:46] You can see I'm not getting any compilation error.
[06:48] If I try to execute, this program will be able to see the values along with their total length.
[06:54] So whenever you have these kind of requirements where you want to write a method or a class which is
[07:00] going to have a logic that is going to be executed regardless of whatever the data type object.
[07:07] In all such scenarios, you can happily use these Unbounded wild card.
[07:11] I hope now you got a clarity around the generics.
[07:14] From now onwards
[07:15] anytime when you start working inside real projects, you may end up seeing lot many flavors of generics
[07:21] that we have discussed so far.
[07:23] You don't have to get scared.
[07:24] You just come to the course, try to revise what we discussed, and with that, you should be good and
[07:30] able to understand any kind of generics code.
[07:32] Before I try to close this lecture, let me discuss about the advantages of Java generics.
[07:39] We have three major advantages when we use Java generics.
[07:43] The very first one is type safety.
[07:45] If you're not using generics while you are trying to create the collection objects, then your collection
[07:51] object will end up with various kinds of objects, which may result into some issues at runtime.
[07:58] And on top of that, you need to write a lot of bad code to understand what kind of objects you have
[08:03] stored inside your Collection object.
[08:05] Whereas if you use generics while you are trying to create the Collection object, it is going to provide
[08:10] a type safety.
[08:11] And with this type safety, your Collection object is going to store only a single type of object.
[08:17] Coming to the second advantage, which is no type casting required.
[08:21] Whenever we are using the Java generics, there is no manual casting required.
[08:26] On top of that, with the help of Java generics, we can write a true polymorphic code, which is going
[08:32] to provide an advantage around the code reusability.
[08:36] The last advantage that we have is compile time check.
[08:40] With the help of Java generics, we are making our compiler to be more smart with the information that
[08:45] we provided.
[08:46] With the help of Java generics, the compiler is going to make sure that the developer is only adding
[08:52] the objects related to a particular specific data type.
[08:56] If you don't have generics at runtime, you're going to get a lot of exceptions like ClassCastExceptions.
[09:01] Since with the help of Java generics, the compiler is going to perform all the compile time checks.
[09:07] We can happily run our code without worrying about the runtime exceptions like ClassCastException.
[09:13] I hope you are clear about everything around that Java generics.
[09:17] So wherever possible, use them.
[09:19] Thank you and I'll catch you in the next lecture, bye.


########################################

# 17.9 — [JAVA 9] Creating Immutable Lists

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Sometimes we may have a requirement to create immutable list objects, just like how we can create normal
[00:08] immutable objects.
[00:09] Very similarly, inside Java, we can also create immutable collection objects.
[00:14] Here you may have a question which is what is the use case or the requirement to create an immutable
[00:22] list object?
[00:23] The answer is very simple.
[00:24] Sometimes you may pass on your list object or any other collection object to other methods to process
[00:31] the elements inside them.
[00:33] While you are trying to hand over your List object, you want to make sure you don't want the other
[00:38] methods to manipulate the data or to manipulate the elements present inside your List object or inside
[00:45] Collection object.
[00:46] In this kind of scenarios, we need to create the immutable List object.
[00:51] Let me show you an example so that it is going to be clear for you.
[00:55] For the same, I'm going to create a new Java class.
[00:58] The class name is ImmutableListDemo. Inside this class
[01:03] first let me create the main() method here
[01:06] first, I'm going to create an normal List object.
[01:09] Maybe using the ArrayList for the same I'm going to type List integer and the variable name I'm going
[01:17] to mention as accountNums.
[01:19] So I'm trying to store List of account numbers inside these ArrayList object.
[01:25] So using these account nums variable I'm trying to add various account numbers.
[01:31] Maybe I'll try to add some random account number.
[01:34] Think like this is a bank account number.
[01:37] Very similarly let me add few more account numbers.
[01:40] In total I'm trying to add three different account numbers.
[01:43] Now think like you are trying to hand over this List object or ArrayList object to some other method
[01:49] to process these account numbers.
[01:51] You may have a business logic which is to credit some amount into these bank accounts for the same.
[01:57] Let me write the private method like private static add $10.
[02:04] So this is the method name and the return type from this method is List of integer.
[02:10] Whatever List I'm trying to send, I want to return the same as an output from this method.
[02:16] So to this method the input
[02:18] obviously it is same as List of integer and the variable name
[02:23] I'm going to keep it as same, which is account names.
[02:26] So inside this method, as of now, I'm going to write a simple logic which is using for each
[02:32] I'm going to iterate all the elements inside my ArrayList object, and for each account number I'm
[02:38] going to credit $10 into their bank account.
[02:42] We're going to talk in detail about how to iterate the elements inside an ArrayList in the coming lectures.
[02:48] For now, let's try to use for each you know how to use for each to use the for each.
[02:53] First we need to type for and inside these first we need to mention Integer account :
[03:00] what is your collection object?
[03:02] Account numbers is the Collection object.
[03:04] So now this
[03:06] for each loop it is going to iterate all the account numbers inside my accountsNum Collection object
[03:11] inside my for each loop
[03:12] for each iteration, I'm going to simply have a System.out.println(), saying that $10 credited
[03:20] into the account colon, followed by I'm going to append the account number, and at last I want to
[03:28] return the same account numbers as an output from this method.
[03:33] So this private method I'm going to invoke from my main() method by invoking at $10 and passing the account
[03:39] numbers as an input.
[03:40] So if I try to execute this program, you will be able to see that the $10 is credited into these three
[03:48] different account numbers.
[03:49] Now think like some bad developer, he added his own account numbers so that he will get free $10 into
[03:56] his account number.
[03:57] So to achieve the same, what the bad developer is going to do is inside this method, he's going to
[04:02] invoke the add() method and he will add his own account number.
[04:06] Maybe he will add a account number which is 545634.
[04:11] Now if you try to execute this program, you will be able to see that $10 is credited into his account
[04:18] as well.
[04:18] So do you see the intention is getting changed because someone is able to change the list elements.
[04:25] To avoid these kind of problems, we need to make sure we are creating the immutable objects are immutable
[04:33] collection objects before we hand over them to the other methods
[04:37] inside your Java project, we can create immutable list objects inside Java in two ways.
[04:44] The very first approach is I can try to invoke the collections.
[04:48] Collections is an utility class which is present inside the java.util package.
[04:54] Inside this CollectionsUtility class you can look for the method which is unmodifiable
[04:59] list.
[05:00] So we have other methods also to create UnmodifiableCollection, UnmodifiableList, Map, Set.
[05:07] So since we are right now looking to create an immutable list object, I'm trying to invoke these unmodifiable
[05:14] list method. To this method
[05:16] I'm going to pass the account numbers as an input and the output
[05:20] from this method I'm going to catch into the same account numbers List object.
[05:25] After invoking this method, I can try to pass the same account numbers to the add $10 method.
[05:32] So this time if I try to execute this program, hooray!
[05:35] We are getting an exception saying that unsupported operation exception.
[05:40] That means if someone is trying to perform some alter operations on top of my unmodifiableList like
[05:48] add(), set(), delete(), remove() anything that they are trying to do which will alter the elements inside
[05:55] my unmodifiableList.
[05:57] They are going to get a runtime exception. My Java at runtime
[06:01] it is simply going to throw an error message saying that I'm sorry dude, I cannot change that.
[06:07] I'm not allowed to do that.
[06:08] How it is conveying it is conveying the same with the help of UnsupportedOperationException.
[06:14] So this is one approach of creating UnmodifiableList.
[06:18] But from Java 9 there is more easier approach is introduced.
[06:22] So let me show you how to do that.
[06:24] To create an unmodifiable list from the Java 9 version, you can straight away invoke of() method
[06:32] available inside the List interface.
[06:34] To this of() method, we can pass any number of elements as an object.
[06:40] This time I'll try to pass same account numbers by comma separated.
[06:45] So this is one of the easiest way of creating the List object. Behind the scenes,
[06:51] this of() method, which we are trying to invoke to pass various elements.
[06:56] It is going to give the object of one of the implementation of list class and this List object
[07:02] it is going to be immutable.
[07:04] So the output from this of() method I can try to catch on the right hand side, either in an ArrayList
[07:11] format or LinkedList format, or I can simply mention List and the variable name as
[07:20] immutableAccountNums.
[07:22] So now if I try to pass these immutableAccountNums and try to execute this program, you will be
[07:29] able to see the same exception which is UnsupportedOperationException.
[07:33] So whatever of() method that we are trying to invoke, this is introduced only from the Java 9 version.
[07:39] To make developer life easy to create ImmutableList objects with a very short code.
[07:45] So with this List.of() we are trying to do initialization and we are also making our List object as Unmodifiable.
[07:52] If needed, we can assign these immutableAccountNums to the ArrayList object.
[07:57] Let me show you how to do that.
[07:59] For the same,
[07:59] let me type var arrayListObject.
[08:03] And on the right hand side I'm going to invoke the array list constructor and mention the integer as
[08:11] the data type.
[08:12] And to this constructor I'm going to pass immutableAccountNums as an input.
[08:17] But please note that these ArrayList object which we have created from the immutableList, it is not
[08:23] going to be immutable.
[08:24] Let me show you the demo as well.
[08:26] If I try to pass this arrayListObject, the method is going to work without any exception.
[08:32] That's why anytime, if you want to pass an immutableList object, please only use these two approaches.
[08:38] One is with the help of List.of() and the other one is with the help of Collection.unmodifiedList()
[08:44] method.
[08:45] The same kind of concept applicable for other data structures
[08:48] also like Set, Map, which we are going to discuss in the coming sections.
[08:53] Whatever we discussed around the immutableList I have highlighted in this slide
[08:58] for your reference, the most preferred way is to use the of() static methods available inside the List
[09:05] interface, but please note that this option is only available from Java 9.
[09:09] I hope you are clear.
[09:10] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

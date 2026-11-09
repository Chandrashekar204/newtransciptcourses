# 26.19 — Finding and Matching methods in Streams

> Section 26: [JAVA 8] Streams API

[00:00] Streams
[00:01] API has some terminal operation methods, which is going to help you to find an particular element or
[00:07] to match a particular element.
[00:09] So these methods we call them as finding and matching methods.
[00:14] Under this category there are five different types of terminal operations or terminal methods are available.
[00:21] So these methods are allMatch(), anyMatch(), noneMatch(), findAny() and findFirst().
[00:27] I'm going to discuss in detail about all these methods by providing examples.
[00:32] But before I try to show you the demo, let me introduce about this method on a high level.
[00:37] So the very first method which is allMatch(), it is going to boolean value true as an output in the
[00:42] scenarios, if all your elements inside your stream are matched with the predicate condition that you
[00:49] have provided. But coming to the anyMatch(), it is going to give the output as true
[00:53] even if one of the element inside your stream is matching with the predicate condition and noneMatch(),
[01:00] it is going to give the output as true.
[01:02] If none of your elements inside your stream, they are matching with the predicate condition.
[01:08] And at last we have two methods which are going to help us to find an element.
[01:12] So findAny() will find any of the element that matches to your condition.
[01:18] Whereas the findFirst() method, it is going to give the first element present inside your stream that
[01:25] you built based upon some intermediate operation or based upon some business logic.
[01:30] The beauty of all these methods are they are going to work just like how we have logical and and logical
[01:36] or operations.
[01:37] What do I mean by they're going to work very similar to short circuiting operations.
[01:42] We have certain short circuiting operations like Logical AND and Logical OR when we are discussing
[01:48] about these logical operators.
[01:50] I told you that when you are trying to apply and operator based upon two different operands, if the
[01:57] first operand gives the output as false, then your Logical And operator, it is not going to evaluate
[02:03] the second operand because there is no need of evaluating the second element if the first operand itself
[02:09] is giving the output as false.
[02:11] Very similarly, in the Logical OR operation, if the very first element is giving the output as true,
[02:17] then it is never going to evaluate the second operand, because in the scenario of our condition, even
[02:23] if one of the operand is true, then the overall output is going to be true.
[02:27] So the same strategy here also these methods are going to follow especially like allMatch() and anyMatch().
[02:34] So allMatch()
[02:35] what it is going to do is, whenever it find an element which is not matching with your predicate condition,
[02:41] then immediately it is going to return the output as false.
[02:44] It is not going to evaluate the predicate condition on all the elements. In the similar lines,
[02:49] anyMatch() also
[02:50] it is going to give the output as true as soon as it identify a first element which matches to
[02:58] your predicate condition.
[03:00] The same principle applies to the other methods like findAny() and findFirst().
[03:04] So both these methods are going to return an element from your stream.
[03:10] In the scenario of findFirst(), it is going to be the first element and all the remaining elements.
[03:14] It is not going to look and bother about them.
[03:16] And similarly, inside the findAny(), it is going to randomly pick one of the element, and it is also
[03:23] not going to bother about all the remaining elements.
[03:26] So let's see that demo of all these methods. Inside intelliJ
[03:30] first I'm going to create an model class with the name Item.
[03:34] So inside Item I'm going to create good amount of fields.
[03:39] So let me paste these field details.
[03:41] Like you can see the very first field is name followed by price followed by a boolean which indicates
[03:47] whether a given item is in the stock, and the next one is a boolean field with the name on sale indicating
[03:54] whether a given item is on the sale.
[03:56] So based upon these fields, I'm going to generate the getter by considering all these fields.
[04:03] Later on, I'm going to generate the getter method for all these fields, and at last I'm also going
[04:09] to generate a toString() method, just in case we want to display the Item object.
[04:14] So let me press command N and select these toString() method.
[04:19] Inside this window
[04:20] please make sure you are selecting all these fields and click okay.
[04:23] And with that you have a toString() method implementation.
[04:26] So now I have my item Pojo class ready.
[04:30] As a next step I'll try to create a Java class with the name StreamFindMatchOperationDemo.
[04:39] Inside this class
[04:40] first I'm going to create the main() method post that
[04:43] I'm also going to create a static method, which is going to return me the list of item objects.
[04:50] Just to save some time here
[04:51] I'm trying to paste a static method.
[04:53] You can get the same method from the GitHub repo as well.
[04:57] So like you can see here this method whenever I
[05:00] work, it is going to return me a List object which is holding all these items.
[05:04] So first one is item name followed by what is a price followed by if the item is present inside the
[05:11] stock, followed by if the item is on the sale.
[05:14] Now from the main() method, I'm going to invoke the static method which is getItems(), and with that
[05:21] I'll be getting the output, which is a List object that is capable of storing all the items that we
[05:28] have populated inside this method.
[05:30] So let me give the variable name to the List object as items.
[05:34] Post that using these items I'm going to invoke the stream() method, and after this stream() method I'm
[05:42] going to invoke one of the terminal operation, which is all match to this allMatch().
[05:47] I'm trying to send a predicate condition which is Item::IsInStock.
[05:52] So what is this line of code it is doing?
[05:54] It is going to check if all my items are in stock, then it is going to return the boolean value as
[06:01] true.
[06:01] Otherwise I'm going to get the output as false.
[06:03] So let me catch the output with the help of boolean and with the variable name as all in stock.
[06:10] So obviously I'm going to get the output as false because this third item is not in stock.
[06:16] That's why if I try to print out these all in stock, I'm going to get the output as false.
[06:20] So you can see here I'm getting false.
[06:22] But if I try to make this third element also as true which indicates that this is also in stock, then
[06:29] I'm going to get the output as true.
[06:31] I hope this makes sense.
[06:32] Now let me revert back to false so that we get false as an output here.
[06:37] Next I'll try to invoke the anyMatch() method.
[06:41] So this time instead of all match I'm going to invoke anyMatch().
[06:45] And to this anyMatch() I'm going to pass the lambda expression with the help of isOnSale.
[06:50] So what I'm trying to do here i, if my any off product is enabled with the boolean isOnSale, then
[06:58] I want to catch the output inside a variable which is anyOnSale
[07:04] That means even if one of my item isOnSale, I'm going to get the output as true.
[07:09] So I think we are going to get the output as true because the smartphone, headphones and camera, they
[07:15] all have this last boolean as enabled.
[07:17] So this last boolean indicates on sale.
[07:20] So that's why if I execute this method this time you can see I'm getting the output as true.
[07:25] So anyMatch() is always going to look only for first element to satisfy your predicate condition.
[07:32] Next I want to check if any of my item is out of stock.
[07:37] Obviously one of the item which is headphone is out of stock.
[07:41] So if I want to check what I can do is, I can first copy these two lines of code and rename this boolean
[07:47] to anyOutOfStock.
[07:51] And here using these anyMatch() only I'm going to pass and predicate condition which is I'll take the
[07:58] item as an input followed by lambda expression.
[08:01] Inside the lambda body
[08:03] I will use the Item.isInStock() method to identify whether my item is in stock or not, but I'm
[08:11] trying to understand out of stock.
[08:14] That's why I'm going to mention a not operator just before my return type of my isInStock.
[08:20] And with that, we are going to get the output as true even if one of the item is outOfStock.
[08:26] So let me execute this program.
[08:28] You can see we are getting the output as true, but if you try to change this headphone boolean to true,
[08:33] then we are going to get the output as false because all the items are in stock.
[08:38] I hope this makes sense.
[08:39] Let me revert back to false so that we are going to get the output as true here.
[08:44] Next, let me show you the demo off noneMatch to show you the demo off noneMatch()
[08:49] the scenario that I want to consider here is I want to check if there is any item inside my List which
[08:56] has a price greater than $5,000.
[08:59] So to achieve the same, let me copy these two lines of code and paste it here.
[09:04] And instead of anyMatch(), I'm going to pass noneMatch() and post that I will write a predicate condition
[09:10] which is Item.getPrice() greater than $5,000.
[09:17] So if there is no element which has a price greater than $5,000, then I'm going to get the output as
[09:24] true, since we don't have any product with the $5,000 price in this scenario, we should get the output
[09:30] as true.
[09:30] So let me rename this variable name to ease any costly product.
[09:36] So these are random variable name that I want to give here.
[09:39] Let me use the same here.
[09:40] And if I try to execute this you'll be able to see true at the end.
[09:44] But if I try to give the value as $1,000, then obviously there are some elements like laptop camera
[09:52] which are greater than $1,000.
[09:54] That's why I'm going to get the output as false here.
[09:57] I hope you're clear.
[09:57] Let me revert back to $5000
[09:59] thousand dollars prize so that it is always going to return as true.
[10:03] Next, I'm going to show you the demo of findAny() by the same.
[10:08] First, using the Items list object, I'm going to create the Stream object, followed by
[10:14] I'm going to write a filter condition to identify the item details, which has a price greater than
[10:21] 1000.
[10:21] So the lambda expression I'm going to write is iterm lambda symbol followed by Item.getPrice() greater
[10:29] than 1000.
[10:30] So this filter() it is going to give me a new Stream object which has all the elements which has a price
[10:37] greater than 1000.
[10:38] After this I want to invoke that terminal operation which which is findAny().
[10:43] So when I invoke this findAny(), I'm going to get the output in the form of optionality.
[10:48] That's why on the left hand side I need to catch the output with the help of optional of item and with
[10:56] the variable name as randomItemOptional.
[11:00] So let me try to print out these optional to confirm what output we are going to get.
[11:06] So if I execute this program, you'll be able to see and getting an Optional object with the item details
[11:12] like laptop along with the price details.
[11:15] Similarly, with the same code, we can try to invoke the terminal operation which is findFirst().
[11:21] So this is always going to give the first matching element inside your stream.
[11:26] So that's why instead of randomItemOptional, I'll just mention these variable name as
[11:32] firstItemOptional.
[11:33] So if I execute this I'm going to get the output as the first item, which is laptop itself.
[11:39] Since we have very limited amount of data, we are getting laptop only in both the scenarios.
[11:44] But if you have large amount of data, findAny().
[11:48] It is always going to give some random element.
[11:51] You can also confirm the same by looking at the documentation of find any here they highlighted the
[11:56] behavior of this operation is explicitly non-deterministic.
[12:00] It is free to select any element in the stream, so this is to allow for maximal performance in parallel
[12:06] operations.
[12:07] So if you are not worried about only the first element, if you are only worried about any of the matching
[12:12] elements, you can always use the findAny() method.
[12:15] I hope you are clear with all these code snippets.
[12:18] Maybe behind the scenes
[12:19] I'll try to mention the comments for all these code snippets indicating what they are doing, so let
[12:24] me do that very quickly for you.
[12:26] Behind the scenes, I have populated the comments explaining about what this particular line is doing.
[12:32] So for all the examples that we have discussed, I have mentioned a detailed comments, which is going
[12:37] to help you to understand what we are trying to do inside these lines of code.
[12:41] The same code snippets that we have discussed so far
[12:44] inside this lecture, I have mentioned inside these two slides for your reference, so feel free to
[12:49] refer the same.
[12:50] I hope you are clear about these finding() and matching() terminal operations.
[12:54] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

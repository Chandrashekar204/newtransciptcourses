# 29.9 — [JAVA 24] Using Gatherer.of() to create an intermediate operation

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] Let me create a new class by simply copying the same class.
[00:05] But this time I'll try to name this class as B_Dev_FriendlyGatherer.
[00:12] Inside this class, we are going to use the developer friendly approach to create the Gatherer implementation.
[00:18] What I'll do is, I'll get rid of this entire code, followed by I'm going to invoke a factory() method
[00:25] available inside the Gatherer.
[00:27] This factory() method is of().
[00:29] If you open this of() method to the same, we need to pass the lambda expression, which is going to
[00:36] return the Integrator implementation.
[00:38] So what I can do is, I can try to define my second lambda expression that I have written previously.
[00:44] If I go to these HelloGatherer
[00:46] this is my second lambda expression.
[00:48] Let me copy the same and paste under this of() method.
[00:52] So do you see?
[00:53] This time we only have to write the second lambda expression.
[00:56] This makes creating gatherer easy.
[00:59] So if I try to execute this program this time also, I'm going to get the same output.
[01:04] We can further simplify this.
[01:06] Maybe what I can do is, instead of writing this entire code here, I can try to copy this entire code
[01:12] and paste as an input to this gather() method.
[01:15] If I try to paste the logic here and this time instead of toUppercase(), I will try to invoke that
[01:21] toLowercase().
[01:22] If I execute this program this time, all my output elements are going to be present in an lowercase
[01:28] letters.
[01:29] I know we are not able to see any difference.
[01:31] Maybe what I'll do is, inside the source elements
[01:33] I'll try to mention first letter as capital so that we can see that different inside the output.
[01:42] Once all the elements are updated, we can try to execute this program.
[01:45] This time you'll be able to see there is a difference between the source and the output list.
[01:50] Inside the output list, all the elements are having lowercase letters. So this confirms that this
[01:56] syntax is also acceptable.
[01:58] Right now we're seeing a warning here.
[02:00] We are nowhere using these Gatherer.
[02:01] That's fine
[02:02] I'm going to keep the score for your reference.
[02:04] We can further simplify these since we are not using these immutable state variable inside our business
[02:10] logic, we can replace this state with an unnamed variable.
[02:14] Unnamed variables are introduced as part of Java 22.
[02:18] Whenever you are into these kind of scenarios where you're not using the input variable anywhere inside
[02:23] your business logic, you can convert them as an unnamed variables.
[02:26] Here
[02:26] also, instead of state, I can mention unnamed variable.
[02:30] Let's try to understand the importance of the boolean variable that is being returned from this push()
[02:35] method.
[02:36] The beauty of this new stream gatherer API is with the help of the boolean.
[02:41] The downstream can always communicate to the intermediate operation that it is not going to accept any
[02:47] more new elements.
[02:49] For example, when you're trying to push an element to the downstream, if the output is false, then
[02:55] it is an indication to your intermediate operation that downstream it is not going to accept any more
[03:01] new elements.
[03:02] Even if you try to push them, the downstream is not going to process them, it is going to simply accept
[03:07] them, but it is not going to process any of the business logic.
[03:10] The same boolean output which we are receiving from the downstream into our intermediate operation can
[03:17] be sent as an output to the UpStream also.
[03:20] If you try to observe the method present inside the Integrator interface, this is also returning boolean
[03:27] variable.
[03:28] If you pass whatever you are receiving from the DownStream as an output from this method.
[03:32] The same can be communicated to the upstream as well.
[03:35] Based upon this boolean value, we are telling if the subsequent integration is desired or not.
[03:41] So based upon these boolean output that we are returning from this integrate() method, the UpStream object
[03:47] will also know whether to send further elements or not, with the help of these boolean outputs available
[03:53] inside these this integrate() and the push() methods, this API
[03:56] it is giving a flexibility to the developers to interrupt the stream processing whenever we want.
[04:02] For example, if your upstream is having 1 million elements and if you want to execute your integration
[04:08] logic only for 1000 elements, you can write a logic such a way that after the 1000 elements, you can
[04:15] tell to your UpStream, don't send any more new elements.
[04:18] I'm fine and I'm done with the logic.
[04:20] The same kind of flexibility the DownStream also can follow if the DownStream is happy with the received
[04:27] elements.
[04:28] And if you don't want to receive any further elements, it can communicate the same back to the intermediate
[04:33] operation.
[04:34] I hope you are clear on the purpose of these booleans as an output.
[04:37] Always your Integrated logic
[04:39] it should make sure it is returning a boolean value based upon this boolean value
[04:43] only the UpStream is going to decide whether to send any further elements to the custom intermediate
[04:49] operation that you have defined.
[04:50] With the help of Gatherer interface.
[04:53] We're going to see some examples focusing on these booleans alone in the upcoming parts.
[04:58] For now, let's try to build one more intermediate operation with the help of gatherer API inside these
[05:03] new intermediate() operation.
[05:05] I want to have both map() and filter() kind of logic before streams gatherer API
[05:10] if you want to apply map and filtering logic, you have to invoke two different intermediate operations
[05:16] with the name map() and filter().
[05:18] But right now, since we have some control on defining our own intermediate operations, we can try
[05:22] to have some fun by mixing the logic of map() and filter() into a single intermediate() operation.
[05:29] What I'll do is, I'll try to create a new Java class with the name C_MapFilterGatherer.
[05:38] Let me get rid of all this logic.
[05:40] I will simply have the Gatherer logic, which I'm going to overwrite the name of these gatherer I'm
[05:46] going to mention as filterAndMapGatherer as of now, Inside these Gatherer, we are simply performing
[05:53] the map logic where we are trying to transform each of the element to the uppercase value.
[05:59] But apart from transferring the element, I also want to filter the elements based upon some criteria.
[06:05] If the filtering criteria is satisfied, then only I want to push the element to the downstream.
[06:11] Otherwise I don't want to push the element.
[06:13] Since my business logic is going to have more than one line, I need to make sure I'm mentioning the
[06:20] curly braces. Inside these curly braces,
[06:23] I will try to write some business logic.
[06:25] I'll check if element.startsWith() a, then only push the element to the downstream, otherwise we
[06:33] don't want to push.
[06:34] So what I can do is, I can try to copy this entire code and paste it here along with the return statement.
[06:42] If this if block is getting executed, we're trying to push the element to the downstream by transforming
[06:47] it with the help of these toUppercase() whatever boolean that we are getting as an output from the push(),
[06:52] we are trying to return the same to the UpStream as well. For the remaining elements, which are not
[06:56] starting with the A.
[06:58] I don't want to push them to the downstream, and I also don't want to perform any transformation logic.
[07:04] Instead, I want to simply return true if I don't return this true.
[07:08] What is going to happen?
[07:09] The UpStream
[07:10] it is not going to send any new elements to my intermediate operation, so I should always make sure
[07:15] I'm returning a boolean value from my Integrator logic here
[07:20] If I mention false, the next elements will not be passed on to the intermediate operation that I have
[07:25] developed here.
[07:26] Our Gatherer is ready.
[07:28] We can use these gatherer as part of a stream pipeline first with the help of Stream.of().
[07:34] I'm going to create an upstream, which is going to have some values like apple, banana, avocado.
[07:41] After this upstream, I'm going to invoke the gatherer() method to this gatherer()
[07:46] I can pass my gatherer implementation by mentioning these filterAndMapGatharer(). Towards the end,
[07:52] I can try to invoke that toList() method.
[07:55] The output from this entire code I'll try to catch with the variable name as result.
[08:00] Let me print this result onto the console so that we can verify the output.
[08:04] If I execute this program, we should only see apple and avocado and these banana will get filtered.
[08:11] I'm executing this program inside the output
[08:13] we'll be able to see apple and avocado in completely uppercase letters.
[08:18] Let's see what is going to happen if you try to return false here.
[08:22] With this logic, we are going to return the false as soon as we process this banana after the second
[08:28] element
[08:29] since we are sending these false, the third element is not going to be sent by my upstream to my intermediate
[08:34] operation.
[08:35] If I execute this program, I'm going to get only Apple as an output
[08:40] off course, banana, even though it is passed to my intermidiate operation due to this filtering logic,
[08:45] it is not going to be pushed to that downstream.
[08:47] I hope you are seeing the power of these boolean.
[08:50] We are going to discuss more examples around these in the upcoming parts.
[08:54] In real projects
[08:55] don't try to define some simple logic with the help of your Gatherer.
[09:00] If some logic can be implemented with the help of the existing intermediate operations and terminal
[09:05] operations, please go ahead with them.
[09:07] Because creating intermediate operations with the help of these Gatherer, it is going to take some
[09:12] time
[09:12] and you should also define the Gatherer by following all these syntaxes.
[09:16] Go with these Gatherer implementation only if you have some custom business logic, which cannot be
[09:22] achieved with the already provided terminal and intermediate operations.
[09:27] Whatever examples that I'm going to show throughout these lectures, I'm trying to show them just to
[09:32] make you comfortable with the gatherer API.
[09:35] Once you are comfortable with the gatherer API, you can take the same knowledge into your real projects,
[09:40] where you can build any amount of complex logic with the help of your custom intermediate operations
[09:47] that you're going to build with gatherer API.
[09:50] So far, we explored on how to build an Gatherer by leveraging only the Integrator.
[09:56] In the next slide, I provided more details around Integrator.
[10:00] For example, what is a single abstract method that it has?
[10:03] What is the signature of it?
[10:04] What are the elements that it is going to accept as an input?
[10:07] What will be the output followed by?
[10:09] I also mentioned on how to create a sample Gatherer by using of() method inside the slide.
[10:16] In the next slide, I have an end to end example where I have built an IdentityGatherer
[10:22] this gatherer, it is not going to do anything.
[10:24] It is going to simply accept the input from the upstream and push the same to the downstream.
[10:29] Please try to build the same on your own to get comfortable with the gatherer API syntax.
[10:34] In the next slide, I have mentioned the same example that we have developed so far.
[10:38] Please refer to this slide whenever you want to quickly brush up around the gatherer API.

----------------------------------------

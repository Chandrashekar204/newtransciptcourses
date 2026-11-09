# 29.14 — [JAVA 24] Interrupting and Chaining Gatherers

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] When we are processing data with the help of Gatherer API. It is also going to give an flexibility
[00:07] or an option to the developer to interrupt the stream processing whenever developer wanted,
[00:13] based upon certain business logic.We know that the integrator logic that we are going to define at
[00:18] the end of the day, it has to return a boolean. Based upon these boolean that we are trying to return
[00:24] from our intermediate operation.
[00:25] The upstream is going to decide whether to send the next value or not for the intermediate operation.
[00:32] We already saw a demo previously where when I'm trying to return a false, the upstream is not sending
[00:37] any new values.
[00:38] That is one option of interrupting a stream when you are processing the data with the help of Gatherer
[00:43] API, based upon your business logic,
[00:46] If you feel some condition is met and you don't want to process any further elements, you can simply
[00:51] return false from your integrator logic.
[00:54] But sometimes we may not have any requirement to interrupt the processing in between.
[00:59] In this kind of scenarios, we are always going to push the elements to the downstream.
[01:03] If your downstream is accepting a limited number of elements. In this kind of scenarios,
[01:09] It is always a wise decision to return whatever boolean value that you are getting from the push() method
[01:16] to your upstream as well from the integrator logic.
[01:20] If you always try to return true from the integrator, then you're going to miss these kind of scenarios
[01:25] where your downstream is accepting only a limited number of elements.
[01:30] Here I have an example where I have built an upstream, which is going to hold 1000 integer elements.
[01:36] If I use this as an upstream and invoke the gather() method to the gather() method, you'll be able to see
[01:42] I'm passing limitGatherer implementation. Inside the limitGatherer,
[01:47] I'm simply trying to push the elements to the downstream from the upstream, but you can imagine in
[01:53] your real applications you may have some complex business logic before you try to push the element to
[01:58] the downstream.
[01:59] The main important point that I'm taking care here is I'm trying to return whatever boolean value that
[02:05] I'm receiving from the push() method of the downstream. Since I also have another intermediate operation
[02:11] limit which is going to accept only 10 elements.
[02:14] This is going to act as my downstream.
[02:16] After accepting 10 elements. The downstream it is going to return false as an output from the push() method.
[02:23] If I pass the same false as an output from my integrator logic, only the first 10 elements inside
[02:29] my upstream, they are going to be processed.
[02:31] And with that I can have some performance improvement inside my program.
[02:35] In this scenario, instead of returning the output from the push.
[02:38] If you try to return manually a true value always, then you will end up keep pushing the elements from
[02:44] the upstream though they won't be any exception happening.
[02:48] If you try to push an element into a rejecting downstream, but still you will have some performance
[02:54] issues.
[02:54] Let's see the demo of this example.
[02:56] I created a class with the name G _ InterruptGatherer, and here inside the main() method
[03:02] I am trying to pace few lines of code.
[03:04] All this code you can get from the GitHub repo.
[03:07] I'm trying to do this just to save some time.
[03:10] Since we already discussed everything about this logic.
[03:13] They should not be any confusion. But I'll try to discuss one more time,
[03:16] let me print the result with the help of System.out.println().
[03:20] At the very starting of the main() method, I'm trying to create a list that is going to hold 1000
[03:27] integer values.
[03:28] Using the same largeList(), I'm trying to invoke the stream() method followed by gatherer.
[03:33] To the gatherer() method I'm trying to pass limitGatherer.
[03:37] Inside the limitGatherer I have written the logic just to push the elements to the downstream.
[03:41] I'm not trying to execute any other logic.
[03:44] After the gather intimate operation, I'm trying to invoke one more intermediate operation with the
[03:50] name limit.
[03:51] So this is going to act as a downstream, since this downstream has some restrictions to accept only
[03:56] 10elements. This downstream will start sending the Boolean value as false after 10 elements.
[04:03] If you return the same to the upstream, we will save some performance.
[04:07] I'm going to execute this program since I had the System.out.println() statement inside my integrator.
[04:13] We can easily identify how many elements are being processed by my integrator logic.
[04:18] Let me execute this
[04:19] as you can see, only the 10 elements are processed and towards the end all these 10 elements are
[04:26] pushed to the downstream,
[04:27] that's why we are seeing this list as an output.
[04:30] In case if you have a requirement, you can also manually check whether downstream is accepting any
[04:36] elements or not.
[04:37] How to do that?
[04:38] With the help of these downstream, you can invoke a method isRejecting()
[04:43] If this isRejecting(), is returning true, it is a confirmation to you that downstream is right now
[04:50] in the rejecting mode.
[04:52] Always remember three thumb rules.
[04:54] The first rule is downstream is always going to start in an non rejecting state.
[05:02] The second rule is once the downstream is entered into the rejecting state, it cannot come back to
[05:08] the non rejecting state.
[05:10] The last rule is the state of the downstream from non rejecting to rejecting,
[05:15] It is going to only happen when you are trying to push an element into the downstream.
[05:20] So these are the three thumb rules.
[05:21] Please make a note of them.
[05:23] I'm going to mention these rules as it is inside this class in a commented form,
[05:27] for your reference.
[05:28] As a next step, let's try to understand how to chain multiple gatherers. Inside Gatherer interface,
[05:35] there is an method with the name and then with the help of these andThen() method, we can chain multiple
[05:42] gatherers.
[05:43] Let me create a new Java class with the name H_ChainingGatherer.
[05:49] First, let me define a main() method.
[05:52] Inside this main() method I'm going to define two different gatherers.
[05:57] These are simple gatherers that I'm trying to create just for our demo purpose, the first gatherer,
[06:03] It is going to accept integrator logic. Inside the integrator logic,
[06:07] I'm trying to simply push the element to the downstream after converting the string element to an completely
[06:13] uppercase value.
[06:15] I also have another gatherer, which is going to check whether the element is starting with a value J.
[06:21] .
[06:21] If yes, then only push the element to the downstream, otherwise the element is not going to be pushed.
[06:26] Let's try to understand how to chain both these gatherers.
[06:30] With the help of stream.of(), I'm going to create an Stream object to this of,
[06:36] I'm trying to pass elements like Java Spring react as an input, followed by I'm going to invoke gatherer
[06:44] as a first gatherer,
[06:45] I'll try to pass these upper gatherer by providing the variable name.
[06:51] Against to these upper gatherer, I need to invoke andThen() method to this andThen() method,
[06:56] I'm going to pass one more gatherer as an input.
[07:00] What is that second gatherer that we have?
[07:02] It is filter.
[07:03] And towards the end I'm going to invoke that toList() method.
[07:07] So here I'm trying to perform the chaining of gatherer by using these andThen() default method.
[07:14] Let me catch the output ,the output
[07:16] we can also try to print out with the help of System.out.println().
[07:20] Let me execute this program.
[07:22] As you can expect, we received JAVA as an output because all the remaining elements, they are filtered
[07:30] by the second Gatherer.

----------------------------------------

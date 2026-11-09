# 30.7 — [JAVA 25] Scoped Values - Part 1

> Section 30: New features from Java 25

[00:00] As part of the Java 25 release.
[00:03] A new feature with the name Scope to Values is released.
[00:06] This feature is an interesting and complex one as well.
[00:10] That's why first, we'll try to understand the background of this scope to values and how to use them
[00:16] in a multithreading environment.
[00:18] By looking at the examples inside the slides later, we can see that demo as well.
[00:23] So what are scope to values?
[00:25] By using the scope to values, we should be able to share immutable data between a method and its colleagues
[00:34] without explicitly passing that data as method parameters.
[00:38] We know inside Java, a thread is responsible to handle a request, and as part of the request business
[00:44] logic, multiple methods will be executed.
[00:47] When a thread is calling a method like M1, this m1 may call other method like m2 from m2, it may call
[00:54] to M3 and this way in real enterprise applications are inside framework code, a good amount of methods
[01:02] will be called internally from one method to other method.
[01:05] So if you have a scenario where you want to share the data in between these methods, like if I want
[01:11] to share the data from these M1 to M4.
[01:14] We have various options inside Java.
[01:17] These scope to values is a modern approach to share the data between the methods without explicitly
[01:23] passing as a method parameters.
[01:25] We're going to explore more details around this.
[01:27] We can also pass the data between parent and child threads by using the scope to values.
[01:33] So these scope to values are alternatives to the thread.
[01:37] Local thread locals are available from last few decades inside Java, but they have their own complexities
[01:44] and drawbacks.
[01:45] By using these scope to values the Java team, they're trying to overcome the challenges around the
[01:50] thread local.
[01:51] I'll discuss in detail what are thread local and what are the drawbacks that they have in few seconds.
[01:56] But before that, let's try to understand what are the various options that we developers has to pass
[02:02] the data in between multiple methods.
[02:04] The most basic option is by passing the data as method parameters.
[02:10] For example, here I have a class with the name order service.
[02:13] For simplicity, I make sure all these methods are present inside the same class, but the methods can
[02:18] belong to other classes as well.
[02:20] If you closely understand there is a process order method and this method it is internally calling other
[02:26] methods like validate order, calculate price and save order.
[02:31] So this process order from some place it is receiving the input parameter data like order details and
[02:39] user context details.
[02:41] Inside this context, we'll have details around the logged in user.
[02:45] Since these user context details are required inside the methods like check user permissions and apply
[02:52] user discount, which are being called inside the methods like calculate price and validate order.
[02:58] So what is happening here?
[02:59] So from process order we are passing these context details as a method input parameter for all these
[03:05] validate order and calculate price and save order method inside the validate order method.
[03:11] Again, there is another method invocation with the name check user permissions.
[03:15] So this method requires the context details to check the user permissions.
[03:20] The same applies for the apply user discount method as well.
[03:23] This method also requires user context details to apply the discount.
[03:27] So if you see the drawback here, though, the in-between methods like validate order and calculate
[03:32] price.
[03:33] They are not using these context details anywhere in their business logic, but they are forced to accept
[03:39] this information as method parameter just for the reason that they have to pass the same information
[03:44] to the other methods that are being invoked in these methods.
[03:48] This may not look like a problem to you, because right now we are only into two layers.
[03:53] So from this method we are calling this method, and from this method we are calling other method.
[03:57] But in real enterprise applications are inside the framework code.
[04:00] Like spring, we may have tens and sometimes hundreds of method layers where M1 method may invoke m2
[04:08] and m2 may invoke m3, and so on up to method 50.
[04:12] For some reason, if method 45 requires some information, if we follow this approach, all the above
[04:19] methods like M1, M2, M3, m4 and so on up to M45.
[04:24] They have to accept the details as method parameters.
[04:27] Due to these disadvantages, this is not a recommended approach, especially inside the enterprise code
[04:32] and framework code.
[04:33] That's why inside industry developers they call this disadvantage as parameter passing hell.
[04:40] So we are passing good amount of parameters and that may result into a lot of code.
[04:46] That's why the senior developers, they are not going to use these very traditional basic approach.
[04:51] Instead all these days developers, they are using the Threadlocal approach.
[04:56] We know all the methods inside Java.
[04:58] They are going to be executed by threads.
[05:00] When a thread is executing a method, we can create a variable which is specific to a given thread.
[05:07] That's why this name thread local.
[05:09] So there is a class inside Java with the name thread local.
[05:12] If you look at this example, I have considered the same order service class at the top I have created
[05:18] a thread local variable with the name context and inside this thread local object I'm going to store
[05:25] the user context object.
[05:27] When we declare this constant.
[05:29] Under this user context, we may have some initial details or null details, but inside the business
[05:34] logic we can update these context details.
[05:37] For example, under this process order.
[05:39] Since this process order is going to receive the user context details from the caller method inside
[05:46] the same method, we can invoke the set method by using the context variable of type thread local.
[05:52] So here we are setting the user context details that we have received.
[05:57] So at the top method we can update that data inside the thread local object.
[06:03] And the same can be accessed anywhere inside any method which is being executed as part of the same
[06:10] thread.
[06:10] So when a thread start processing these process order method so the same thread, it is going to invoke
[06:17] the validate order, calculate price and save order.
[06:21] Let's imagine I need these user context details inside one of the method with the name validate order.
[06:27] So to this method we're not passing any context details as an input, but still this method can access
[06:33] that context information available inside the thread local object by invoking the get method against
[06:40] this context variable.
[06:42] So when this Get method is invoked, it is going to get the user context object, which we stored inside
[06:47] this variable.
[06:48] And the same context details can be passed to other methods or can be used inside any business logic.
[06:55] So the advantage that we are getting with the thread local here is we don't have to manually pass the
[07:01] context details to each method by using the method parameters.
[07:05] So with that, a major problem is solved and most of the senior developers who write the enterprise
[07:10] code and framework code like Spring spring Boot.
[07:13] They are using these thread locals to a great extent.
[07:17] Once the developer feels like that, all the business logic is executed and no more wanted the details
[07:24] stored inside the thread.
[07:25] Local object.
[07:25] Towards the end, the developer has to invoke the remove method by using the same context variable.
[07:32] So this is going to remove the data that we stored inside the thread local.
[07:37] So invoking this remove method is super important.
[07:41] Otherwise the same data is going to be stored inside the thread unless the thread is shut down or unless
[07:48] the thread is died.
[07:49] The data that we stored is going to be stored forever.
[07:53] So this thread local approach is working for developers, but it has some serious drawbacks.
[07:59] Let's try to understand what are those?
[08:00] The first major problem is whatever data that we store inside the thread locals.
[08:06] It is not immutable, so anyone can change the data by invoking the set method.
[08:11] For example, inside method one, I may update the data like method inside the Threadlocal, but the
[08:18] other method that we are invoking from the same thread, it may update the value to some other name
[08:24] like John.
[08:25] So this will be a problem, because any method that is being executed by the thread can mutate the data
[08:31] that we stored inside the threadlocal.
[08:33] To debug any runtime issues or defects around these threadlocal, it is going to be a lot of work to
[08:40] the developers because they clearly can't track which method update to what value, and this will result
[08:46] into some unexpected results as well.
[08:49] The next problem is around the unbounded lifetime.
[08:53] As I said before, when these threadlocal is being used, once the data is set and once the data is
[09:00] retrieved by using the set and get methods, and once the developer feels like he is done with the thread
[09:07] context data, the developer has to make sure to invoke the remove method.
[09:11] But in reality, most of the developers, they are not invoking this remove method, even in the enterprise
[09:16] applications as well.
[09:17] And with that, what is going to happen?
[09:19] The data is going to store forever inside that thread, inside Java and inside frameworks like spring,
[09:26] there is a concept called thread pool.
[09:29] So as part of this thread pool, what the developer or what the framework is going to do is they're
[09:34] going to create a good amount of threads like maybe 50 or 100, and they are going to maintain all these
[09:41] threads into the pool.
[09:42] Since the creation of a thread is a time consuming operation, usually during the startup, the framework
[09:50] are the developers, they're going to create a required amount of threads like 50 and 100, and they
[09:55] are going to maintain inside a pool.
[09:57] So whenever a request comes, the thread will be retrieved from this pool and will be assigned to the
[10:02] request handling.
[10:03] And let's imagine as part of a request handling, I stored some data into a thread with the user information
[10:12] and once the request is done with these request to processing, the same thread will go back to the
[10:19] thread pool.
[10:19] Next time when another request comes, the same thread will be assigned to the new request.
[10:24] And if the new request also is setting some some other data or some other information inside the thread
[10:30] local.
[10:31] So this way the same thread will end up storing a good amount of data because we are never shutting
[10:38] down the thread, or we are never killing the thread from processing the request.
[10:43] The shutting down of the threads inside the thread pool will only happen when the application is getting
[10:48] restarted, or when it is getting shut down.
[10:51] So with the thread pool concept, the thread is going to have unbounded lifetime.
[10:56] And if the developer forgets to invoke the remove method, all the data that we are trying to store
[11:01] inside the thread locals, they are going to be increased exponentially and at some point of time we
[11:07] are going to have memory footprint issues or memory leak issues as well.
[11:11] So what is a memory leak?
[11:12] Let's imagine a request to one is processed by thread one, and as part of this request one, I stored
[11:18] some data like modern using the thread local.
[11:22] If I don't invoke the remove method and the request is processed, the thread will go back to the thread
[11:27] pool and for the request two if the same thread is assigned.
[11:32] So this request will have the information around the modern because this information is still hang to
[11:42] this thread t1.
[11:43] Due to this, what is happening?
[11:44] The memory is getting leaked from one request to other request and this may result into security vulnerabilities,
[11:51] memory issues and performance issues.
[11:54] The third problem that we have with the thread local is expensive inheritance.
[11:59] When we are creating a thread, we can also create it.
[12:03] A child threads by using the inheritance concept.
[12:06] So I can create a child thread.
[12:08] So if this is a parent thread, the child thread, it is going to inherit all the data that we store
[12:14] inside this parent thread by using the thread local concept.
[12:17] If I end up multiple channels and subchannels of a thread at some point of time, the most recent child
[12:23] thread, it will end up storing all the memory that we stored inside the parent and super parent threads.
[12:31] Using this thread local that will result into memory overhead, especially with the virtual threads.
[12:37] So virtual threads is a new concept which is introduced in Java 21.
[12:41] We know virtual threads are lightweight threads, so from a single platform thread we can create millions
[12:49] of virtual threads.
[12:50] And if all these millions of virtual threads inherit the data from the same platform thread, it will
[12:56] leads into memory overhead.
[12:57] That's why to resolve all these problems, especially since nowadays the developers are inclined to
[13:04] use the virtual threads in new modern approach is introduced with the name scope to value.
[13:10] With the scope to values.
[13:11] We are going to overcome all the disadvantages of thread local.
[13:14] Let's continue this discussion in the next lecture as well.

----------------------------------------

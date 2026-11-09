# 30.8 — [JAVA 25] Scoped Values - Part 2

> Section 30: New features from Java 25

[00:00] Let's try to understand how these scoped values is going to help us compare to the thread.
[00:06] Local option a new class with the name scoped to value is created inside the Java library.
[00:12] By invoking a static new instance method.
[00:15] Inside this class, you should be able to create a scoped to value object, and inside the scope to
[00:22] value object, you should be able to store any kind of information.
[00:25] Here I'm trying to store user context information.
[00:28] The variable name I have mentioned context itself.
[00:32] Now let's try to understand how to leverage the scope to values to pass the data across multiple methods.
[00:39] We have the same class order service and process order method.
[00:43] The process order method.
[00:44] It is going to receive some user context information inside this process order.
[00:49] By using these scoped to value class, we need to invoke a very static method to this.
[00:56] Where.
[00:56] Static method.
[00:57] We need to pass our scope to value variable name, which is context.
[01:01] Along with that, we should also pass what information we want to store inside this context variable.
[01:07] Since we are looking to store this context object, I'm passing the same as a second parameter to the
[01:12] where method.
[01:13] This way you can invoke this where method multiple times and you should be able to store any amount
[01:18] of data.
[01:19] Just like how we have this context variable, I can create one more variable and store some other information
[01:26] by invoking the where method one more time here.
[01:29] So once we satisfied offsetting the information into the scoped variable, we need to invoke a run method.
[01:37] To this run method, we need to pass a lambda expression.
[01:41] By using this lambda expression, we can invoke all the other methods that we want to invoke from this
[01:49] method.
[01:50] So here I want to invoke the validate order method, calculate price method and save order method.
[01:57] Whatever methods that we are invoking as part of this run method, those methods will have access to
[02:04] the scope to variable context.
[02:07] For example, here inside these validate order method by simply calling context dot get.
[02:13] I should be able to get the user context information and the same information I can use inside the business
[02:20] logic.
[02:21] If any method is invoked inside this process order method outside of this run logic, those methods
[02:28] will not have access to these scoped variable context information.
[02:33] If they call these Get method, they are going to get a runtime exception.
[02:37] I'll show you all these details in a demo in a few minutes.
[02:39] Let's see a simple example.
[02:41] So here I have a class with the name Simple example itself.
[02:45] And inside this class I created a scoped variable by invoking the new instance method.
[02:50] For this scoped variable, I have given a variable name as user underscore name, and inside this scoped
[02:57] variable I'm storing string data.
[03:00] So there is a method do work.
[03:02] And when someone invoke these do work method, I'm assigning a value allies to these user name by invoking
[03:10] the scoped variable dot where method.
[03:13] So once the assignment of the data to the scoped variable is done by using the run method, I'm passing
[03:19] a lambda expression.
[03:21] Inside this lambda expression, I'm invoking another method with the name process task.
[03:27] So inside the process task I can simply call username dot get method, which is going to give me the
[03:34] data that I stored allies the same.
[03:36] I can print it here.
[03:38] And from this process task if I invoke another method like call another method.
[03:43] So this call another method also will have access to the username data.
[03:48] It can simply invoke the get method which is going to provide the same username details.
[03:53] So this way inside any method that are being invoked under the same thread that is being executed,
[03:59] this run method.
[04:01] So all those methods, they should be able to access the scoped value data.
[04:05] But any logic or any method which is trying to access this username information outside of this run,
[04:11] they will not be able to access this information since the value is scoped to only to this run method.
[04:19] This name has been given which is scoped values.
[04:21] Anyone who is trying to access outside of the scope, they will not be able to access it.
[04:27] They will get an runtime exception.
[04:29] That's why it is always a good practice to check if the scoped value has any data bounded.
[04:35] If yes, then only we should invoke the get method, otherwise we should not invoke.
[04:39] I'll show you how to check whether a scoped value has any bounded value in the demo that we are going
[04:45] to discuss.
[04:46] So whatever scope that we are maintaining by using the scoped value.
[04:50] In other words, we can call it as dynamic scope because based upon what content are what methods we
[04:57] are invoking inside this method, the scope of the variable is going to be decided.
[05:02] So since inside the run method, they're calling the method b, and from method b they are calling method
[05:07] C.
[05:07] Both these method B and method C, they will have access to the scoped variable name.
[05:13] Any code outside these run logic, it will not have access to these named scoped variable.
[05:18] When we are using scoped variables.
[05:20] It is also possible to define some nested scope or rebinding scope.
[05:26] Let me show you how this is going to work.
[05:28] So here first I have created a scoped variable with the name level and inside the scoped variable I'm
[05:35] trying to store the string data.
[05:37] So there is a outer method inside this outer method.
[05:40] First I have assigned the level as level one.
[05:43] After the assignment of the data into the scoped variable, I'm invoking the run method inside the run
[05:48] method.
[05:48] If I try to invoke this level dot get, obviously I'm going to get the output as level one.
[05:54] After this println statement, I'm invoking the inner method.
[05:57] Inside the inner method I'm again invoking the level dot get.
[06:02] And here also I'm going to get the level one as an output.
[06:05] But in the next statement I'm trying to bound a new value to the same scope to variable with the name
[06:12] level.
[06:12] The new value that I'm trying to bound is level two.
[06:16] Once the new value is bounded, I'm trying to invoke the run method, and inside this run method, I'm
[06:21] trying to invoke the deep method.
[06:23] Before that deep method invocation.
[06:25] I'm trying to print the level dot get value, and here we are going to get the new value that we assigned,
[06:31] which is level two.
[06:32] And inside that deep method also we are going to get the value as level two.
[06:36] But outside of this run, if we try to print level dot get, we are going to get the level one as the
[06:43] output.
[06:44] So whatever new data that we are setting that will only be bounded to the methods or logic that we are
[06:52] going to invoke inside this run method.
[06:54] And once we are done with this method, if you go back and if you try to execute the System.out.println
[07:00] here, we are going to get the output as level one because we are present inside the first run method
[07:06] scope.
[07:06] So this way we can create a nested dynamic scopes by using the scoped values.
[07:13] So here inside this deep method, if I assign some other value to my scoped values by invoking the wear
[07:19] and run methods, then whatever logic that I'm going to write inside the run method of these deep method,
[07:25] it is going to have a new scope values.
[07:28] So this way I can define nested scopes.
[07:31] So with nested scopes we are going to avoid all the disadvantages of threadlocal.
[07:36] So inside Threadlocal the developer has to invoke the remove method manually.
[07:42] But here the developer they don't have to invoke the remove method because as soon as the Java is done
[07:48] executing these run logic, it is going to automatically remove these level two from these level scoped
[07:56] values.
[07:56] And once these method is executed, it will go back to the outer method.
[08:01] Once this outer method is done with its run logic, whatever level one that we stored inside this level,
[08:07] it will automatically removed.
[08:09] And by the time this entire method gets executed, the scoped value that we stored inside this level.
[08:15] Along with this level scoped variable, everything will be removed by that Java library itself.
[08:20] So with that, we solved the very first disadvantage of scope thread locals, which is unbounded lifetime
[08:27] and coming to the mutability issue.
[08:29] When we are using the scoped variables, we can only set the data once by invoking the where method.
[08:36] If we try to invoke the where method again in a new method, then it is going to have a new nested scope,
[08:45] and this way the developers, they are going to have a clarity around the scope of the nested variables.
[08:51] And they will also going to have some clear clues on how the scoped value is being changed due to the
[08:56] nested scope concept.
[08:58] So when we are using the scoped variables, the data is always going to travel in an unidirectional.
[09:04] Whereas when we are using the thread locals, the data can travel in bidirectional flow, which is causing
[09:11] a lot of problems to the developers.
[09:13] And coming to these expensive inheritance, this is not going to be a problem again in the scenario
[09:19] of scoped variables, because when we are storing the data inside the scoped variables, the data is
[09:24] getting automatically removed.
[09:25] As soon as the logic that we have written inside the run method is done with the execution.
[09:30] So with these new modern approach of scoped variables, there won't be any memory overheads.

----------------------------------------

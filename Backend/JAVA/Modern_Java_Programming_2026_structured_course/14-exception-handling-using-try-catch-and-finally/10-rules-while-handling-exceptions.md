# 14.10 — Rules while handling exceptions

> Section 14: Exception handling using try, catch and finally

[00:00] Let's discuss the rules and guidelines that we need to follow while handling the exceptions inside a
[00:07] Java program.
[00:08] The very first rule is the try block is always mandatory.
[00:12] Without a try block, you can't write exception handling by using only catch and finally blocks.
[00:20] Always
[00:20] the very first block that you need to define is try block.
[00:24] For example
[00:25] here you can see I have written a method where I have only catch block, but there is no try block.
[00:30] So this is not going to compile because inside Java try block is always mandatory
[00:36] and in this scenario, since try block is missing, we're going to get a compilation error.
[00:40] Let me show you a demo around this
[00:42] you can see inside this ExceptionDemo class
[00:44] as of now I have try, catch
[00:46] and finally for a second let me remove these try block parentheses and try keyword
[00:51] and with that you can see I'm getting a compilation error saying that catch without try.
[00:57] And similarly finally without a try.
[01:00] So this confirms we can't write, catch or finally blocks without defining a try block.
[01:07] The second rule is we are not allowed to define any code between a try block and catch block and finally
[01:14] block.
[01:14] If you try to be oversmart and try to write a piece of code in between your try and catch or try and
[01:20] finally or catch
[01:21] and finally, in all such scenarios we are going to get compilation error.
[01:25] I can also show you a demo very quickly.
[01:27] So here just after that try block and before that catch block I'm going to simply write a System.out.println().
[01:35] You can see I'm getting an immediately an exception saying that catch without a try.
[01:39] That means my catch block does not have any clue where the try block is present, because we have break
[01:45] the relationship between them by adding a code between them the same kind of behavior you will be able
[01:51] to see if you try to add a code between catch
[01:54] and finally, in this scenario also you can see finally without try we are getting this compilation
[01:59] error.
[02:00] So that's why I always make sure you are not writing any piece of logic between your try and catch,
[02:06] try and finally catch and finally.
[02:08] Otherwise your Java program won't compile.
[02:11] The third rule is, try should always be followed with a catch, or finally, or both.
[02:18] We need to have at least either catch or finally is present.
[02:21] If needed
[02:22] we can define both of them as well.
[02:24] So these are all the valid syntaxes.
[02:27] A try followed by catch, try followed by finally, or try followed by catch and finally.
[02:32] So let's see the demo around this as well.
[02:34] So here you can see if I try to delete these catch
[02:37] and finally I'm going to get a compilation error saying that catch are finally expected.
[02:43] Let me bring back my catch and finally blocks to resolve the compilation error.
[02:47] Now I can remove the catch block and with that there won't be any compilation errors because my try
[02:53] is having a finally block.
[02:55] The same is going to happen even if I try to delete these finally block.
[02:59] So the combination of try and catch is also valid. But please make sure you are always mentioning the
[03:05] finally block just after the catch block.
[03:07] You can't define an order like try finally catch that is not allowed.
[03:12] I can show you a demo as well.
[03:14] Let me copy this entire
[03:16] finally block and paste it just above the catch block.
[03:19] And in this scenario you can see we are getting a catch without try.
[03:23] So always make sure the catch block is getting immediately followed after the try block and if needed,
[03:29] you can define the finally block after the catch block.
[03:32] I hope you are clear.
[03:33] let me move back the finally block to the proper position which is just after the catch block.
[03:39] The last rule is regarding that try with resources.
[03:42] Whenever you are trying to define a try with resource statement, the catch and finally are completely
[03:48] optional.
[03:49] So please note that there is a difference between try and try with resources.
[03:54] So inside interviews, people can try to confuse you by asking questions like can I write a try block
[04:00] without any catch and finally blocks.
[04:03] In such scenarios you should confidently say if you are talking about try with resources, then definitely
[04:09] it is perfectly possible to define a try with resource statement without any catch
[04:14] and finally, but if you are talking only about the normal try block in such scenarios, it is not possible.
[04:20] So this is how you should answer to the interviewer.
[04:24] So you can see here I have defined a try with resources and it does not have any catch
[04:29] and finally, and this is perfectly allowed and from which version this is allowed.
[04:34] This is allowed only from the seventh version of Java.
[04:37] Let me show you that demo very quickly.
[04:39] You can see here I have a try with resource.
[04:41] I can delete this catch block and you can see we're not getting any compilation errors.
[04:46] I hope you are clear with all the rules and guidelines that we have discussed.
[04:50] Please have this slide handy whenever you are trying to attend a Java interview or whenever you have
[04:55] a confusion around try, catch and finally blocks.
[04:59] This slide should
[05:00] clear all your confusions.
[05:02] Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------

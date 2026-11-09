# 15.8 — Override hashCode() & equals() methods using IntelliJ

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] In the previous lecture, I showed you a lengthy approach to override a hashCode() and equals() method.
[00:07] But there is a very easy way to generate a hashCode() and equals() method with the help of intelliJ.
[00:14] That's why I'm saying a sorry here.
[00:15] The reason why I showed you the lengthy approach in the previous lecture is I want to teach you the
[00:21] concept.
[00:22] You should understand the concept first
[00:24] if I showed you the shortcut or the fastest approach, then I know you will not pay attention to the
[00:31] lengthy approach because you will be under the assumption I may not need it.
[00:36] I always take help from intelliJ.
[00:38] I don't want you to be under such impression, because understanding these concepts are very useful
[00:44] for your interviews or whenever in a scenario where you want to override these methods inside real projects.
[00:51] I hope you understand.
[00:52] Now let me show you the shortcut approach for the same here
[00:56] I'm going to delete the hashCode() and equals() method that we have written.
[01:00] Post that I'm going to simply right click and select the generate option.
[01:06] And there is a option to generate the equals() and hashCode() method.
[01:10] So let me select this.
[01:11] And your intelliJ is going to ask you which template to consider.
[01:15] So please make sure you are selecting the template which has java 7+.
[01:19] And after that you can click on this next button followed by
[01:23] you can select which instance variables of your object you want to consider in the business logic of
[01:30] hashCode() and the equals() method.
[01:32] Since we want to consider all these, for instance variables, make sure you are selecting all of them,
[01:38] and at last you can click on this next.
[01:40] And your intelliJ is also going to ask you one more time for the hashCode() method.
[01:44] Previously it asks for equals() method.
[01:46] Now it is asking for the hash code.
[01:48] Now if I click on this create, you will be able to see the same logic that we have written
[01:54] like under hashCode().
[01:55] It is trying to leverage Objects.hash() and similarly under the equals() we have first to handle all
[02:02] the edge cases or all the special scenarios.
[02:05] So here you're not seeing the curly braces because after the if block there is a single statement.
[02:10] That's why mentioning the curly braces after the if statement is optional.
[02:14] And apart from that, you can see all the remaining logic is same as what we have written in the previous
[02:20] lecture.
[02:21] So these are shortcut approach.
[02:22] You can see you can overwrite the equals() and hashCode() method based upon your own requirements within
[02:29] a second or two seconds.
[02:30] I hope you are clear and happy with the shortcut approach.
[02:34] Before I try to close this lecture, let me share a few other important details related to the rules
[02:40] and guidelines that you need to follow whenever you are trying to overwrite the equals() method.
[02:45] In the previous lectures, we have discussed that these are the four rules that we need to follow whenever
[02:50] we are trying to override the hashCode() method on the similar lines, we also have certain rules that
[02:55] we need to follow whenever we are trying to overwrite the equals() method.
[02:59] Before I try to share those rules and regulations, first let me confirm you that the code snippet that
[03:05] we have discussed around the demo of hashCode() and equals(), you can find it inside the slide.
[03:11] I have mentioned the code examples that we have discussed for your reference by having these code snippets
[03:16] inside this slide.
[03:17] Now moving on to the rules.
[03:19] Like you can see, these are the six rules that you need to follow while you are trying to overwrite
[03:24] the equals() method.
[03:26] The very first rule is you need to follow the symmetry rule.
[03:30] That means if you are trying to invoke the equals() method with the help of object A, by passing the
[03:37] object to be as an input.
[03:39] If this is giving as true, then the symmetry or the reverse invocation should also be true.
[03:44] Like if a.equals(b) is resulting as true, then b.equals(a) should also give the true as an output.
[03:53] The next rule is reflexivity.
[03:54] These rules conveys that you are trying to invoke the equals method by passing the same object as an
[04:01] input.
[04:01] Then in such scenarios, we should always get the output as true.
[04:05] So here I'm trying to invoke a.equals() and to the equals() method I'm trying to pass the same a object.
[04:11] So this is handled by the first if condition that we have inside the equals() method.
[04:17] And the third rule says transitivity.
[04:19] That means if a.equals(b) is true and b.equals(c) is true, then a.equals(c) should also be
[04:29] true.
[04:29] If there are three different objects with the name a, b, c are involved.
[04:34] If a.equals(b) is resulting into true and b.equals(c) is also resulting in true, then obviously
[04:42] you should also get the a.equals(c) also as true.
[04:46] And the fourth rule says consistency.
[04:48] That means the equals() method should always give the consistent results, even if you try to invoke it
[04:55] multiple times as long as the objects are not
[04:59] modified.
[05:00] And the fifth rule is we should make sure we are handling the null.
[05:03] It's common to check for null to avoid NullPointerException in the equals() method.
[05:08] So we have handled the null check as part of the second if condition, like you can see here this second
[05:15] if condition it has one of the check where it is going to check the null check.
[05:20] And the second object that we have received the same is being conveyed with these rule number five.
[05:26] And the rule number six is the equals() method has a strong relationship or tight coupling with the hashCode()
[05:32] method.
[05:32] So that's why whenever you are trying to override the equals() method, you should also make sure you
[05:38] are overriding the hashCode() method with the same object instance variables or the object parameters.
[05:44] And like we discussed in the previous lectures, whenever the a.equals(b) evaluates to true, then
[05:51] the hashCode() calculation of the a object and the b object should be same, but the reverse of it does
[05:57] not always result into true.
[05:59] That means if the hash code of two different objects is considered as true, then there will be no guarantee
[06:05] that two different objects they are going to be considered as equal.
[06:09] I hope you are clear with all the discussion that we have done around the hashCode() and equals() method.
[06:15] These methods are very complex to understand, but with all the efforts that we have put, I'm assuming
[06:21] now you are a proud Java developers who understand equals() and hashCode() method in a far better manner
[06:28] compared to other developers.
[06:29] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

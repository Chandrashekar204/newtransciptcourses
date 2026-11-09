# 17.7 — [JAVA 7] Diamond Operator in Java

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] As of now, whenever we are trying to create an collection object like ArrayList, we are trying to
[00:05] mention that data type of the elements that we are trying to store, both on the left hand side and
[00:11] the right hand side.
[00:12] So inside the angle brackets you can see on the left hand side, I have mentioned the integer the same
[00:17] I'm trying to repeat on the right hand side as well.
[00:20] IntelliJ is also throwing a warning to me on the right hand side
[00:23] you can see if I try to hover on this, I'll be able to get that
[00:27] details of the warning, which is explicit type argument integer can be replaced with empty angle brackets.
[00:35] This means since we are already mentioning the element data type on the left hand side, while we are
[00:40] trying to declare the variable, we don't have to repeat the same information again on the right hand
[00:46] side.
[00:47] Let me show you a demo around this.
[00:49] For the same, I'm going to create a new Java class with the name DiamondOperator.
[00:55] In few minutes it will be clear for you why I have given this class name as DiamondOperator.
[01:00] For now, let me try to create the main() method and inside the main() method I can try to copy all these
[01:07] declarations of array list inside these main() method
[01:11] let me paste the code.
[01:13] This time I'm going to remove the all the element data types that we have mentioned and the right hand
[01:19] side.
[01:19] But whenever we are using the var data type, we should not delete what we have on the right hand side
[01:25] because we didn't mention anything about the element data type on the left hand side.
[01:30] That's why whenever you are trying to use a var keyword to declare and create an any Collection object,
[01:36] in those scenarios, you should mention the element data type on the right hand side.
[01:41] And at last here I can remove these String on the right hand side because on the left hand side I already
[01:47] mentioned, if you closely look at these empty angle bracket, it is looking like a diamond.
[01:53] That's why this operator is called as diamond operator.
[01:57] So whenever you are trying to use this syntax to declare any Collection object, it can be an
[02:03] ArrayList or it can be LinkedList or it can be Set implementation or Map implementation. Inside collections
[02:09] whenever you're following this syntax we call this kind of syntax is diamond operator syntax.
[02:16] And this diamond operator is only introduced from Java7.
[02:20] Before Java7, it is mandatory to mention the element data type both on the left hand side and
[02:26] the right hand side.
[02:27] Inside programming language there is a principle which is DRY,
[02:31] DRY means Don't Repeat Yourself by following these principle.
[02:37] This diamond operator is introduced in Java7.
[02:41] Since we are already mentioning the element data type on the left hand side, there is no need to mention
[02:45] on the right hand side.
[02:47] My recommendation is always use this diamond operator and don't try to mention the element data type
[02:52] on the right hand side unnecessarily.
[02:54] Whatever we discussed around the diamond operator I have mentioned in this slide for your reference,
[02:59] please, please always use the diamond operator inside your code, and that is going to show that you
[03:05] are a mature user and you are trying to achieve your business logic by writing less amount of code.
[03:11] I hope this is clear.
[03:12] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

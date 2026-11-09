# 2.5 — Big O: O(n^2)

> Section 2: Big O

Now let's look at o of n squared. So I'm going to bring up our code from our last video here. This was a for loop followed by another for loop. To make this code O of n squared, all we have to do is make it where one for loop is inside of the other for loop. Like this. Now let's flip over to IntelliJ and take a look at this. So there is our method there with one for loop inside of another for loop. And I want to point out with this line of code here that it's important to have these quotes because it turns the whole thing into a string.

If you don't, it's going to take I and J and add them together as integers, and you're not going to get the output that you expect. So I'm going to run this. And then over here I'm going to scroll up to the top. Here we get zero zero and it goes all the way down at the bottom. Here it goes to nine nine. So now let's flip back. So these four loops ran n times n times or n squared. So we pass this a ten. And we had 100 lines that were output. And that is O of n squared.

So now let's take a look at this on the graph. So you can see compared to O of n, that O of n squared grows much faster. And that means from a time complexity perspective it is less efficient. So if you have a situation where your code is O of n squared, and there's a way of rewriting the code to make it O of n, that is a huge gain in efficiency. So that. Is O of n squared.

----------------------------------------

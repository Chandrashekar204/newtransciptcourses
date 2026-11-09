# 2.4 — Big O: Drop Constants

> Section 2: Big O

So in big O, we have a few ways that we can simplify things. And the first of those that we're going to look at is drop constants. So let's bring up the method that we had in the last video that looked like this with a single for loop. And with this we'll add a second for loop. And both for loops are going to run n times. And so to run this let's flip over to IntelliJ. So there is our new print items method there. And once again down here we're going to run this with the number ten.

And I'll run this now. And you can see here that this printed out zero through nine here. And then it printed out zero through nine again here. Okay. So let's flip back. So in this case we had n plus n operations. We passed this ten items and it ran 20 times which is two n. So you might think that this would be O of two n. But we simplify this by dropping the constant and it just becomes O of n. And it doesn't matter if the constant is 2 or 10 or a thousand.

We're going to remove it and just leave this with o of n. So our first rule of simplification. Is dropped. Constants.

----------------------------------------

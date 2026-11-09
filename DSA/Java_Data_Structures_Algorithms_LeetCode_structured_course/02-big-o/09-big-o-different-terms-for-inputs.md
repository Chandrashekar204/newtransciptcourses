# 2.9 — Big O: Different Terms for Inputs

> Section 2: Big O

So our next rule for big O is different terms for inputs. So what I'm going to do is walk through some code that we've seen before, and then we're going to make some changes to it. So the code that we saw before is when we have a for loop, and then we follow it with another for loop. And then we say each of the for loops runs in times. And we would say that's O of two n. Except we're going to drop the constant and it becomes o of n. So the change we're going to make to this is instead of passing this one argument, we're going to pass it two arguments.

And then we're going to say the first for loop is going to run a times. And the second for loop is going to run B times. And this is a very popular gotcha interview question. And the reason is because you see a for loop and you say okay that's O of n. Here is another for loop that is also O of n. And then we'll add them together and that becomes O of two n. And we drop the constant. And this is O of N, but that is not correct. If you think about this from an algebraic standpoint, you cannot say that A is equal to n, and b is also equal to n.

You would have to say that this is O of A, and this is O of B, and when you add them together, this becomes o of a plus b. And that is as far as you can simplify this. And the reason for that is if A was one and B was a billion, these would be two very different for loops. And you'd have to understand how each one works to understand the time complexity of the entire method. Likewise, if we took these two for loops and instead of having them one after the other, we had them one inside of the other.

This would become o of a. Times be. So we can't just say that each of the terms is in. We have to use different terms for inputs.

----------------------------------------

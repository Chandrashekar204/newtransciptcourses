# 9.2 — Stack: Parentheses Balanced

> Section 9: <> S&Q: Interview / LeetCode Exercises

So our next coding exercise is called parentheses balanced. So you will have a string that will contain nothing but parentheses. And these parentheses are balanced. There's an open parentheses and a closing parentheses. However these are not balanced. And you might say that there's an equal number of each. So why are these not balanced. And the reason for that is with parentheses we always start with an opening parentheses and then have a corresponding closing parentheses.

This string also has balanced parentheses. They're also balanced if we do it like this. Because we can have something in a set of parentheses inside of a set of parentheses. So now let's walk through how it is that we check if the parentheses are balanced. I'm going to bring up a stack and we're going to iterate through this string. And when we see an open parentheses we're going to add it to the stack. And then we go here and add this open parentheses to the stack.

And when we see a closing parentheses we pop one of these from the stack. And this is also a closing parenthesis. And we'll pop this from the stack. And now we've gotten to the end of the string. And because that stack is empty it means that the parentheses are balanced. So now let's look at another example. We'll put this back at the beginning and move these parentheses. So we'll start out by adding that open parentheses to the stack. And then we go to here.

And then we pop that from the stack. And then with this open parentheses we add that to the stack. And then with the closing parentheses we remove that from the stack. And we have gotten to the end of the string. And the stack is empty. And that means the parentheses are balanced. So now let's put this back and remove one of the closing parentheses and see how that works. We'll add this opening parentheses to the stack. And we'll do the same thing with this one.

And then when we move to here we pop this one from the stack. We are at the end of the string. The stack is not empty. And that means the parenthesis are not balanced. And we're going to return false. In the previous two situations where the stack was empty, we would return true that the parentheses are balanced, but in this situation it is false. So let's put this back at the beginning and look at what happens when we have too many closing parentheses.

We will add this to the stack. Move to here and pop this from the stack. But when we move to here we will have a check to see. Is that stack empty? If it is ever empty before we reach the end of the string, that means our parenthesis are not balanced. So in this case we return false and that is how we do parenthesis balanced.

----------------------------------------

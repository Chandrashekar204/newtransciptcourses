# 4.13 — Java's Logical OR Operator: Enhancing Conditional Statements for Flexible Code

> Section 4: Transitioning from JShell to IntelliJ IDEA: A Comprehensive IDE Guide

Kind: captions Language: en In the previous video, I talked about operators, including the logical and operator. In this video, I'll continue on with the discussion of operators and get into operator precedence. I'll be starting with the class, hello from the previous video. We finished off the last video by talking about the logical and operator, denoted by the two ampersands, and how it required both the left operand condition and the right operand condition to be true, in order for the code block to be executed.

Let's confirm that by running the code. You can see that the code in the code block wasn't executed because it didn't print out the greater than second top score and less than one hundred message. This is because we defined second top score to have a value of eighty-one, which caused the left operand condition to be false. All right, so a useful thing to do with these expressions or conditions is to use extra parentheses to clarify your meaning.

I'll put parentheses around the left operand condition, as well as the right operand condition: This makes the code easier to read, becase its clear now what the condition is for the left and right operands of the logical and operator. And if I run the code again. Nothing's changed, which is good, so adding the parentheses didn't change the outcome. We got exactly the same results. The idea of using them is to makes it quicker to understand the code at a glance.

This can be helpful in the future when you're looking over your code, or if someone else is reviewing your code, and you might have forgotten the reasoning for putting it there in the first place. So that's the logical and operator. Let's move on now and talk about typing two pipe symbols, which is known as the logical or operator. The logical or operator works in a similar way to the logical and operator. But the difference is that it only requires only one of the conditions to the left or right side of the logical or operator, to be true.

Remember that the logical and operator, or two ampersands, required both sides, both conditions, to evaluate to true. The and operator actually comes in two flavours in Java, as does the or operator. && is the logical and which operates on boolean operands; checking if a given condition is true or false. The & is a bitwise operator working at the bit level. This is an advanced concept that I won't get into here. Likewise || is the logical or, and again it operates on boolean operands; checking if a given condition is true or false.

The | is a bitwise operator which is also working at the bit level. And just like the bitwise and operator, we won't be using it as much as their logical counterparts. We'll almost always be using the logical operators. So let's put in some additional code here, on a new line, starting on line twenty-two. We want to test a new condition using the logical or operator, so I'll type: if, left parentheses, left parentheses, top score, greater than, ninety, closing parentheses, logical or operator, left parentheses, second top score, less than or equal to, ninety, right parentheses, right parentheses, left curly brace. I'll print a message if at least one of the conditions is true.

and finish with a right curly brace. All right, previously, I defined top score to be eighty. And looking at the code just written, the left condition is going to be false because eighty is not greater than ninety. I defined second top score to be eighty-one. And this is going to return true for the right condition because eighty-one is less than or equal to ninety. So, we have one false operand and one true operand. Therefore, we should still get the output because one of them is true.

And there it is, "either or both of the conditions are true". And just to confirm that, if we change second top score to ninety-five, an arbitrary number that's greater than 90: Run it again. And this time we don't get any output from that last if statement because both the left and right conditions return false. All right, so let's finish the video here. In the next video, I've got a mini challenge for you, which I think should be fun. And after that, we'll talk about the differences between the assignment and "equal to" operators, and how to ensure you don't get into difficulty with those.

I'll see you in the next video.

----------------------------------------

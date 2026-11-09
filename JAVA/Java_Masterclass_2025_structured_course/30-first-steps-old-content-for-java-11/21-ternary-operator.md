# 30.21 — Ternary Operator

> Section 30: First Steps - Old content for Java 11

All right so it's now time to talk about something called the Ternary Operator. So what I'm gonna do is come back here and undo the latest change that I had for isCar, so that we are testing to see whether it's true. But now what I wanna do is below that code, I'm going to type boolean wasCar equals I'm gonna type isCar, space, question mark, space, true, colon, false. So this is a case where we've got three operands. Now incidentally the Ternary Operator refers to the fact that the operator takes three operands.

So the first operand is the condition we're testing which should evaluate as all conditions to true or false. So the second operand is the value to assign to wasCar if the first condition was true and the third operand is what to assign to wasCar if the first operand condition was false. Now the first condition could be a lot more complex than what we currently have but if we add some code now and type if parenthesis wasCar add a code block and we'll put some output in the code block wasCar is true.

If you run this... ...you can see we've got the output This is true, but we haven't got the output for wasCar equals true and what's happened there is we are testing here, wasCar, basically what we're saying is isCar equal to true? If it is we wnat to set our wasCar variable to true otherwise set it to false so because on line 72 we've defined isCar as false therefore wasCar was assigned as false and we didn't see the output. If you come back and instead below that I'm going to type isCar equals true and now if you run the code again...

...this time we've got no difference of the code and that's because I put that in the wrong place obviously that should've been before the boolean because that point in the code, it tests the value and obviously by assigning isCar after the fact we didn't see any result but now if we do this we should see the wasCar output. And there it is - wasCar equals true. All right so the ternary operator - so confirming the ternary operator is a shortcut to assigning one of two values to a variable depending on a given condition.

So think about if the shortcut of the if-then-else statement, and of course we haven't discussed else at this point on the course but we will be discussing that later. So consider this example - int ageOfClient equals 20 boolean isEighteenOrOver equals ageOfClient equals equals 20 question mark true colon false. So operand one - ageOfClient is equal to 20, we're using the equals to operator, so that's the condition we're checking for and that condition, remember, needs to return true or false.

Operand two - true here is the value to assign to the variable isEighteenOrOver if the condition in operand one is true. And operand three, which is assigned to false, that's the value that's going to be assigned to the variable isEighteenOrOver if the condition in operand one was false. Now in this particular case isEighteenOrOver is assigned the value true and that's because the age of the client has the value 20 and our condition for operand one ageOfClient is equal to 20 returns true.

Now it can be a good idea to use parentheses like this example below to make the code more readable particularly in the ternary operator. So boolean isEighteenOrOver equals, we can just put in the condition for operand one equal to 20 in parentheses to make it clear. All right so let's end the video here. I want to talk a little bit more about operators and a bit of a summary and then we're going to get into a challenge and talk a bit about operator precedence and all of that's coming up in the next video.

----------------------------------------

# 8.11 — Is it Included?

> Section 8: More on Arrays & Iterables

There also is another useful method for finding out whether is part of an array or not and that's the includes method, though it's also most useful for primitive values because it also just checks values like index of does. So just wanted to throw this in here real quick, we could for example check if test results includes a value of let's say 10.99, which it does. This will then return true or false and therefore includes is a great choice if you're not interested in the index and also not interested in the value but just want to know whether it's part of the array or not. Though it's important to keep in mind that index of will return -1 if something wasn't found.

So this is essentially the same here as running index of and comparing that to not being equal to -1 because if that is not equal to -1, we know that it exists. If it is equal to -1, it does not exist but of course that's a bit shorter and say saves us this extra comparison so if you only are interested in knowing whether it's part or not, includes this nice to have for primitive values. So here if I reload, I see true twice because it is part of that array.

----------------------------------------

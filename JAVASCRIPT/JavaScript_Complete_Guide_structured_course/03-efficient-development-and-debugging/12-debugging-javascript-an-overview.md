# 3.12 — Debugging JavaScript - An Overview

> Section 3: Efficient Development & Debugging

So you know how to write your code and how to dive into external resources and find support, now you're writing code and you're having errors in there and that will happen. That doesn't make you a bad developer, that's just totally normal, you will always also encounter errors when writing code. Now we need to learn how to find and fix them and that there also are different kinds of errors. So when we think about debugging our code, there are different kinds of errors you can get, you got errors which basically show you some error message, where your app maybe crashed, where it doesn't work at all and you've got logical errors. Logical errors don't make your app crash, they also don't result in an error message but your app behaves incorrectly.

Now I will show you both kinds of errors in this module and show you how to find and fix both. Now if you're getting an error message, read and utilize it, seriously. So many people see an error message and they just go into panic mode and that's it, so many people don't even bother reading error messages even though many error messages are quite clear regarding what's wrong. So by just reading it and diving into the line of code which typically is included there, you can fix many errors. If you got an error message which you don't understand, you can Google it because guess what?

You're probably not the first person who got an error message, so put it into google and you'll find many solutions there. But sometimes that alone doesn't do the trick, sometimes you need to look into your code whilst it's executing to get a feeling for how values of variables change over time and where something might be going into a wrong direction. For that you can use console log which I already showed you, this is a built-in command which outputs information in this developer tools console.

It's invisible to the users of your page, unless they open the developer tools, then they can see it and that's important to keep in mind. Everyone can see what you output here not just you but it doesn't show up on the page itself and it allows you to log whatever you want, log whichever variable you want to log and this can be really useful for getting a first look into certain things or values of your code. You can also have multiple console log statements to see how things change throughout your program execution, so the kind of output, the flow of your application. But writing these console log statements can also be cumbersome, especially if you have a more complex error to fix.

You might need to throw a lot of console log statements into your code, change them, configure them correctly and that can be annoying over time, so therefore also leverage the debugging tools which are built into modern browsers, I recommend the Chrome debugging tools which are really amazing but Firefox also has debugging tools built in for example. Same for Edge and so on but in this course, I will go with Chrome and show you how to work with those.

Last but not least, your IDE can also help you with debugging and with fixing errors and we'll have a look at all these things now in the next lectures.

----------------------------------------

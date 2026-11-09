# 13.14 — The "Error" Object & Constructor Function

> Section 13: Back to the DOM & More Browser APIs

Now besides the date object, there's also one other built-in object which I want to show you because it can be important and that's the error object built into Javascript. You have to use new with it because that's a constructor function actually to create a new error. To this error object, to this error constructor function I should say, you can pass a string which will be your error message, something went wrong and when you created such an error object, you can throw it with the throw keyword.

Now you might recall that we saw this earlier in the course when we had a first look at error handling and at try catch. There I actually didn't throw this or such an error object, I threw a normal object which you can also do, you can throw anything as an error, you can throw an object, you can throw a string like an error and that will cause an error with that information but you might want to consider throwing an error object using this dedicated error constructor function.

When you do so, you don't just get your message which is automatically put into a message property of the created object, you also get a stack trace which basically tells you where this error was thrown, in this case in the console which is why we see anonymous here but if we would do this in a file, we would get the file name and the file numbers and so on. So besides just passing some error message, this can give you more information, also since it's an object, you can add stuff to it.

You can create your error object with new error here and put in your message, like something went wrong by passing it to the constructor but then of course, you can go to this object and you can add other properties as well. You see by default you got this message property and the stack property because this error constructor function creates an object which has these properties and that's of course nice to have, you also got a name here and you can change that of course if you want to but you can add anything else, like an error code if you wish to.

That's all possible and you can always console dir, not lohgbecause that will always just give you the error message but console dir that custom error to get a full view at the object which was created under the hood with my code property here, with the message property and the stack property. So that's the error constructor function, it creates an object, what you pass to the constructor function is automatically stored in the message, when you console log your error object, it will automatically give you that message, so console log will directly access to message property but if you console dir it, you get full access and you can always of course access all these properties with that dot notation as you can do it on any other object because it is like any other object basically, the only special thing about it is that you can throw it particularly well because it gives you extra error information, like the message or this stack trace.

So the error object can be really important for custom error handling.

----------------------------------------

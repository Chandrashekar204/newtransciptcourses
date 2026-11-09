# 9.22 — What the Browser (Sometimes) Does to "this"

> Section 9: More on Objects

Now one use case where this thing in front of your function execution will not really work is for example when you bind or set your function on an event listener. So the key thing really is that this refers to what called a function, the thing with what's in front of the function only works if you're executing the function on your own in your code. If you're setting it to an event listener like we're doing here with add movie handler, then we'll see something interesting, if I console log this in let's say the search movie handler which is also bound to an event, then what would you expect that this refers to here?

Well since there is nothing in front of it, it would be the global context right but that's wrong, again this what's in front of it thing only makes sense if you're executing a function on your own, so if you added parentheses or if you're using apply or call, here we're not doing that. We're indirectly executing this if you will by binding it to an event listener. So therefore we have to focus on the first definition I named, which is that this refers to who's responsible for calling this and here, that will actually be the event if you will, so the browser will trigger that event where we click on a button the browser then triggers the function, so the browser is kind of responsible for executing this but in the end it's this event which is responsible, right?

It's this click event which in the end is responsible for triggering this function and if we break it down even more it's the button that is responsible for executing this, right and that's actually how the browser configures this. When a function executes based on an event, then this inside of the function will actually refer to the object, to the element that's triggered that event which in the end triggered that function. However that's now also important, only if you're not using an arrow function because there is something special about arrow functions to which I'll come back in a second.

For now let's switch this to a normal anonymous function with the function keyword and then save this and let's have a look at this. If I reload and click on search, we indeed see the button is output there, so this inside of a function that's triggered based on an event listener refers to the element or to the thing that is responsible for triggering this event. Now I said for arrow functions that would be different though, so let's have a look at that now.

----------------------------------------

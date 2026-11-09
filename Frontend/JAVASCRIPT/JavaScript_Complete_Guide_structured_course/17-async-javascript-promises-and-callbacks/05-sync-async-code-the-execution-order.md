# 17.5 — Sync + Async Code - The Execution Order

> Section 17: Async JavaScript: Promises & Callbacks

Let's now dive a bit deeper into callbacks and async code and for this, I'll comment out this for loop, don't really need that here and instead let's say here where we have track user handler, instead of just logging clicked here, we want to get the user location. Now we can get this with the navigator object and then geolocation, this is a built-in API which allows us to reach out to the browser to get the user location with the help of getCurrentPosition.

Now getCurrentPosition is a method here which actually, if you have a look at its parameters, takes three potential parameters - a success callback, basically a function that is executed if the position was successfully fetched, an error callback which is executed if the position was not successfully fetched and then an options object where you can configure how that should be fetched and you can either set up some named functions and pass in the names here, like I'm doing it here for the event listener or you use anonymous functions.

So here for example, I'm using an anonymous arrow function where I get my position data and then I can console log posData, that's my success callback, as a second argument to getCurrentPosition I have my error and here I can console log that, this will be the error callback. Well and then if we wanted to, we could pass in a third argument, an object where we can configure that, for example set timeout, how long we want to wait for this to resolve until we throw an error and so on but I'll not do that and go with the default instead.

Now if we do that, what happens is if I reload and I click track me, here I am asked if I want to allow access, I click allow here in this case and now this will take some time to locate me and get that location and after a while, here it's done and we can expand this to now also see the coordinates if we want to and read them and do whatever we want to do with that in our app here. Quite convenient for many apps, let's say you're building a food delivery web service, then getting the user location might be useful.

Now here, we got these cases. Now to also simulate the error case here, let me reload, click this again and now I block this and now you see I get this error object and it's thrown or printed by app.js line 10 and this is simply the line here in this error callback. So this is how these callbacks work and just as with add event listener, getCurrentPosition offloads this task to the browser and when it's done, it pushes this into the event loop to execute our code there.

Now just as before, if we do something after calling getCurrentPosition, like outputting this to the log here, then this line will run before we print either of these lines, simply because we execute this code, push it to the browser and no matter how fast it finishes, Javascript moves on to the next line and the browser is then able to push this into the message queue so that the event loop moves to the call stack but the event loop will only do this once the call stack is empty.

So since this line is executed right away, even if we would get the position instantly, still this would print first because that goes into the event loop first, this code here inside of the callback functions can never be executed before this code because this is offloaded to the browser and the browser always has to take the way over this message queue and with the event loop to then go back into our current Javascript execution, something which is not the case for this line, this is executed immediately after handing this off to the browser.

So this line will always execute before one of these lines no matter how fast they actually are done, even if it would be done instantly, we would still execute this here first. This is how that works, so if I reload here, click track me, click block, still getting position was printed instantly because Javascript is non-blocking.

----------------------------------------

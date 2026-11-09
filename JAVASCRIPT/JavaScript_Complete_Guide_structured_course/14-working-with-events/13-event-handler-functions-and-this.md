# 14.13 — Event Handler Functions & "this"

> Section 14: Working with Events

Now to finish this up before we dive into our practice project here, one note about the this keyword. We already saw earlier in the course that inside of the event listener functions, this is actually bound to something else, to the event's source as I mentioned and therefore in the past, we had to use bind or arrow functions to make sure that this actually points at the right thing. Now let's quickly see this in action again, on this button here where I added an event listener, let's not just console log event but also console log this here and see what we get.

Now please note that here I'm using an arrow function though. So now if I reload and I click this click me button, you see I get the window object there because as I said, I'm using an arrow function and that ignores any bindings you might have assigned to this when this function gets called and here, the thing calling the function is the browser. The browser does bind this to something else though and to see this, let's convert this here into a regular function so to say, without the arrow but with the function keyword and still with the event object of course and let's see what this points at right now with a normal function being used here.

If we now reload this and click on that button, now you see this points at the button here, so in the end this points at the event target, to be precise as I can show you here on our list event listener here, if we console log this down there and transform this to a regular function as well and not an arrow function, so to be precise as you see if you click down there, it points at the current target, so not at the concrete target you clicked on but at the current target, so basically at the element on which you registered the event listener, that's what the this keyword refers to inside of a function you add as an event handler function, so you assign to an event listener if you don't override it yourselves by binding this function to something else and binding the this inside of that function to something else therefore or by using an arrow function as you saw, this is how you can kind of override or change this behavior, by default with a normal function.

This inside of a function which you assign to an event listener points at the current target of this event.

----------------------------------------

# 14.9 — Understanding "Capturing" & "Bubbling" Phases

> Section 14: Working with Events

So prevent default is a very important method on the event object which you can use to control what the browser does with that event. We also got another important method for which we first of all need to understand how exactly the event behaves. Our events in Javascript, in browser side Javascript have two phases through which they run essentially and where they then trigger your event listeners, a bubbling and a capturing phase. Let's say we have a button in a div which is in a section, this could be the markup we have.

Now we click that button here, now what actually happens is that the browser runs through two phases where it checks for listeners to that event. First, it runs through a phase which is called the capturing phase, second it runs through a phase which is called the bubbling phase. Now the capturing phase goes from outside to inside, now what does this mean? It's important to understand that a click event on such a nested button here cannot just be listened to with event listeners on the button but for example also with an event listener on that section and the browser during the capturing phase checks if you got a capturing event listener on let's say the section registered which would then actually run its function before any event listeners registered on the button because it's from outside to inside in the capturing phase and the section is outside of the button.

The bubbling phase on the other hand does the opposite, it goes from inside to outside. Now all event listeners you add with add event listener are by default registered in that bubbling phase which means if we have an event listener on the button and on the section, the button event listener will run first, the section event listener will run second. We can change this and we can also do interesting things with that bubbling and capturing behavior as I will show you in the next lectures.

----------------------------------------

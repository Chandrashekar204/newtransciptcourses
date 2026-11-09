# 35.45 — Dispatching Custom Events

> Section 35: Bonus: Web Components

So now that we can close and open our modal, let's dispatch our own events. Now how do we do that? Well for that, let me first of all accept, on the canceled event, the event object. We get this automatically, we get this automatically because we used this click event listener here and Javascript just works in a way that the method which gets triggered for this event automatically receives an object with some metadata about the event that was created by Javascript, so about that built-in event.

Now we don't need that event to dispatch our own once, we will not copy it or anything like that but on this event with event target, I get access to the target that is responsible for this event, so in my case the button and this button, just like every other HTML element, is capable of dispatching a new event with the dispatch event method. The dispatch event method takes a new event, so a totally new event, not this event we receive here, a new event as an argument.

So here I'll name this cancel event, the name is totally up to you and I create it with the new keyword which we use in Javascript to create new objects based on constructor functions or classes and I'll use the built-in event object, so this is built into Javascript, just as the HTML element is. So now I can create a new event here and we give this event our own name by passing it in the constructor here, between quotation marks, so as a string and here I'll name this cancel and this is exactly the name to which we will be able to listen to from outside later.

So here, I am listening to the cancel event in my index.html file and this should work later because I'm dispatching an event named cancel here. So now I pass this cancel event to my dispatch event function and with that, let's see if that works, let's go back and reload here, click that and click cancel and we don't see canceled here in the console, even though we should be logging that here when we listen to the cancel event. So somehow our own event doesn't really seem to be dispatched on our component and indeed it isn't and it is dispatched on the button because, and that is the only reason why I accepted the event argument here, we're dispatching it on the event target of the cancel event or of the cancel event handler I should say and that event handler is used on the click event of the cancel button.

So the event target of that event is the cancel button, so we're using that HTML element to dispatch the event here and therefore the only place where we can listen to that is that button. So if I would add an event listener here and I would listen for the cancel event here and there I just use an anonymous arrow function to quickly output cancel inside the component, then we should see that log once we click the cancel button because now we're listening to the same element where we dispatch this and indeed, here we see cancel inside the component.

So the good thing is dispatching our customer event works, the bad thing is it is only available on our button, it doesn't leave our component and that is not ideal. Let's work on that and I'll comment this out here, let's work on this in the next lecture.

----------------------------------------

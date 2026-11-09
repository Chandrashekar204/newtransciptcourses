# 35.26 — Conditional Host Styling

> Section 35: Bonus: Web Components

Now let's take what we learned in the last lectures one step further. What if we want to apply a default style from inside our component but only if some condition is true on our custom element? Let me give you an example. Let's say on this first tooltip here, we added a class, we might have done this right from the start when we wrote our HTML document or maybe we did this programmatically when our app runs, a user clicks a button and we add a class to this element, as we can do it with any HTML element.

The class here is maybe important, the name does not matter, let's say we added the important CSS class to our custom element. Now we only want to set a background color on our custom element if that important class was set. Now what you can't do is you can't say :host.important, this might be something you would think that works because that is how you'd normally combine multiple selectors together in one rule if they all have to match simultaneously but here if we reload, this actually has no effect as you can see, on our custom element, we now don't have any styling from inside our web component.

So this does not work, instead :host is also used as a function if you have some condition for it. So you then simply wrap your condition, so the other CSS selectors that should be matching on your host element, so on your custom tag and you add all these required selectors, the required conditions in parentheses here and you can have anything in there, you can have an attribute selector in there, a class selector as we have it here, an ID selector, any kind of combinations.

Now with this syntax, with host with the condition of also having the important class, now with that, we get back this gray-ish background but only on the first web component here, not on our second one because we now require the presence of this important class and this is simply not the case on this second component. On the first one, it is and in this style inspector here, we indeed see this is responsible for setting this gray background and this is our host rule with the condition of also having the important CSS class on our custom element.

So that is another, very important variant of host that allows us to style things with way more flexibility.

----------------------------------------

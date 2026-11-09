# 13.5 — The DOM & Prototypes

> Section 13: Back to the DOM & More Browser APIs

Now before we continue working with width and height, one short extra lecture regarding MDN and the element docs we find there and the HTML element docs we find there. Now that we understand how inheritance and prototypes works, this picture here actually also makes more sense or should make more sense. Javascript or this DOM API exposed by the browser in Javascript I should say simply alsi works with multiple constructor functions, with multiple classes if you want to call it like this and this is how they are related.

The way you should read this is that every HTML element is inheriting basically from element, so has an element prototype, any element prototype has a node prototype and that in turn has an event target prototype and that makes sense because if you remember earlier, I explained that elements are just specific type of nodes, so it makes sense that they have a node prototype but then they bring their own properties and methods as well and you even have more specific types than just HTML element because you have specific types of HTML elements.

If you scroll down a bit further on this HTML element article, you find the more specialised versions and there are a bunch of them as you can see, for example there is the HTML input element. The specific thing here is that it has all the properties or it has access to all the properties and methods of HTML element, of element, of node and of event target but it also adds its own special properties and methods to which only an input element has access.

Here for example, the labels property, a property other HTML elements don't have access to but HTML input elements have access to it. Now how do you create such a HTML input element? Well you don't have to create these objects or these instances, instead when you select a HTML input element from the DOM, you will automatically get such an object of that type With all these properties and all these methods and thanks to how prototypes and the prototype chain works, we then also have access to everything from HTML element, from element, from node and from event target.

So this hopefully now also makes a bit more sense now that we had a look at object oriented programming and at prototypes in earlier modules.

----------------------------------------

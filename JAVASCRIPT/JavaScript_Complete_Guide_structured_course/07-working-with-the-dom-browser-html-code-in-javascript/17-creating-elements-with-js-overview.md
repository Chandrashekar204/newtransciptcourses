# 7.17 — Creating Elements with JS - Overview

> Section 7: Working with the DOM (Browser HTML Code) in JavaScript

So now we have an understanding of how you select elements with different selection methods, most importantly get element by ID and query selector, we have an understanding of how you traverse the DOM based on an element which you selected with parent node and so on, we have an understanding of how you can read values from a DOM element and how you can manipulate DOM nodes or DOM elements, now let's have a look at how you can create and insert brand new elements because that's something we haven't really covered thus far.

Now for that, we have basically two different ways of doing that - we can and that might sound surprising but we can write some HTML code in Javascript and tell Javascript and therefore the browser that it should take and parse this HTML code and render it in a certain place of our documentary in the end or we use the create element method on the document object to create a brand new node and manually then insert it somewhere in our document. Now the HTML string can be added with the innerHTML property which you find on element nodes and that indeed adds and renders an HTML string, so some HTML code in that place where you add it.

Alternatively, you also have insert adjacent HTML, a method you can use if you want to add some rendered HTML content next to existing content instead of replacing that content with it, so that's also supported or as I said, use create element to create single DOM element nodes instead of a bunch of HTML at once. Such created elements or element nodes can be added with append child or append and I'll come back to the difference throughout the next lectures, so this appends such a new DOM element or node inside of another, the new parent element or node then. You also have prepend, before, after, insert before and so on to be more specific where you want to add it, instead of adding it at the end of the existing child node list, you can add it in front of it and so on, so that can help you be more specific about the position where it should be added and you can also replace an existing node with that, with replace child or replace with, that's also possible and allows you to basically remove an existing element and replace it with a new one.

So these are different ways of manipulating the document, let's now have a look at them and understand their differences and when to use which.

----------------------------------------

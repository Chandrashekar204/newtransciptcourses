# 7.23 — Removing Elements

> Section 7: Working with the DOM (Browser HTML Code) in JavaScript

Now being able to add elements is of course nice, sometimes you also want to remove them. Now with replace with, we are able to remove them but of course only to replace an element with a brand new one. To just get rid of it, we of course also have ways. Now for that, I reloaded this document and here, let's say we want to get rid of that entire list. So I'll again select it with document query selector ul, ul as a string and now to get rid of it, there are two ways.

One is to use list.remove and this will just do what it sounds like, it removes the list from the DOM, so from the rendered page. Now good old MDN, if we check the remove method there shows us however that Internet Explorer again is not too fond of this method so if you want to ensure that this works there as well, you can't really use remove there. All other browsers have great support so you can definitely use it there but if you need to support this like this in Internet Explorer, then another way of making this work is to select the item you want to delete and then you reach out to the parent element, so the element node above the item you want to delete and there you have a remove child method and to that, you pass the item which you want to delete, list in this case and it will also work. Remove child is supported in all browsers, just like append child and therefore, this is the safest way of removing an element, reaching out to its parent and then remove child and then passing the item you want to remove but again, remove also has pretty good support.

If Internet Explorer support doesn't matter for you, then just remove on the item you want to remove just like this is of course the shorter and the recommended way.

----------------------------------------

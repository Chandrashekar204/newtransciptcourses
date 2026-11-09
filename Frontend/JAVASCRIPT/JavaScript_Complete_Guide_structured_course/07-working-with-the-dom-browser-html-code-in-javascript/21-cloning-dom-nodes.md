# 7.21 — Cloning DOM Nodes

> Section 7: Working with the DOM (Browser HTML Code) in JavaScript

So you learned that inserting an element more than once will move it and not copy it, if you would want to copy an element, well then you can do this with another method which is available on every DOM node object, so let's say on our new li with clone node this will clone this node and will really return a brand new one. It takes one optional argument and that's a boolean which can be true or false which by default is false, which simply determines whether a deep clone, so with all child and descendant elements should be done or not.

If you pass false here, which is the default, then only the list item itself is cloned but no nested elements you might have in there. If you pass true here, then not only the direct child element but also all child elements of that element and all descendants in general will be part of the clone. So now if we do that and we have newLi2 where I store this clone, now I can of course go ahead to my list and let's say append new li and newLi2 and the result of that is of course that item 4 is moved to the end because I appended new li which already was part but I also appended the brand new li 2 which is why I have another item 4 here added to the end.

So this is how you can also copy elements if you need to instead of recreating and reconfiguring it, this might simply save you some time if you want to take most of the settings of an existing element or all of the settings and then just insert this brand new element into your DOM as well.

----------------------------------------

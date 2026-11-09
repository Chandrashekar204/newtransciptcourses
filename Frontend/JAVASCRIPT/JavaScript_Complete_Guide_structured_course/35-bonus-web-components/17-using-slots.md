# 35.17 — Using Slots

> Section 35: Bonus: Web Components

Let's start with our lost text. It's easy to bring back because the template solution here has a tool for us to enable us to pass some content between our opening and closing tags of the web component and this feature is called slots. We can define a slot in the template which basically means hey you can insert the content which is between the opening and closing tag of our element in that place. You do that by simply adding a slot element, opening and closing, nothing in between, like this inside our our template. If you do that with just that addition, if you now reload the page, you'll see our text is back and now the question mark is correctly added after it because essentially, it's now taking this as a template and this template says here is the place for whatever you pass between the opening and closing tag and thereafter we have our own DOM, our own template whenever we want to have.

So this works now as before but now we're taking advantage of that slotting mechanism. Now slots also can have a default value, some default and this will kick in if you don't pass anything between the opening and closing tags. So if I delete my text down there for the second usage of this custom component and I then go back to the page and reload, we see some default here because the text I passed between my slots tags then is used as a default unless we override it with our own text as we do up there.

----------------------------------------

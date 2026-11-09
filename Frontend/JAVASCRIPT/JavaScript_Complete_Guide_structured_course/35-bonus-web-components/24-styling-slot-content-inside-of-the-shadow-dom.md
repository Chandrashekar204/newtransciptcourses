# 35.24 — Styling "slot" Content Inside of the Shadow DOM

> Section 35: Bonus: Web Components

Well if you want to style slotted content, there is a special selector you can use inside your web component, so inside your shadow DOM styling and that is a special pseudo selector, ::slotted. This will select all slotted content and the way it works is that you call this like a function here is CSS and to it, you pass the selector of the slotted content, so now you could say I want to select all slotted content that has the highlight class or all slotted content that is a span or an anchor tag, so anything like that.

Important though, you can only select the slotted content itself, so if for example in my slotted content here in this span, I also had an anchor tag in there, then what you could not do, you could not select slotted and then the span, this would still work because the slotted content is the span but you can select a child element in the top level slotted content. So this would not style the anchor tag in your slotted span because you can only select the topmost element for styling, this is an important restriction you have here.

So if you have nested content, you can't select this but you can select a span or since this is also directly on the slotted content in our case here, the highlight class and then here, what we could do is we could give us a border bottom of one pixel dotted and red for example, save that and go back and reload this page and you will see this slight red border here and if I inspect this again, you see here is our styling getting applied, the border bottom is having an effect here.

Still important to highlight the order of the styles here, the styling you set up in the light DOM will override your slotted styling you set up in the shadow DOM and the idea here simply is that you always want to give the user the final say on how things should look like but you can set up some default styling you want to have as we do it here but if we were to set a border bottom in the light DOM too, so in our case for the highlight class, if I had a border bottom of let's say two pixels solid and blue here, then you would see that if we reload this page, we see that border instead of our red dotted border because whilst this rule still gets applied, it gets overriden here.

So the specificity in CSS is such that light DOM styling overrides shadow DOM styling for projected or slotted content. This is just one thing to be aware of, I will comment this out here in the light DOM because I don't want to override this, I want to have my red dotted border but it is something you definitely have to be aware of, this can be overriden from inside the light DOM.

----------------------------------------

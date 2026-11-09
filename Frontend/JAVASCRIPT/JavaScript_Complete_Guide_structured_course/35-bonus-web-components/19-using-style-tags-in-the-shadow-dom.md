# 35.19 — Using Style Tags in the Shadow DOM

> Section 35: Bonus: Web Components

Now with our own template being defined here, we can now also define some styles here and by the way this would have been possible with the template in the HTML file too because in here, we can now of course also add style tags as we can do in any Javascript file as we can do in normal HTML too, and the styles here and that is the interesting thing, since we do that on innerHTML of the shadow root, the styles here will only apply to the HTML code in our template, so to this span here or to the div we add dynamically and this means that we can now add all these styles down there in our style tag here.

So I add a div selector and now I want to set the background color with normal CSS because this is now a normal CSS written in a string, so the background color is black let's say, the color, so the text color is white, the position is absolute, the z-index is 10 and now I can't go down there and remove all these manual style assignments and still if we save that and we reload, we have the same styling as before but now we can write all styles conveniently as you are used to in HTML or in CSS syntax and it is scoped to this component only.

Please note that I'm using a general div selector and yet if I go to index.html and I would add a div here, this does not get the web component styles because of the shadow DOM. So if I now reload, you see the orange border which makes sense because we set this up here but you don't see the black background, this does also not have the absolute position because we really have scoped styles, thanks to the shadow DOM and our styles being set up as the innerHTML of that shadow DOM for our custom web component.

And this gives you a lot of flexibility regarding how you style your components, regarding the template you set up for them, regarding the elements you add to them and all of them is part of your custom element and does not spill over to your normal DOM.

----------------------------------------

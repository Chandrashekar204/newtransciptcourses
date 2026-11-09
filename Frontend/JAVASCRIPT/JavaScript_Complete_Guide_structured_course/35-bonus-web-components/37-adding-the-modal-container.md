# 35.37 — Adding the Modal Container

> Section 35: Bonus: Web Components

So with the backdrop added, let's work on modal, so #modal selects the element with the ID modal and just to reiterate on that, because we're in the shadow DOM, this only affects elements with the ID modal that are inside of our template here, so basically only this element here and for the modal, I want to have that in the foreground, so I'll actually give my backdrop a z-index of let's say 10 and modal will have a z-index of 100 because it should have a higher z-index so that the backdrop is in the background of the modal.

I'll also give a position of fixed, to position it in a fixed way in our viewport in our document, from the top let's say we have a distance of 15vh and from the left we have a distance of let's say 25% and then we have a width of 50% because we have 25 distance from the left, then a width of 50% and then also 25% from the right which is the leftover space, therefore this should be nicely centered and you can set different styles, optimize this for mobile, I'm not caring so much about the styling here, I just want to focus on the general functionality and not write a ton of styles.

You could add media queries in here, whatever you need for the right styling. I'll go with this styling and I'll give it a background of white and to ensure that we can see something for now, I'll give it a height of let's say 30rem and we might be able to get rid of this later once we have some content in there. I also want to have a border radius of let's say 3 pixels and I'll give it a box shadow of 0, 2 pixels 8 pixels and then let's say this style here, some transparent box shadow drop shadow and with all of that in place, let's head over and reload this page and here's our modal and obviously, this is missing all the content but we're getting there.

Now we have the modal container, we have the backdrop behind it, now we want to populate that modal with some content of course and I want to have some static content in there and I also want to have some slotted content in there. So let's add that next.

----------------------------------------

# 3.16 — Adding Dimensions

> Section 3: CSS Fundamentals

-: So now let me just very quickly show you how we can add dimensions to elements in CSS using the height and the width property. And let's once again start with our side element down here, which at some point later will be our side bar. And so it shouldn't be as white. And instead we only want it to be 500 pixels wide. So, we can simply come here to our element and specify the width as 500 pixels and just like that, now our a side element is only 500 pixels wide so a lot more narrow than the rest of the page.

Okay? So very easy, very straightforward. That is the width property. Let's try another one. So, actually, let's try height now. And I'm doing that here in the main header. So here, let's set the height to, let's say, 80 pixels. All right. And now you saw how it increased here. Right? Now, let's actually inspect this header here. So not the link, but the entire header element, right? And if we check out the box model down here So, this is all a bit small, but never mind.

So you can see that here we actually have the 80 pixels that we just specified, right? And then on top of that, we have the 20 pixels to the top and to the bottom. And so the complete final size of the element is actually not the 80 pixels that we specified here, but it is 80 plus 20, plus 20, which is 120 pixels. So that is exactly that default behavior of the box model that I mentioned before. And that, in my opinion, doesn't make any sense at all.

But again, we will fix that a little bit later. For now, it is important to learn how the box model actually works originally. And so again, the real height of this element is not the 80 that we specified here, but we would then have to add the padding to the top and bottom. Okay? Now, one thing that you also might have noticed here is that the content, so the text here, doesn't just magically get vertically centered inside of this header element.

So it actually was vertically centered before. But that was simply because we had applied the same padding to both of the sides. But now, not anymore. I mean, we still do have the same padding on both sides. But now we have this other high tier. And so now the space that's at the bottom is no longer the space that's at the top, that actually, it's not really straightforward to center this vertically, but of course we will learn how a little bit later.

Okay, so let's close it. And now, let's actually finally talk about this image. So up until this point, it has been sitting here untouched, but now let's select it, and let's actually size it. And for that, let's give it a class, so that we can then select it. So it is this one here. So, class of post image, let's say. Copy it. And then, well, let's say somewhere here at the very bottom, actually. So this year was just a demo, so I'm putting it here.

And now let's specify the width here. So it is actually very common to size images in CSS and not in HTML like we did. Actually, many times we never even specified the width of images in HTML, but only in CSS. Now here, for the first time, I will not use a length in pixels. I mean, I could, for now, let's say 800 pixels. And so, well, that looks like it actually was the wrong image that we selected here. So the class should be of course, on this one.

And so now that looks correct. And so that 800 that we specified there did now override this 500. However, this 200 tier is still in place, and that's why the aspect ratio is now like completely broken. Right? So this doesn't look correct anymore. It's way stretched to width. And so, in order to fix that, in case we do have the height specified in HTML, what we need to do is to then set the height to auto. And so, that will then fix it and will put the aspect ratio back to the original. Okay?

But again, specifying the height and setting it to auto is only necessary if that height is already specified before in HTML. In case we don't do that. So in case we don't specify any image dimensions in HTML, then if we set the height or the width using CSS, the other one will automatically adapt in order to account for the original aspect ratio of the image. So, for example, if we set this to 300, then it would become really small, right? But now, as I said, let's actually move away from pixels for the first time and use percentages.

So, I can say the width like this. So, 100%. And usually for a width measurement like this, the percentage is usually the percentage of the width of the parent container. So the parent of the post image is the header and this header is basically the entire width of the page, right? And so, if I say width of 100%, then this image should not be the width of the entire page. And indeed, that is exactly what we get. And so, what's special about this is that now, as we change the size of the window, then the size of the image will always stay at 100%.

Okay? Because that is always the size of the parent container. Of course, we could set it to something else, like half of the size of the parent container. And what would still happen is that as we changed the size of the parent container, then the size of the image would also adapt. Okay? And this is something that will become very very important once we start talking about building responsive websites. So, websites that adapt to the screen width, okay?

But let's put it back to 100%, which is what we originally wanted. And with that, I think we are actually done with setting some heights and some width, at least for now.

----------------------------------------

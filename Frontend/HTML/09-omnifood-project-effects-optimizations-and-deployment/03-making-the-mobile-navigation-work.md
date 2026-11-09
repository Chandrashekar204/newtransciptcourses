# 9.3 — Making the Mobile Navigation Work

> Section 9: Omnifood Project – Effects, Optimizations and Deployment

Instructor: Now it's time to finally make the mobile navigation work. And let's start by remembering how the mobile navigation actually works. So, this one we don't need for now. So it's here at the queries now, right? Let's actually open this here on another side. And the same with the script, removing some space there. And now down here, I think it was in this media query where we have the mobile navigation. And so that mobile navigation is displayed whenever the header has this nav open class.

Remember that? So let me copy this. And then here we need to go back to our responsive view, basically. So double clicking on inspect, and now the header. So, I'm gonna paste now this class name, hit enter and then there is our navigation. And then when we want to close the navigation we want to remove the class. All right? And so now we will use JavaScript to basically do this automatically whenever this button here is clicked. All right? And that's actually not that hard.

So let's add some comment here. So set current year and make mobile navigation work. We already paste that here so that I can now copy paste this comment just to give this file some easier to understand structure. Okay? And so just like before, let's start by selecting the elements that are relevant here. So in our html, let's move up here. So 2D navigation. So right here. So, when do we want a certain action to happen? So in this case, adding this class here.

So we always need to start by thinking about that. So where we actually need to click in order for something to happen. And in this case, that is this button right here, right? So let's grab this class name here and then select that. And again, creating a new variable for that. So let's call it button for navigation. And then document.queryselector. And then again, our selector between these quotes. And it doesn't matter if single quotes or double quotes, so the dot as always.

And yeah, so that is our button here. And the lines always need to end here with the semicolon but they haven't been writing that because Prettier which is the extension that formats our HTML code and or CSS, does also format JavaScript, right? So this is one of our HTML elements that is relevant. And the second one is the header, right? Because that is where we will want to add this class. And so, let's go select that one as well. So this one has the class of header.

So header, let's again actually call this EL and this one as well, just to follow that same convention. So document.queryselector and then with the header class. Okay, and now we do just as we did before right here using this function called add event listener. So we want to listen for the click event now on this button, right? So btnNavEL.add event listener, and then click. And there are of course other events than clicking, for example, hovering or typing some key on the keyboard or something like that.

Okay? And then the second part here of this add event listener function is that we pass in our own function. And so remember that here now goes the code that we actually want to execute whenever this click event happens on the button. So what is that action that we want to take? Well, we basically want to add this class here to the header when it is not there. But if it is already there, then we want to remove that. And in JavaScript we can do that very easily with just one line of code.

So we take our header and then since we want to work with classes there is something called the class list property. So class list, then dot again. And here from the VS code suggestions you can see that we can use this one here to add classes. We can use this one here to remove classes. But what we want to do actually is toggle which is kind of adding and removing all at the same time. So toggle. And here now we're going to use that nav open class.

And that's it. That's actually all we need. So what toggle will do is it will look at this element here and if it does have this nav open class it will then not add it. So if it's already there, it will remove it. But if it's not there, then it will edit. Okay? And here I make sure to really just write the name of the class, but without the dot. So not like this, but really just the name of the class. Okay? And that's actually it. So let's check that and clicking here.

And indeed you see that now here is nav open. Beautiful. Now I'm just seeing that the focus effect is here behind so we need to fix that a little bit. But the functionality here is already working. So beautiful really, really nice with just a couple of lines of JavaScript. We just made this happen. So we can click here as many times as we want and it will always just work. But now what I was mentioning about the focus date is that maybe you can very faintly see it here.

So that orange border here in the background. And so the problem here is that we need to actually make sure that this button here is always on top of this navigation right here. So of this element with the white background. So let's do that and remember that exactly for that purpose, we have the Z index property. So let's see where that is, right here. So let's just set some very high value here. Z index, let's say 1000. So it doesn't really matter here.

Sometimes we even use something like this just to show that we want to really use some really really high value here. So let's, well, let's actually keep that here. So that's kind of a convention that many people do and yeah, and so there's no problem of us also using that. But anyway, now you see that the focus date always stays on top which means that this button here is now in fact also on top of all of this here. Now okay, and just like this, we made it work.

And so mission accomplished.

----------------------------------------

# 3.5 — Combining Selectors

> Section 3: CSS Fundamentals

Lecturer: Let's now make the CSS code that we just wrote a little bit better by combining some of the selectors. So you might have noticed that we applied the exact same font-family to all of our elements here, right? So all these six CSS rules that we have here, all of them have font-style or actually have font-family set to sans-serif, right? And you see that VS Code actually highlights these occurrences here in all of the rules. So doing that is a little bit repetitive, right?

And it's also not a good practice. Because let's say that all of a sudden, we wanted to change the font-family to something else, then we would have to go through all of these different rules and set the font-family then to something else there. So instead, what we can do is to create a list of selectors in order to select multiple elements and then apply this font-family to that list, essentially. So let me show you how we can do that and let's do it first here actually.

So what we want to do is to select the h1 element and the h2 element and the h3 element. And so as you see, the way we write that is by using these commas, okay? So again, here we are going to select the h1 elements and the h2 elements and the h3 elements and the h4 elements and the Ps and also all the LI elements. Okay. And now we can grab this text here and cut it and paste it here. And now we can remove it from all of these other selectors. All right.

And if I give it a save now, the page should basically look exactly the same. And it does. Okay. Now prettier formatted our CSS code here like this. So having one element for each line. And so this is a bit easier to read. And so now if we wanted to change the font-family, let's say, to serif, which is actually the default, so if I save this now, then you see that all of the elements changed at once, right? So all of them now have the serif text.

Then of course, if we set it back here, then all of them will change, right? So now have serif text everywhere. Well, actually, except for in the footer. So that's something that we need to fix. And to make it easier here, let's actually simply wrap this text here inside a paragraph. So let's come here to our HTML. So this is really important that you do this. And so create a new element here and it automatically closed it. So let's just then grab this text and paste it here.

And you see that now this paragraph looks just like all the others, okay? So don't skip this step, please do this because we will now need it for another example. And in fact, let's look at that example right away. So the size of our paragraphs is 22 pixels. And so of course, now the paragraph that's in the footer, so this one is also 22 pixels. However, the text that's in the footer is usually a lot smaller than the rest of the text because this is just some secondary information that is not really important.

And so therefore, we should actually make this text in this paragraph here smaller than the text in the other paragraphs. And one way in which we can do this is to combine selectors in another way. So just to recap. Here we combined these six selectors into one list. So we say that the selector here is now a list selector. So this here is still one selector but it is a list selector, okay? So this is one way of combining selectors. But now I will give you another way of combining selectors, and the goal of that is, as we just discussed, to decrease the font-size in here.

So we will now use the so-called descendant selector, which is to write something like this. So we select the footer element, then a space, and then the p selector. And so what this will do is it will select all the p elements that are inside of footer elements. And so that's why this is called the descendant selector, because the p element is a child element of the footer in our HTML, and so therefore, this selector here will then select all of these paragraphs that are children of footer elements.

And so if we now set the font-size here to something smaller, let's say 16 pixels, then you see that all the other Ps, they are still normal. But in fact, this paragraph that is inside the footer is now only 16-pixels small. And hopefully, you can see how useful the descendant selector like this here is. So actually use this all the time. However, in this case, this actually isn't very robust, because like this, the selector basically reflects the HTML structure, which can lead to problems.

And to show that to you, let's write another descendant selector. So in this case, let's say that we want to select this paragraph here that's inside of the header. So remember that we have a header here in the article. So this one here. And we have a p. So let's say we wanted to style that italic, so make the text italic. And so using what we just learned, we could say header and then the p that is inside there and then say font-style and set it to italic.

Okay. So this worked just fine. But now imagine that for some reason, we also added a paragraph to this header element that is up here in the page. So let's try that. And remember that here we have another header, right? So as I was just saying, let's add a p here, Test paragraph. And you see that this one is now also italic. However, what we wanted was only this paragraph here to be italic and not this one, right? So we need to solve this somehow.

And actually we can solve it. It is not too hard. Well, at least in this case, because this header here is inside of the article and this one is not, right? And so we can actually create a nested descendant selector. So we can have a descendant inside a descendant. So what I mean is basically writing this. So we only want the paragraphs that are inside of headers which are inside of articles to be italic. So let's give it a save. And now only this one is italic and this one here not anymore.

So this actually works, but we are now even more encoding the HTML structure into our CSS selectors. And that can make our code hard to maintain in the future if we ever change our HTML. And so that's not a good idea. So if we think about this, wouldn't it actually be a lot better if we had a way to basically give some elements names and then use these names to select them? Well, we actually can do that, and it is exactly the subject of the next lecture.

So let's go there right now.

----------------------------------------

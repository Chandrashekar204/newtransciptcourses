# 18.11 — Triggering Requests via the UI

> Section 18: Working with Http Requests

So sending requests generally works, now let's link it to our UI because that's a bit more realistic and for that we also need access to the form and to that fetch post button. The form here is in the section with the ID new post and the button for fetching posts is in the available posts section. So we can use that to select our elements form by using document query selector and then that would be, what did I say? New post is the ID and then there, the form element and the fetch button, that would be document query selector and then there, we have the section with the ID available posts and there it's the first button which we find.

So here, ID available posts and then the first button. Now we have access to these two elements, now for fetching, we can scroll down here and we can reach out to our fetch button and add an event listener here where upon a click, I'll use an anonymous function, doesn't matter if it's an arrow function or a created with the function keyword, where we call fetch posts, of course we can also shorten this and just point at fetch posts like this without parentheses and for the form, I want to add an event listener for the submit event and then here, we get the event object where I want to call prevent default so that the browser does not submit the form and now we could also validate the form here if you wanted to, we could validate the user input, I'll not do that here, it would just be about fetching the inputs, checking the value the user entered and then maybe presenting an error, again not something I want to focus on in this module, instead I want to get my input from the field with the title and from the field with the ID content.

So to get that access, I will get my entered title by reaching out to event current target which is the form, query selector title, that should give me the title input and then .value is what I'm interested in and for the entered content, I do the same for the field with the content ID and now here I can call create post and forward the entered title and the entered content here. With that if we save that, let's reload and now we don't start with any posts here, if I click fetch posts however, they are fetched and now to add one, a new post, let's try it.

If I click add here, you see that request is sent and it contains the data we just entered. So now we connected these two requests to our UI, let's now mix it up and also see how we can send a delete request.

----------------------------------------

# 18.16 — POSTing Data with the fetch() API

> Section 18: Working with Http Requests

In order to be able to create a post, we need to make sure that this function can succeed and for that, we need to make sure that we use the HTTP method in the fetch API and also the data, the body that should be appended to the outgoing request. Right now, we always just send a fetch request to a URL and therefore we always send a get request. Now just as with XMLHttpRequest, we can configure the outgoing request, however unlike XMLHttpRequest, you don't pass the request method here directly as an argument to the fetch function here, instead you can pass a second parameter here, a second argument which should be an object where you can configure the request and there you've got a couple of keys you can set as you see, a lot of them are pretty niche and rarely need it but method is one of the more important ones.

Method should be set to a string and by default, it's set to get so you'll never need to set this but you can but you always need to set it to post, put, patch, delete and so on if you plan on sending such a request. So here I'll set it to method pointing at the parameter I'm getting here in send HttpRequest and forwarding my parameter value as a value to this key-value pair here. So that will set the method, now you can also set the body and that has to be set to JSON data.

So not just data like this, data would be my third argument here but instead, to data converted to JSON which we can do with JSON.stringify around data. If we now do that and we reload and try to enter a new post, does this work? Let's see if it works if I now click add. So if I clicked add, we go to the network tab, we see this is the post request we just send, status code 201 and indeed here, that's the body we appended. So here we can see, yes this worked, this request successfully was sent now with help of the fetch API.

Now let's also check if deleting works, if I fetch posts and I click delete, let's say on the second post, then a request is sent here to the post with id 2, the delete request has a 200 code so that seems to work. Now before we have a look at how we handle errors here, let's have a look at how we can add headers to HttpRequests, not just with the fetch API but also with XMLHttpRequest.

----------------------------------------

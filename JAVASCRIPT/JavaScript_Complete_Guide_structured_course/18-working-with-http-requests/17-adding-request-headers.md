# 18.17 — Adding Request Headers

> Section 18: Working with Http Requests

Headers can be important. Now thus far we haven't really needed them but for some APIs, you need to describe which type of data you sending for example or other APIs might need some extra authentication data and headers are basically metadata you can attach to outgoing requests. If you inspect requests, you see there are some default headers added by the browser and the response also has headers set by the server. Now we can add more headers to the outgoing request and we do that here on fetch by adding a new key to that configuration object which is the headers key.

This takes a Javascript object where every header which you want to add is a key-value pair. Now the types of headers you can add are generally standardised, there are some default headers which are typically used but you can also add any arbitrary header you're coming up with, so you're really flexible there. Of course a header makes only sense to be added if the server expects it and does something with it, otherwise you can add it but it won't have much effect.

Now a header which is often added, even though it's technically not required here for this API is the content-type header, typically written like this. Content type has a value, so that's the key name here, has to be in quotes because of the special dash character here, the value for that header then is application/json, that's one of the typical headers you add to outgoing requests which carry JSON data, this tells the server hey my request has JSON data. Now our dummy server here, JSONPlaceholder, does not care because it always just expects JSON data, other APIs might care and then this is how you could add your header. You can of course add more than one header by adding more than one key-value pair here.

Now let's see if that works, if I add this header here, if I reload and I fetch my data, we see that on this fetch request if we scroll down to our request headers, here is the content type application/json header we just added, so this is how you can add headers with the fetch API. On XMLHttpRequest, it would have worked as well, there you have to set request header method where the first argument is the header name, content type and the second argument is the value for that header, application/json and you can add multiple headers by calling this method multiple times. Important, once a header is added with this method, you can't delete it.

Now here, I'll comment this out of course because I don't need the XMLHttpRequest anymore but that is how you could have added headers there and this is how you add it with the fetch API.

----------------------------------------

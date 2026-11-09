# 28.6 — CORS (Cross Origin Resource Sharing)

> Section 28: Security

The last security hole you should be aware of or the last security relevant concept you should be aware of to be precise is cross origin resource sharing and I did talk about this earlier already. It's not really an attack pattern but a security concept. The idea here is that requests from your browser side application can only be made to a backend, so to a server side that runs on the same server, so that the HTML page and the script that executes there was served by the same server you're trying to send the request to, that's how browsers by default work with your pages, this is what they allow by default.

Now in modern web applications, you often need to send requests to other servers though, so a server which did not serve the running HTML and Javascript code but which only provides some API endpoints, some URLs to which you can send data, to store data or to fetch data, this is something we had to look at in the Node.js module. Then you can control via server side headers and only via server side response headers whether this request, this incoming request is allowed and you send back a valid response or not.

So this is a concept where by default browsers would not allow you to reach out to some other server but with the right server side headers, you can override this. So it's a concept which in the end should secure servers so that not everyone can access their resources, not every page can access their resources at least but with the right headers on the server side, you can allow this and an example for that actually would be Javascript modules. This built-in Javascript concept also required a development server if you remember and it required a development server because Javascript modules, so Javascript files you import into another file are only allowed if they're from the same server.

So I'm only used to importing another Javascript file which sits on the same server which is served by the same server and here we have no real way of changing this because that's a built-in security mechanism by browsers specifically for this Javascript feature. Another example though would be the Node.js application we worked on. There, we have our different routes which we handle on the backend, like add location and the request which is sent there is not sent from some page that is served by the same server, it's sent by a page that runs on a different domain, on a different server and still it works because here, I set these right CORS headers which tell the browser that's okay, this page which sends the request is allowed to get the data and therefore the browser won't block it.

So it's a security mechanism which you can use or disable or configure to your needs based on your requirements. That's the idea behind CORS, this cross origin resource sharing concept.

----------------------------------------

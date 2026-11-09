# 13.10 — Deep dive of client credentials grant type flow in OAUTH2

> Section 13: Deep dive of OAUTH2 & OpenID Connect

Instructor: CLIENT CREDENTIALS GRANT TYPE FLOW is the most commonly used grant type flow inside the microservices environment. We need to use this grant type flow when now there is no end user is involved and when our two backend applications are two different APIs that are trying to communicate with each other. So this Resource Server can be a microservice and this client also can be another microservice, or some other backend application or backend API who are trying to talk with each other.

But instead of directly allowing them to talk with each other, we are going to enforce security with the help of Client Credentials Grant Type Flow. Behind the scenes, what this client application has to do is it has to register with the auth server and it needs to get its own client credentials. So once this step is completed, the client application, it is going to resume client ID and client secret. So these values are going to act as username and password for this client whenever it want to get an token from the auth server.

So let's try to understand how this flow is going to work. Like I said, there won't be any end user involved whenever there is no end user involved, we can blindly use the Client Credentials Grant Type Flow instead of Authorization Code Grant Type Flow or PKCE Grant Type Flow. In the very first step, the client is going to approach the auth server to provide an access token and inside the request it is also going to mention its client credentials and since there is no user involved inside this, it's not going to share any end user-related details.

If the client credentials are valid, the auth server, it is going to issue an access token to the client. Now my client, which can be a microservice or a backend API or a backend server, it can invoke another backend server or another backend API or microservice. In the step three, so inside the step three it is going to invoke the Resource Server where the resources that it is trying to fetch are present. Inside these third request is going to send the access token as well, along with the other request details.

If the access token is valid, the Resource Server is going to reply with the proper successful response. I hope you're clear. It is a very simple grant type flow and it's very easy to understand. The only thumb rule that you need to be aware is you need to choose this grant type flow whenever there is no end user is involved. Inside my microservice course, I have used this grant type flow to a great extent while I am trying to enforce security between multiple microservices.

Inside the next slide, I also provided more details like what are the details that my client application is going to send to the auth server inside the step one. It is going to mention client_id, client_secret, along with the scope and grant_type, the grant_type value, we need to mention client underscore credentials. So this is an indication to my auth server that it should not expect the end user details with whatever client details provided by the client application using this only it has to perform the authentication and issue the access token.

Unfortunately, there is no option here to see the demo of the Client Credentials Grant Type Flow. But don't worry once we adopt to Oauth 2.0 standards inside our own Spring Boot application, I'm going to show you the demo of Client Credentials with the help of the postman. I hope you're clear. Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------

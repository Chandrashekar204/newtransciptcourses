# 16.9 — Refresh token grant type flow demo with Spring Auth Server

> Section 16: OAUTH2 Auth Server using Spring Authorization Server

Instructor: Inside this lecture, let's try to test the Refresh Token Grant Type flow. We know how to test the Refresh Token Grant Type flow. If you click on this refresh button, the refresh token flow is going to be initiated behind the scenes. So let me click on this refresh and you'll see I'm getting an error. Let me see the console of my Spring Auth server inside my Spring Auth server I see an exception. Let me go to the top of the exception to identify the issue.

Here I have a logger stating that client authentication method failed. So the authentication() method, whatever right now we configured for the client is not enough to test the refresh token grant I flow. So I debug this framework code behind the scenes and the reason why we are getting this issue is as of now for the both these client's Auth code client and the PKCE client, we have configured the authentication() method as client to secret post.

But during the refresh token grant I flow the postman it is going to send the refresh token using the http basic format. Since our client is not supporting that method, we are facing the issue. So what I can do is I can try to repeat this line of code and instead of CLIENT_SECRET_POST, I'll just mention CLIENT_SECRET_BASIC, the same, I'll try to configure for the PKCE client as well. So with this we should be good and for the very first client, which is clienCcredentialClient, but this client, we have not enabled a refresh token grant I flow.

The reason is very simple. This client is supposed to be used by the backend services. So whenever they're making a service call, they should get an access token and use the same with the resource award. We should not give the flexibility of the refresh token, but the API to API communication scenario because that is not standard. That's why I have not configured the Refresh Token Grant Type flow with the clientCredentialsClient. So let me save these changes to the build.

So let me get a new access token because we have changed our client to configurations. That's why I want to get a new access token before trying the Refresh Token Grant Type flow. So let me click on this new access token and I received a new access token and along with the new access token, I also received the refresh token as well. Let me use this token. So as of now you can see my token is going to be expired in 10 minutes, which is 6:33 PM, so right now the time is 6:24.

So if I try to refresh this token, I should get a new token with a new expiration time. So the Refresh Token Grant Type flow, we should be able to invoke before the access token expiration as well. So if I click on this refresh this time, you can see I got a new access token that is going to expire at 6:34. You can also check the console and here towards the end, if you open this post under the RequestBody, you'll be able to see this is the refresh token and the grant Type Refresh Token.

This confirms Refresh Token Grant Type flow is also working fine. As a last step from the next lecture, let's try to test one scenario by changing the self-contained to the opaque token format. Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

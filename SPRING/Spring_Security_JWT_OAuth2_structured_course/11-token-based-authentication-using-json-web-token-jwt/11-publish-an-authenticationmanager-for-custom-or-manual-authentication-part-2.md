# 11.11 — Publish an AuthenticationManager for custom or manual authentication - Part 2

> Section 11: Token based Authentication using JSON Web Token (JWT)

Instructor: To test our changes that we have done in the previous lecture, you need to open these API login request under the section11 folder. Please make sure this API is invoking with the help of POST method. And under the authorization, you don't have to mention any authorization, but inside the body, you need to make sure you're sending the same JSON with the field names as username and password. Before I try to click on the send button, let me keep a break point inside my UserController.

So here inside my apiLogin()method, I'm going to keep a break point. Now I'm going to click on the send button. Let's try to debug this method line by line. So first, I'm trying to create an Authentication object representing unauthenticated. Later on, I'm trying to manually authenticate the user. So once the authentication is successful, we are going to have this isAuthenticated value as true. And with that, this if condition is going to be executed.

For some reason, I'm getting these env as false. So let me release this breakpoint. Inside the response, I'm just simply getting the okay but no jwtToken. Let me go to this env variable declaration. Here, while I'm trying to inject this bean, I forgot to mention final. So let me mention this final and do the build. Once the build is completed, I'll try to send the request one more time. So let's try to debug this method line by line. This time there should not be any issues.

Seems we're going to create our jwtToken successfully. So if I release this break point, inside the response, you'll be able to see status as okay, and this is a jwtToken. I need to take this value. You'll be able to see inside the head desk also. There is an response header with the name authorization with the same jwtToken value. So using these jwtToken value, my client applications, they should be able to invoke the other APIs. For example, if they want to invoke this myAccount API, they just need to make sure inside the RequestHeader with the name authorization, they have to pass the same jwtToken value that they have received previously.

So let me click on the send button. As soon as I click send button, I'm getting a 403 error. Let me take this jwtToken value and try to analyze what is happening. Inside this website, I'm going to paste the jwtToken, and under the payload, you'll be able to see there are no authorities information inside the payload. That's why I'm getting a 403 error. So let's try to debug what is the issue. I think the problem is with the copy paste that we have done.

So while we are trying to generate the jwtToken, we are referring to the Authentication object here. Instead, we should refer to these authenticationResponse object. So it is going to have the authorities details. So that's why let me try to use the same here in both these places. So once this change is completed, we should be good. Let me do the build. Once the build is completed, I will go to the apiLogin and try to generate a fresh jwtToken. So let me take these jwtToken value and paste it inside the AuthorizationHeader.

Now this time, we should get a successful response, and in fact, we are getting a successful response. With this manual authentication approach, you should be able to handle any kind of business requirements that you may have inside your real projects. I hope you're clear with all the changes that we have done. So let me try to do the similar changes inside my other ProjectSecurityConfig file. I need to open ProjectSecurityProdConfig, and here, I'm going to paste the same bean.

But inside this bean, instead of EazyBankUsernamePwdAuthenticationProvider, you need to use EazyBankProdUsernamePwdAuthenticationProvider. After creating this bean, you should also make sure you are mentioning the apiLogin under the permitAll(). The same API should also be mentioned inside the CSRF ignoringRequestMatchers() as well. I hope you're clear. Whatever quote that we have discussed so far inside this lecture, I have mentioned all of the quote snippets in these two slide for your future reference.

Thank you, and I'll catch you in the next lecture, bye.


########################################

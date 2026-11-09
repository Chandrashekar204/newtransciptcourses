# 8.11 — Demo of default CSRF protection inside Spring Security

> Section 8: Understanding CORs & CSRF

Instructor: As a next step, we are going to focus on CSRF security attack. Unlike CORS, CSRF is a proper security attack that leveraged by the hackers to steal the data inside your applications or to perform some privileged actions inside your application. We're going to discuss in detail about what is a CSRF attack and how an hacker is going to use this attack to perform an illegal action inside an web application. But before that, inside this lecture, let me show you a small demo on how Spring Security is protecting the web applications from the CSRF attack with the default configurations.

As of now, inside our security configurations, we have disabled the CSRF related protection that is provided by the Spring Security framework. That's why we're able to make some post request. Inside the register API, we use this post API to create the new data inside our backend server. This is possible because we have disabled the CSRF protection completely. But disabling the CSRF protection by the Spring Security is not recommended for production applications.

We need to properly implement a solution to handle the CSRF attacks. If you don't implement CSRF related solution inside your application, then by default, Spring Security is going to stop all your http methods that are going to alter the data or create the data or delete the data. To show you the default behavior of the Spring Security framework, what I'll do is I'll try to remove this csrf() related configurations. With this, what is going to happen?

Spring Security will start securing all your posts to put, to delete related methods by throwing an 403 error. So let me save these changes. Do the build. Once the build is completed, I'll try to invoke these post API one more time. If I click on the send button, this time you'll see I'm getting an 404 error because behind the scenes, Spring Security what it it in construing is, it is trying to invalidate my session so that I can't create this data on the backend side.

So whenever the invalid session is happening, we are going to redirect the end user to the invalid session path. But since this path is not available, it's throwing me the 404 error. What I can do is, I'll try to delete all the sessionManagement() related configurations so that we can completely focus on the CSRF. So if I try to save these changes, do the build, this time if I try to send the request, you'll be able to see a proper 403 error with a message saying that invalid CSRF token 'null' was found on the request to parameter.

Why we are getting this error? We are getting this error because we are trying to create a new data with the help of post method, but we are not passing any CSRF token as part of our request. Whenever the CSRF token is missing, the Spring Security will assume that someone is trying to attack our application with the help of CSRF attack. That's why it stopped processing this request by throwing the 403 error. The same kind of behavior we can also observe from the UI application as well.

As of now from the UI application, we're able to invoke the notices API. And since notices API is a GET() method, CSRF related checks won't come into picture because as part of the GET method, anyone can only read the data but they can't update the data or create the data or delete the data. That's why Spring Security gave a flexibility by allowing all the GET API methods, even though if you don't implement any CSRF related solution. But coming to the POST, PUT methods, or DELETE methods, it is going to stop.

I can also show you a demo by going to the Contact Us page. So here I'll try to enter my details, like Madan Reddy, and I'll try to enter the email as tutor@eazybytes.com. Subject, I'll just mention Test Subject and message I'll try to mention as Test Message. So let me open the developer console. As soon as I press this button, a backend API of type HTTP post is going to be invoked, but we know that Spring Security is going to stop this request.

So let me click on this send message. You can see we are getting 403 forbidden error. This is due to CSRF attack protection provided by the Spring Security framework. So to resolve these CSRF related errors, we have two options. One needs to completely disable the CSRF protection provided by the Spring Security framework, which is not recommended for critical applications and production applications. And the other solution is we need to properly understand what is a CSRF attack.

Once we understand the details of the CSRF attack, we need to make some changes on the Spring boot backend application to handle the CSRF attack. Once these changes are completed, then we should be happily invoke any kind of HTTP methods. I hope you're clear about the fact that Spring Security, by default, it is going to secure your web applications from CSRF attack. In the next lecture, let's try to understand what is a CSRF attack and how to handle it.

Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

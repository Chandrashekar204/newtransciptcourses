# 10.4 — Adding a custom filter using addFilterAfter() method

> Section 10: Custom Filters in Spring Security

Instructor: Inside this lecture, let's try to create a custom filter and configure the same using addFilterAfter() method. To create my own custom filter inside this lecture, I have taken a business scenario, which is once the authentication is successful, I want to log a message with my own custom filter saying that so-and-so user authentication is successful with so-and-so authorities. I have taken a very simple scenario just to keep our discussion very simple.

But in your real applications, you may have good amount of scenarios which you may need to handle based upon your business problem once the authentication is successful. Since we are looking to execute a custom filter post-authentication, we need to configure our own custom filter, which is a logging filter, after the BasicAuthenticationFilter. So by the time the BasicAuthenticationFilter is executed completely, the authentication is going to finish.

Once the authentication is completed, my custom filter is going to be executed. That's why this time you'll be able to see that my custom filter order number is going to be four and the BasicAuthenticationFilter order is going to be three. One more time, I'm highlighting here this order numbers. They're just my imagination. In reality, the order numbers may change. I hope you're clear with the scenario. Let's implement our own custom filter inside our web application.

Inside the filter package, I'm going to create a new Java class with the name, AuthoritiesLoggingAfterFilter. The name can be anything. You can give whatever name is comfortable for you. Next, we need to implement Filter interface from the jakarta.servlet package and overwrite the method, doFilter(). Since I'm looking to write some log statements, I'm going to mention lambok annotation Slf4j. Since I'm going to implement a log statement, which is going to log about the authenticated user, first I need to get the current authenticated user details from the SecurityContextHolder.

Using the SecurityContextHolder, I can invoke the getContext() method. Inside this getContext(), I have a method, which is getAuthentication(), the same I'm trying to invoke. And on the left-hand side I'm going to catch the output with the variable name as authentication. Next, I'm going to perform null check, if the Authentication object is not null or not. Once my not null condition is satisfied, I'm going to write a log statement, which is going to log an info statement.

So to this info method, I'll try to pass a String as an input. You'll be able to easily understand the String. So first, I'm trying to mention hard-coded user String followed by who is the current authenticated user with the help of this authentication.getName(). It's successfully authenticated and has the authorities and the authority details I'm trying to get with the help of these getAuthorities.toString() method. So this is the only logic that I want to execute in my Filter.

But like I said before, in real applications you may have more complex requirements. At the end, I need to make sure I'm invoking the doFilter() method with the help of chain and to the same, I need to pass the request and response. So let me configure this filter inside the ProjectSecurityConfig. So this time, instead of addFilterBefore(), I'm going to invoke the addFilterAfter() method and pass the object of AuthoritiesLoggingAfterFilter. So let me save these changes. Do the build.

Once the build is completed, I'll keep a breakpoint inside the AuthoritiesLoggingAfterFilter. So let me send this request. You'll be able to see the breakpoint stopped here. If I try to debug, I'll have an authentication object. Inside the authentication object, I have details like principle authorities and authenticated as true. With this, my if condition is going to be satisfied and my log statement is going to be logged on to the console. If I go to the console, I'll be able to see a statement saying that User happy@example.com is successfully authenticated and has the authorities, ROLE-ADMIN, and ROLE-USER.

So by default, in the leads it is going to display the log statement in a single line. But if you're looking to wrap the log statement, you just have to enable this soft wrap. So if I disable this, this is how the log statement is going to be displayed but I felt wrapping the log statement is always going to be developer-friendly so that we don't have to scroll onto the right and left. We can always scroll up and down. So let me release the breakpoint.

And once the breakpoint is released, you'll be able to see a successful response here. And inside the console, I also want to highlight about the SecurityFilter Chain related log. So if I go to the top, you'll be able to see this is the SecurityFilterChain that got executed. And inside the SecurityFilterChain, you'll be able to see our filters as well. So just before the BasicAuthenticationFilter, the RequestValidationBeforeFilter executed. And just after the BasicAuthenticationFilter, the AuthoritiesLoggingAfterFilter is executed.

So we also have another filter configured, which is CsrfCookieFilter. So once the CsrfCookieFilter is executed, the AuthoritiesLoggingAfterFilter is getting executed in my scenario. But I'm assuming this order, it is going to be completely random. But regardless of this order, as long as our filters are getting executed after the BasicAuthenticationFilter, we should be good. I hope you're clear with the simple filter that we have created so far and configured with the help of addFilterAfter().

Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

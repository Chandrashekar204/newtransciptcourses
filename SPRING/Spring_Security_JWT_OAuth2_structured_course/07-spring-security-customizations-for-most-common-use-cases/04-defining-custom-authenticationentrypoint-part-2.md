# 7.4 — Defining Custom AuthenticationEntryPoint - Part 2

> Section 7: Spring Security customizations for most common use cases

Instructor: Apart from configuring the AuthenticationEntryPoint using the httpBasic() configurations, we can also perform the similar kind of configurations at a global level. Let me try to show you the same. Using the same http variable, we need to invoke the exceptionHandling() method. So to this exceptionHandling() method, we can pass the custom configurations using a Lambda expression. Let me try to define a variable name to the input of the Lambda expression.

So I'll just mention ehc, which means exceptionHandlingConfig. Using the same ehc, I can try to invoke the authenticationEntryPoint(). To this authenticationEntryPoint(), we can send the object of CustomBasicAuthenticationEntryPoint class. This is another style of configuring the authenticationEntryPoint() inside Spring Security. This approach has advantage, which is it is an global config, which means inside your project, whenever an AuthenticationException happens, then these CustomBasicAuthenticationEntryPoint logic is going to be executed.

But the same authenticationEntryPoint() configuration, we can't configure for the formLogin. I can also confirm you the same here. Let me mention a variable name, which is flc followed by... Using the same flc, If I try to invoke for authenticationEntryPoint(), there is no such method supported by form Login. Do you know the reason? The reason is very simple. During the form Login, we are going to deal with the UI pages but not with the JSON response or response.

The end user who is using the UI application, you don't bother about looking for the ResponseHeader, ResponseBody. That's why whenever we are trying to use the form Login, we have other type of configurations that are supported by the Spring Security. For example, we can configure what is a login page that we need to show to the end user. And similarly, we have many other methods like defaultSuccessUrl(), failureHandler(), loginProcessingUrl(), failureUrl().

I'm going to teach you in detail about form Login configurations in the coming lectures. For now, let's go with the default configurations. With this explanation, you may have a different question, which is, you said only the authenticationEntryPoint is supported by httpBasic(). Then what is the need of configuring these authenticationEntryPoint() at globally with the help of exceptionHandling? It's a great question. Let me try to clarify your question.

If you try to configure the authenticationEntryPoint() only for the httpBasic(), then these authenticationEntryPoint() is going to be executed or considered only during the httpBasic() flow, like during the login flow. But apart from login flow, Spring Security may also throw 401 or AuthenticationException in many other places throughout the framework. To handle all such possible scenarios, you can go with these global configuration. I hope you are getting the difference between these two configurations, but for now I'll go with these httpBasic() specific configurations only.

I'm going to remove these global configuration, because in our application we don't have such complexity to configure authenticationEntryPoint() at the global level. But like I said, in real project, if you have such requirements, you can configure at the global level as well. Whatever we discussed around the AuthenticationEntryPoint, I have mentioned all the details inside these slides. First, I tried to explain about the contract of the interface AuthenticationEntryPoint.

I also highlighted a couple of entry point that are commonly used by the Spring Security framework. BasicAuthenticationEntryPoint is going to be used during the httpBasic() flow. Similarly, LoginUrlAuthenticationEntryPoint is going to be used during the form Login flow. In the next slide, I also highlighted on how to create your own CustomBasicAuthenticationEntryPoint and how to configure the same with the help of the httpBasic() method supported by the Spring Security framework.

At last, I also highlighted on how to configure AuthenticationEntryPoint globally with the help of exceptionHandling() method. I hope you are clear. Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------

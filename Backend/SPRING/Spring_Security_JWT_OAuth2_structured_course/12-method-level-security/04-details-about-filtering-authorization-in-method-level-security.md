# 12.4 — Details about filtering authorization in method level security

> Section 12: Method Level Security

Instructor: We are clear about what is invocation authorization and how to implement it with the help of reauthorize and @PostAuthorized annotation. As a next step, let's try to understand what is Filtering authorization. With the help of this Filtering authorization, we should be able to control what kind of input that a method can accept and what kind of output that a method can return to the client application. Let's try to understand what annotations are involved when we are trying to implement Filtering authorization inside our web applications.

The very first annotation that we can use ease @PreFilter annotation using these @PreFilter annotation, we should be able to control what kind of input that my method can accept, whenever we are looking to use @PreFilter annotation on top of a Java method, we need to make sure that the method is accepting a collection object as an input. So here I have a method which is sale contact inquiry details. So this method is going to accept list of contact objects unless my method is not accepting a list or a collection object, I cannot enforce the Filtering authorization.

That's why as a very first check, please make sure that your method is accepting a collection object as an input parameter. So inside this collection object, we are going to store the contact related objects. So whatever expression that I'm going to write, with the help of @PreFilter annotation, it's going to be applied for each object that I have inside this list input that I have received. Every object that we are going to receive as part of the collection object, we're going to refer it with a standard name, which is filterObject.

So here the filterObject is going to be of data type Contact because we're trying to accept list of Contact as an input. So inside this Contact to Pojo class, there might be a field name with the name, contactName. That's what I'm trying to use here. So if this contactName is not equal to test, then only I want to accept that Contact object as an input inside my List object. Otherwise, if someone is trying to send a contact details with a contactName as test, I'm going to simply ignore such records and I'm not going to send such record as an input to this method.

So this is one style of Filtering authorization. If you want, instead of this test, you can write the logic to check the current authenticated username. I hope you're clear in the similar lines, we also have @PostFilter annotation. The purpose of this @PostFilter annotation is whatever data that you are going to return from your method, it is going to be examined based upon the configurations that you have provided, and accordingly, the data is going to be filtered.

Here I have just changed the annotation from @PreFiltered to @PostFilter, but I'm using the same expression inside the configurations. With this, what is going to happen is inside these list of contact response that I'm going to get from this method, if there is a Contact object with a contactName as test, then search record will never be received by my client application. If required, we can also use @PreFilter and @PostFilter annotations, both of them on a single Java method.

The same applies for @PreAuthorized and @PostAuthorize as well. If you have a business requirement, we can club both @PreAuthorized and @PostAuthorize on top of a single method. But the same annotation is not allowed to use multiple times on top of a Java method. Let's try to validate where inside the spring security framework these @PreFilter and @PostFilter related checks are going to happen. Inside the search box, you can search for with *PreFilter, and with that you'll be able to see there is a class with the name PreFilterAuthorizationMethodInterceptor.

So this class, it is going to act as a method interceptor, which filters a method argument by evaluating an expression from the @PreFilter annotation. The same is highlighted inside these class documentation as well. Similarly, there should be a class with the name PostFilterAuthorizationMethodInterceptor. So this class, it is going to handle all the expressions that we are going to provide for the @PostFilter annotation. I hope you're clear on how to define @PreFilter and @PostFilter annotations.

In the next lecture let's see the demo of this annotation by enforcing filtering authorization inside our web application. Thank you, bye.

----------------------------------------

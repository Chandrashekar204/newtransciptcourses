# Step 03 : Stubbing Example - with Disadvantages of Stubbing

*Section: Need For Mockito*

Instructor: Welcome to the third step of this Mockito course. Thanks for the patience that you showed in creating the small example in the last step. And in this step we would try and test the last example with a stub. So we would learn what is a stub and we would create a unit test with a stub and we will understand what are the disadvantages of using stubs. To just get an overview of what we did so we have a TodoService which is the dependency of this particular class.

This TodoService is being implemented by some other team which we don't have access to, but we would want to be able to test the TodoBusinessImpl. What we would need to do is to create some kind of a TodoService. So one of the things that we can do is create something called a stub. A stub is nothing but a sample implementation of this particular TodoService. So I can create a stub class which implements this particular interface.

So what we'll do now is we'll create a stub for TodoService and we will try to use that stub to test the TodoBusinessImpl. So there are basically two steps that we want to do. So the two steps are, one is create TodoServiceStub and second thing is test the TodoBusinessImpl using the TodoServiceStub. Let's start creating the TodoServiceStub very quickly. So since this is stub I don't want to really create a stub in the main codes.

I mean I don't want this stub to be included in main code. So what I'll do is I'll create this stub in the test Java and I would kind of use the same package structure so it's com.in28minutes.data.api. So I'll say right-click, New. This would be a Java class and I would want to do com.in28minutes, package would be same as the original class data API and I would want to call this class TodoServiceStub.

Stub is nothing but a class which returns some kind of dummy data. So I'll go ahead and I would want to implement so I'd want to create a dummy implementation of the TodoService. So I'll say implements TodoService. There's a compilation error. Why is there a compilation error? Because the TodoService has this method. The TodoService has a method to do which we need to stub now. So let's say now add unimplemented method.

So this would create a dummy TodoService method or you can manually go ahead and create this method as well, public List String retrieveTodos. So instead of returning null what I would want to return is an array list with a couple of values in there so that I can use this as a stub for testing the TodoBusinessImpl. So what I would want to do is create a... So Arrays.is list is a very useful, Arrays.asList, sorry it's a very use useful function.

So if I want to create two items, 1,2, so Arrays.asList 1,2 would create that for me. So this would create a list of these two and return it back. What I would want to really give is a little bit more useful values. So I'm giving a list of todos. So I'll enter a little bit better values than one, two. So I'm creating Learn Spring MVC, Learn Spring, Learn to Dance as the list of todos that I would want to retrieve.

So this is a dummy implementation. You can see that this TodoService we are creating a dummy implementation for that. So this is a stub. So this is a sample implementation of the TodoService. I'm not really talking to the service at all. I'm actually hard coding values and returning them back so that now when I'm testing the TodoBusinessImpl I can make use of this stub. So now let's try and test the TodoBusinessImpl.

So I would go to right-click and say New, Other and I would type in test. So I would want to create a new JUnit test case so Next. I can say which package I would want to put the test in. I'll use the same package as the original class. So com.in28minutes.business that's where the original class is. And I would want to call this TodoBusinessImpl because I'm using a stub here I'll call it ImplStubTest and click Finish.

As usual, a sample test is created for us. So what I would want to do now is I would want to be able to use this stub to do the testing for TodoBusinessImpl. So first thing is I would want to create a TodoBusinessImpl. So TodoBusinessImpl, let's create a TodoBusinessImpl. todoBusinessImpl is equal to new TodoBusinessImpl. So to create a TodoBusinessImpl I needed todoService. So let's go ahead and first create a TodoService.

TodoService todoService. todoService I would want to create a todoService is equal to new. What we want to make use of in this test is the new TodoServiceStub. So I'm creating a TodoServiceStub. To be really specific compilation error, I have to input this in. To be really specific, I'll actually rename this. So I'll call this todoServiceStub. So the shortcut is all Shift + R, or you can actually do right-click, Refactor, Rename.

So that's the one which you can use to change the name of a variable. So I've renamed this to todoServiceStub and I've now created a TodoBusinessImpl with the todoServiceStub. So now we can use this stub to test the method. So I would want to call the method todoBusinessImpl.retrieveTodosRelatedTo some dummy user. I don't really care who the user is because we are hard coding it in this stub and I'll take this and I'll put it in a local variable.

So List filteredTodos. That's basically it. So since this is a unit test, what we would want to be able to do is to check the filtered list of todos. So what we did in the TodoServiceStub is that we put in one, two and three and out of which only two are related to spring. So I would want to check whether the list which is returned back contains only two values. So let's do that. How do we do that?

We use the assertEquals. assertEquals the first one is expected. So we want the size of the filteredTodos to be two. I would want to give a better name to this. So typical naming convention is test and the method, testRetrieveTodosRelatedToSpring. I prefer using an underscore to say usingAStub. So this makes it clear that this particular test is using a stub to test that. I mean here it's already, we are putting it here as well.

So it's a duplication depends on whether you like it or not. So I'll do right-click, Run As, JUnit Test. So there you go. Now we are able to test this particular thing using the stub. So for the TodoService we created a stub and we return dummy values and we use those dummy values to check whether this is working or not. So this is how you can create a test using a stub for anything that you depend on.

So this TodoBusinessImpl depends on TodoService. And what we are doing is we created a stub called TodoServiceStub and it returned dummy values back. So now this is good. So we are able to write this test. I mean this is a good test. We can improve this test further to not just look for the size, but to check whether the exact todos are populated or not that I would leave as an exercise for you. So if you look at the exercise, one of the exercise would be to improve the asserts for the ArrayList.

So right now we are just looking for this size whether it's two, but actually we can test much more. So what we can actually check is whether the two items in the ArrayList are these two. So that I would leave as an exercise for you to do. What we want to really focus on is what are the advantages and disadvantages of using a stub to test. So now this stub is nothing but a real Java class. So let's say I want to create another test case.

So here this particular test case I created where the stub is returning three values. But let's say I want to write another test case where this particular method is returning only one value back or it's not returning anything back. So I want to create another test wherein I would want to check for a scenario where I'm passing empty like when I'm getting no values from the service using a stub I'll just call it two, let's just, I mean it's a meeting so it doesn't matter what they call it.

But in this test I would want to actually check whether when there is nothing returned back from the service, where there is nothing coming back from the business Impl as well. Here what one of the options I have is I can pass in a dummy one and then I have the user. So I can say if user is dummy, then return this. If else user is dummy one, return something else back. Now you can see how complex that kind of a code can become.

So as in when I need more things then I would need to keep adding logic to my stub. So the stub class will start growing a lot. The other problem you'd have typically when you're using stub is the fact that let's say in addition to this, there is another method which is coming in. So let's say in this particular thing I'm adding a method String user. And let's say there is a new method instead of retrieveTodos I would say configureSomething for a user.

There's a new method in the interface. What you'd see is this stub. Now you need to create the new method in this stub as well because this stub implements the TodoService. It needs to implement all the methods which are there in this service. So this is the other problem. So you need to start having a lot of maintenance headaches because you're using stubs, because stubs are nothing but like a dummy implementation of the interface.

Whenever you add a new method, delete a new interface or anything of that kind you need to keep maintaining this stub as well. So the two main problems with using a stub are dynamic conditions. So when I want this particular method to return different kinds of values in different kinds of scenarios, then it becomes very complex code. So this code will start becoming very large and difficult to maintain.

Stubs are useful in very, very simple scenarios, but in most of the projects we use something more dynamic called mocks. We will get introduced to mocks in the next step. In this step we looked at a sample test using a stub. We saw how to create a test using this stub and also we looked at what are the problems that we usually face when we write tests using stub. In the next step we would start using a mock.

Until then, bye.

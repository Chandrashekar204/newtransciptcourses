# Step 14 : Theory : Why does Mockito not allow stubbing final & private methods?

*Section: Mockito Advanced*

Teacher: Let's take a break from all the hands-on stuff, we are doing and this would really be a theory step. So what we learned during this step is why does Mockito not allow stubbing final and private methods? We will actually go to the Mockito site and see why they don't allow it. So just go to the link down here and you would see that Mockito doesn't mock private methods. You can read this stuff down here but the summary is basically, Mockito wants to promote good design and good testing concept.

One of the things about unit testing is we are supposed to test the public interfaces of a class. Mockito wants to really promote that. That's the reason why Mockito does not allow mocking private methods. Let's go to the FAQ and read a little bit more. So this a FAQ for Mockito. You can find the link in here. So here you'd actually kind of looked through all the decisions that the Mockito framework, creators made when they started creating Mockito.

So they had to make a lot of choices and they chose a few things. One of the important things is, you cannot mock final classes. You cannot mock static methods. These are all there because of reason. So typically having static methods is considered to be a bad object oriented design and you wouldn't want to depend, I mean you wouldn't want to mock a static method in a really well designed program.

So that's the reason why Mockito does not support these. There are other frameworks like PowerMock when used with com Mockito you can override. I mean you can mock final class, you can mock static methods, but Mockito by itself does not support, like mocking final and static classes. And with Mockito as we already saw, we can mock both classes and interfaces. We looked at what are the values which mocks return by default.

So you can see that. So you cannot mock static methods. You cannot mock private methods. I doubt if you'd be caring about, whether it's thread safe or not, but just go through this list down here. This is a really good set of things that you can look through to understand Mockito further. The other thing I would really recommend you to do is, with Mockito is to always know the other frameworks which are in this specific field.

So if you look at Mockito the real, like one of the first mocking frameworks, which was really famous was EasyMock. So you can try and understand the comparison between Mockito and EasyMock. There is a really good page. I mean, typically I would never refer to the create like Mockito is a competitor to EasyMock and I would really never want to go to a Mockito page and see the comparison versus EasyMock because the comparisons will always be in the favor of Mockito framework.

But having said that, I think this is a really a fair comparison. I've worked with both EasyMock and Mockito and I think Mockito is really better framework in terms of readability of code. On this page you can see how things can be written with EasyMock and how it's different from Mockito and how you, you can also see that writing EasyMock test, is a little bit more complex than writing a Mockito test.

So you can see a little bit of more information down here on what is the difference between Mockito and Easy Mock to understand Mockito much further, the idea behind this step was to just give you references to where you can go and try and find more information about Mockito. We understood the basic, most frequently used features of Mockito, but it might be good for you to understand what the Mockito framework creators were thinking when they created the framework.

So all the things that we discussed during this step will help you to do that. It's not if, if you're a beginner, what like it's not really necessary for you to understand whatever we are talking completely. But if you're interested with Mockito then you can actually go and read everything that's there in the links that we referred to through this step.

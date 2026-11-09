# Overview of this Section

*Section: Need For Mockito*

Instructor: Hi, there. Welcome to this section "Getting Started". One of the most important things with Mockito is to understand why we are using Mockito, to understand what kind of a context Mockito fits in, and to be able to understand that we need to set up our system under test. We need to set up an example that we would want to test. The example that we would be using is a to-do service. This is basically an interface.

You can kind of think of it as it integrating with some external web service or over MQ or some external system and getting it as a list of to-dos. And what we would want to be able to do is to provide business logic around it. So what we'll do is we'll create a to-do business IMPL which will use the to-do service. What we'll try and do throughout the examples that we would be doing as part of this course is we'll try and mock the to-do service.

So instead of talking to the external systems, we would mock this. We would kind of make it return the values that we would want. And using those values, we would be testing the different methods which are present in to-do business IMPL. So that's the first thing that we would do is we would try and unit test this with a stub. What we'll do is we'll create a to-do service stub which kind of returns hardcoded values and we'll write a unit test using that.

So we'll write a unit test called TodoBusinessImplStub test that we will do as part of our unit testing with stub example. And once we understand system under test, once we understand how stubs can be used to write unit tests, we will start really writing tests with Mockito. This is really going to be a little slow, but I think with Mockito, it's very important to understand the concepts of stubbing and also understanding the system under test so that we can write really good tests around it.

Have some patience for the next couple of steps, you would be doing a lot of setup and be doing a lot of basic work. But when we start using Mockito, things will really get interesting.

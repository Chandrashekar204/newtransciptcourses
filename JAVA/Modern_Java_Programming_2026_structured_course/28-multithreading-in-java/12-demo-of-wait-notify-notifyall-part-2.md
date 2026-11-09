# 28.12 — Demo of wait(), notify(), notifyAll() - Part 2

> Section 28: MultiThreading in Java

[00:00] Let me create a new Java class with the name ProducerConsumerExample. Inside this class
[00:08] first I need to create the main() method, followed by
[00:10] first, I'm going to create the object of SharedResource class that we have created previously.
[00:16] Once this object is created, we can get started with creating the thread objects.
[00:22] So the very first thread that I want to create is Producer thread.
[00:26] So that's why I'm trying to give the name as Producer thread.
[00:30] Now, on the right hand side to the constructor of Thread, I'm going to pass a lambda expression as
[00:37] an input.
[00:38] So my lambda expression is not going to accept any input parameter, followed by I'm going to mention
[00:43] lambda symbol.
[00:44] And inside the curly braces I'm going to write some business logic.
[00:48] So the logic that I'm going to write is I'm going to have a for loop, which is going to help this thread
[00:54] to produce five different int values. Inside my for loop,
[00:58] let me mention int i = 1, followed by int I <= 5, followed by
[01:06] i++.
[01:06] So now inside these five loop I can try to invoke the produce() method available inside the SharedResource
[01:15] object.
[01:15] And to this I can pass the index value which is i.
[01:18] So basically you can see my Producer thread
[01:21] during each iteration,
[01:23] it is going to invoke some value based upon the index number.
[01:27] So at a max it is going to produce five different values.
[01:30] Post that I'll try to make this thread to sleep for a second, so that we will be able to see the
[01:37] output properly.
[01:38] So here we are getting a compilation error to handle the checked exception.
[01:42] What I can do is, I'll try to go to the more actions and select the option which is surround with the
[01:48] try or catch.
[01:50] So once the thread object is created, I want to start it with the help of start() method.
[01:55] So let me invoke the start() method in the similar lines
[01:59] I also want to create one more thread, which is responsible to consume the data that my Producer is
[02:06] going to generate.
[02:07] That's why let me paste the same code and rename this variable to Consumer thread.
[02:13] And inside this for loop, instead of invoking the produce() method, we need to invoke the consume() method,
[02:19] which is not going to accept any input and post that using the same Consumer thread object, I'm going
[02:24] to invoke the start() method.
[02:26] So let's hope for the best.
[02:27] Let me try to execute this program and see what is going to happen.
[02:30] So you can see for every second my Producer is producing a value immediately.
[02:36] My Consumer is trying to consume like Produce 2, Consume 2, Produce 3,
[02:41] Consume 3, Produce 4,
[02:42] Consume 4, Produce 5, Consume 5.
[02:45] So let's try to understand how we are getting these output for the same.
[02:48] First we need to go to the SharedResource.
[02:50] So initially isEmpty() is true.
[02:53] And with that this while block is never going to be executed, the thread will directly execute this
[03:00] piece of code.
[03:00] So here it is trying to assign the value one to the data and update.
[03:05] This boolean isEmpty() as false and executing the System.out.println().
[03:10] So after printing the statement we're also invoking the notify() method because based upon this initial
[03:17] value true this Consumer thread, it is going to be waiting.
[03:22] And since we want to notify() it to wake up and execute this condition again, this time this isEmpty()
[03:28] is false.
[03:29] And that's why this while block is not going to be executed and the Consumer is going to execute this
[03:34] piece of logic, once this piece of logic is executed, once the consumption of the data is completed,
[03:40] again, we are trying to notify the Producer thread to wake up and generate the new value.
[03:46] So this kind of iteration, it is going to keep on happen until our for loop execution is completed.
[03:52] So here we have mentioned the code to execute our for loops five times, but instead of five maybe if
[03:57] I try to mention ten, then in such scenarios the Producer and Consumer thread they are going to produce
[04:03] ten different elements and consume ten different values.
[04:06] I hope you are clear with the purpose of wait() and notify() method.
[04:10] We can also check the documentation very quickly.
[04:13] Here, let me open this wait() method.
[04:15] You'll be able to see causes the current thread to wait until it is awakened.
[04:20] So how it is going to be awakened, typically by being notified or interrupted.
[04:25] So if you see these wait() method is available inside the Object superclass longback
[04:29] when we are discussing about the objects, I told you that we're going to discuss about wait() and
[04:35] notify() related methods.
[04:36] When we are discussing about the multithreading concept, the same we are doing right now.
[04:40] So these wait() method, it also has some overloaded methods.
[04:44] If you want you can pass some milliseconds as well.
[04:48] Suppose if I pass 1000 milliseconds to my wait() method
[04:51] in this scenario, my current thread will only wait for one second.
[04:56] Then after that it is automatically going to be awakened
[05:00] once the time is elapsed or within these 1000 milliseconds
[05:04] if someone is invoking notify() method, then that also may cause the current thread to awaken.
[05:10] That's why here they mention causes the current thread to wait until it's awakened, typically by being
[05:15] notified or interrupted, or until a certain amount of real time has elapsed.
[05:20] Similarly, we can try to check the documentation of notify().
[05:25] So the purpose of notify() method is wakes up a single thread that is waiting on these objects monitor.
[05:32] Whereas if you have a scenario where you want to notify multiple waiting objects, you can use the notifyAll()
[05:39] method.
[05:40] So it is going to wakes up all the threads that are waiting on these objects to monitor.
[05:45] When I say objects monitor, we are running all these threads with the help of shared resource.
[05:49] So all the threads which are waiting using the SharedResource object to monitor all those threads will
[05:56] be awakened whenever we invoke that notifyAll() method.
[06:00] So whenever a thread transition from waiting state to awakened state, it is not going to immediately
[06:06] get the CPU time.
[06:08] It again has to enter the race of getting the CPU time along with the other threads.
[06:13] So the operating system it is going to provide the CPU time at later point of time, maybe after few
[06:18] fractions of seconds.
[06:20] Whatever we discuss around the wait(), notify() and notifyAll(() methods.
[06:24] I have mentioned all those details inside the slide along with these details
[06:28] I also mentioned the example that we have discussed for your reference.
[06:32] If you have any questions, you'll be able to find the code inside the GitHub repo.
[06:36] Please take the same code and try to execute them inside your local as well.
[06:40] You can also debug the program line by line to understand what is happening.
[06:44] We have any questions?
[06:45] Please post your question to me and I'll be able to help you.
[06:49] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

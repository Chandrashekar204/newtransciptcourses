# 4.36 — Deep dive on Heap memory and stack memory

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let me try to explain you about the Stack memory and Heap memory visually so that
[00:06] you can easily understand these complex topics. Like you can see here on the left hand side, I have
[00:12] a Heap memory in the circle shape.
[00:15] And very similarly I also have Stack memory, just like how we have plates arranged in a stack style.
[00:21] Here
[00:21] also, you can see I have a stack with a size of three, like one, two, three.
[00:26] With that quick understanding, let me show you what is happening here.
[00:29] Think like I'm trying to create these three new objects inside my main() method.
[00:35] So there are three objects e1, e2, e3 of data type Employee.
[00:40] Since the main() method is the very first method that is going to be invoked inside my Java program,
[00:46] the entry is going to happen at the bottom.
[00:49] If I try to invoke any other methods from my main() method, the entry is going to happen on top of the
[00:56] main() method.
[00:57] For now, let's assume inside my Java program there is only main() method.
[01:00] That's why the Stack memory has only one entry related to the main() method.
[01:05] So inside the Stack memory what are we going to store,
[01:08] we are going to store the local variables method parameter details along with the object references
[01:15] that we have created.
[01:16] When I try to create these e1, e2, e3 objects, these objects physically will be created inside my
[01:24] Heap memory.
[01:25] You can see there are three employees objects created and all of them have an objects reference with
[01:31] the name e1, e2, e3.
[01:33] So it is pretty clear that physical copy of the objects will be present inside my Heap memory, whereas
[01:40] inside the Stack memory where my main() method details are being maintained inside the Stack memory,
[01:46] the reference details of the objects like e1, e2, e3 will be stored.
[01:51] But please note that this is only reference
[01:54] details or the memory location details where the objects are originally stored inside the Heap
[02:00] memory.
[02:01] As soon as we are done with the main() method execution, this Stack memory entry will be removed.
[02:06] Along with that, the references details like e1, e2, e3 also will be removed from these Stack memory.
[02:13] We also discussed about the Garbage collector, which is going to take care of deleting the unused objects
[02:20] from the Heap memory.
[02:21] Please note that when the Stack memory entry is deleted, the objects are not going to be deleted from
[02:27] the Heap memory.
[02:28] Only the Garbage collector is responsible to delete the unused objects regularly or frequently.
[02:36] Behind the scenes
[02:36] it is going to keep on running as soon as a method execution is completed and the objects became unused,
[02:43] the Garbage collector is going to delete the objects from the Heap memory.
[02:47] So this is the story that is going to happen when we try to create the objects.
[02:52] Now let me show you what exactly is stored inside the Stack memory.
[02:56] In the previous lecture, I gave a very quick introduction about the Stack memory.
[03:00] With the help of main() method.
[03:01] This time let's assume a more complex business logic.
[03:05] You can see here I have a sample method invocation where method1() is trying to invoke the method2(),
[03:12] method2() is trying to invoke the method3().
[03:14] So here total we have three methods.
[03:17] Since the method1() is our starting method which we are going to invoke.
[03:22] It is the first entry inside my stack.
[03:25] After that, method2() is going to have its own entry, followed by method3() at the top.
[03:31] Always, the last method that we are trying to invoke will be at the top of the stack by following the
[03:37] principle of Last In First Out (LIFO).
[03:39] This method three entry will be removed as soon as we are done with the execution of the method3().
[03:45] Apart from these method details entries, you can also see there are also some local variables and object
[03:52] references.
[03:52] Inside the method1() we have created a boolean c, which is of type primitive data type.
[03:58] Since this is a primitive data type, its value along with the variable name is going to be created
[04:04] inside the Stack memory only, and similarly inside the method2(), we have two variables.
[04:09] One is y, which is an input parameter, which is again a primitive data type, and z is also a primitive
[04:16] data type.
[04:17] That's why we have y and z primitive data type entries inside the method2().
[04:21] Inside the method3(), we are trying to create a object of Employee with the variable name e1.
[04:27] So whenever we try to create an object, the same will be physically created inside the Heap memory.
[04:33] You can see there is an object created with his own details like firstName, lastName, age and gender.
[04:40] But the reference to this object is going to be maintained by the Stack memory with the variable e1.
[04:46] Always please note that local variables like primitive data types like c, y, z and similarly e1.
[04:54] All these variables is going to be maintained inside the Stack memory only because the life
[05:00] time of these variables are going to be restricted to the scope of that particular method only.
[05:05] That's why JVM is going to store them inside the Stack memory, whereas instance variables, which are
[05:11] going to help us to hold the data inside the object, they are going to be physically stored inside
[05:17] the Heap memory only.
[05:18] For example, this employee event object, they have some instance variables like firstName, lastName,
[05:25] age, gender.
[05:27] So these kind of instance variables which are present inside the object, they are obviously going to
[05:33] be stored inside the Heap memory because the object itself is saved inside the Heap memory.
[05:37] That's why along with the object, the instance variables are also going to be stored inside the Heap
[05:44] memory.
[05:44] Whereas local variables which we have created within the methods, they are going to be stored inside
[05:50] the Stack memory.
[05:51] So here even is a local variable because we have created Employee object inside the method three this
[05:58] event is not going to make any sense to the other methods, because this is completely local to the
[06:04] method3() only.
[06:05] That's why we have even reference stored inside the Stack memory.
[06:10] As soon as we are done with the execution of this method3() this event reference will be deleted
[06:16] from the Stack memory.
[06:17] And with that, this Employee object which is available inside the Heap memory is going to be eligible
[06:23] for the Garbage collection.
[06:25] I hope with this it is very clear for you what is Stack memory and Heap memory, method area and the class
[06:31] area is the memory where all our definitions of classes methods, static variables are going to be stored.
[06:38] Only the Stack memory and Heap memory are complex to understand.
[06:42] That's why I tried to explain them visually with these two slides.
[06:46] I hope you are happy with these explanation.
[06:48] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

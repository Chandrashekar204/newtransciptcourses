# 16.2 — Arrays have limitations

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] Are you going to live with a single goal throughout your life?
[00:03] Off course not
[00:04] your goals will keep changing from time to time based upon how you are progressing inside your life.
[00:10] For example, while you're studying in a college, you may have a goal to get a job in a decent company
[00:15] with a decent pay.
[00:17] And once you settle down inside this job, your goal may change
[00:20] this time, you may have a new goal like you want to buy your own car, or you may want to buy your
[00:26] own home, or you may want to get married and settle with your own family and children.
[00:30] This way, as you're trying to progress inside your life, the goals are going to keep changing from
[00:36] time to time.
[00:37] In the similar lines, when you're trying to build and run a Java program, the requirements from your
[00:42] program may change from time to time.
[00:45] Maybe initially, you might be under the assumption that your program may need only certain space to
[00:51] execute, but later on during runtime, your program may demand more space to store more new elements
[00:59] or more new objects.
[01:00] As of now, inside this course, we discussed about arrays.
[01:04] Using arrays, we can store any amount of data or collection of objects or collection of items, but
[01:11] with arrays there is a problem.
[01:12] Whenever you want to use arrays inside your program, you have to be very clear about your memory requirements
[01:19] of your array.
[01:20] For example, if you want to store ten different objects, then you need to be very clear about the
[01:25] same while you're trying to build your Java program later on during runtime.
[01:30] If your program is demanding more space inside your array, then in this kind of dynamic scenarios arrays,
[01:36] they are not going to work like you expect.
[01:38] They are not going to grow based upon your program requirements.
[01:42] I can also show you an example here.
[01:44] Think like you have started your own startup, which has its own mobile application and a web application.
[01:50] Inside your startup, web application or mobile application.
[01:54] You might have used Java because you are a Java developer.
[01:57] Initially, you might be under the assumption that your startup is not going to work,
[02:02] you're not very confident.
[02:03] That's why you have written a small piece of logic inside your web application, with an array that
[02:09] can hold up to 50 Customer objects. Because you don't want to waste memory unnecessarily
[02:15] by buying a big server, you just wanted to go with a minimum budget.
[02:20] So with the array that is capable of holding 50 customers, your program is going to work without any
[02:25] issues, up to 50 customers.
[02:27] But the moment the 51st customer is added into your application in such scenarios, definitely you're
[02:35] going to have a surprise from your arrays.
[02:37] They are going to throw ArrayIndexOutofBoundsException because inside an array which is capable
[02:43] of storing 50 customer objects, you are trying to add 51st customer.
[02:48] And since arrays can't grow dynamically, your program will fail.
[02:53] So to fix this issue immediately, you increase the size of your array from 50 to 100.
[02:59] This time
[02:59] also, you are not very confident that not more than 100 people will use your application.
[03:04] But to your surprise, a lot many people are liking your application and more and more customers are
[03:11] being onboarded into your application.
[03:13] So the story is keep repeating
[03:15] like every time you're trying to onboard more and more customers into your application, you need to
[03:19] continuously increase the size of the array.
[03:22] So with this, you may feel frustrated and you may ask a question yourself.
[03:26] Is there any alternative to this array?
[03:28] Should I live with this array with these pain points.
[03:31] So these kind of questions you may ask yourself or you may ask your friends or senior developers
[03:36] in the Java community.
[03:38] They will simply answer, saying that you don't have to live with these arrays.
[03:42] If you have a dynamic scenarios where the amount of size needs to be very runtime based upon how many
[03:48] objects you are trying to store at runtime, then in this kind of scenarios, we can go for the collections
[03:54] in Java.
[03:55] I'm going to give an introduction about collections in the next lecture.
[03:59] But before we try to close this lecture, let me also highlight you about other disadvantages that we
[04:04] have with arrays.
[04:05] We know one of the greatest disadvantage of arrays is they support only a fixed size.
[04:11] On top of that, whenever an array is getting created, they are going to be created in a continuous
[04:18] memory location.
[04:19] In future, whenever you want to add a new element, then in this kind of scenarios, your JVM is going
[04:24] to look for new space in the same continuous memory location.
[04:28] If it is not finding any new space in the same continuous memory location area, then obviously it has
[04:34] to move to some other location inside the heap memory where the continuous memory location is available,
[04:40] including with the new element.
[04:43] On top of this limitation, arrays also has another limitation, which is they are only capable of storing
[04:49] elements of a single data type.
[04:51] This means you can either only store the int numbers or String objects, or Person objects or Customer
[04:57] objects, but you can't store
[04:59] different data type objects within the same array.
[05:02] So all these limitations we are going to overcome with the help of Java collections.
[05:07] But before that, let's see one more example to understand the limitations of arrays like you can see
[05:13] here.
[05:13] Initially I have created an people array and inside this People array I'm trying to store the name of
[05:20] three different persons.
[05:21] Since I have provided three different names, the size of these array is going to be three with the
[05:27] index number zero, one and two.
[05:29] So once I have created these array, think like in the upcoming methods or in the upcoming lines of
[05:34] code, I have a different requirement which is to add one more person name.
[05:40] So in this kind of scenarios definitely I can't straight away go ahead and add a new name to the existing
[05:47] people array.
[05:48] Instead, I should create a new array with the size of four.
[05:51] Once the new array is created, I should copy the three names from the old array with the help of
[05:57] arrays.copyOff() method or with the other approaches that we have discussed previously.
[06:01] And at last I'm trying to populate a new name Sita at the index three.
[06:06] So if you see here these are very cumbersome or complex process that needs to be followed whenever we
[06:11] want to resize the array, as it is not going to grow automatically.
[06:15] So to overcome all these limitations, we have collections in Java.
[06:20] So let's start the journey of collections from the next lecture.
[06:24] Thank you,
[06:25] bye.

----------------------------------------

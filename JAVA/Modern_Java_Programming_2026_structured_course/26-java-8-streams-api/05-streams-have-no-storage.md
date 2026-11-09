# 26.5 — Streams have no storage

> Section 26: [JAVA 8] Streams API

[00:00] I'm going to show you a few images around the memory.
[00:03] First, let's try to watch them later on
[00:05] I'll explain the reason why I'm showing these images right now.
[00:09] So this is the very first image I have.
[00:11] This lady is climbing.
[00:12] I have no memory of it.
[00:14] Let's see the next image here
[00:17] the famous singer Shakira.
[00:19] She's saying the secret to happiness is no memory.
[00:22] So this also related to memory.
[00:24] Let me go to the next image.
[00:26] You can see this is an image from Men in Black movie. Inside Men in Black
[00:31] they have a special tool which can be used on someone with a flash.
[00:37] As soon as someone saw that flash, all their memory will be wiped off.
[00:41] I hope you saw this movie and you know about this.
[00:44] And the last image I have here around the image is again, this person is climbing.
[00:48] I don't remember a thing.
[00:50] If you see there is a pattern in all the images that I showed, so all the images are related to memory.
[00:55] Now let's try to understand why I'm trying to show this memory related images right now.
[01:00] The reason why I'm trying to show all these images is, I want to explain you about a important concept
[01:06] inside streams, which is streams
[01:09] they are not going to have any associated storage with that.
[01:13] You may scream at me saying that hey Madan, in the previous lecture itself, we have created a stream
[01:18] of objects with the help of collection objects.
[01:21] Then how come you can say that streams have no storage?
[01:25] So this can be your question.
[01:26] Don't worry, I'm going to clarify it.
[01:28] First, let's try to understand how the collections is going to work, how the memory is going to be
[01:33] handled inside collections.
[01:35] Later on we'll move on to the streams.
[01:36] So this is going to be super quick.
[01:38] Don't worry.
[01:39] First, if we try to understand inside a collections, we know all the data structures.
[01:43] It can be leased or it can be set or it can be HashMap or it can be a Map.
[01:47] So all these data structures, they store all these elements either in a sequential order or in some
[01:53] random locations.
[01:54] But at the end of the day, all the elements that we are trying to store inside an collection data structure,
[01:59] they are going to be stored inside the heap memory.
[02:02] So all these elements, they are going to be exist somewhere inside the memory.
[02:07] Once the addition of an element into the collection data structure is completed.
[02:12] So once an element is added into the collection object, as long as you're working on that collection
[02:17] object, all the elements of the collection, they are going to be hold in a memory location.
[02:21] And these collection elements, they are going to reside inside the same memory location until an element
[02:27] is removed from the collection data structure.
[02:30] So this is the memory story around the collections.
[02:33] Now let's try to understand about the streams.
[02:35] Like I said, streams
[02:37] they're not going to have any storage.
[02:40] This means streams does not maintain a collection of elements in memory.
[02:44] Instead of storing the elements in a memory location, what the stream objects are going to do behind
[02:49] the scenes is whenever we are trying to create a stream object, they'll try to have a reference to
[02:53] the memory locations where the elements are actually stored inside a collection object and post that,
[02:58] based upon the need bases, are based upon the demand they're going to pull the elements from the actual
[03:04] data source, like a List or an Array or a Set.
[03:07] That's why the way streams operates also is lazy.
[03:11] When I say lazy, it means think like a collection object has ten different elements inside it, and
[03:16] from this collection object you created a Stream object, and using these stream objects, you try to
[03:21] perform various kind of operations like filtering or manipulating the data.
[03:27] So when you're trying to perform all these kind of operations with a stream pipeline, so behind the
[03:32] scenes stream is not going to load all the elements, or it is not going to read all the ten elements
[03:37] at a time from the source.
[03:39] Instead, on the need basis are lazily it is going to load the element each one by one while it is trying
[03:46] to execute a particular operation.
[03:48] I hope now you are convinced with this discussion and accept the fact which is streams does not going
[03:54] to have any storage.
[03:55] But here you may have a question which is in the previous lectures, when you are trying to show you
[04:00] how to create the Stream object from the collection objects, we saw one of the approach, which is
[04:06] with the help of Stream.of() method.
[04:08] Let me show you the same here very quickly.
[04:11] So inside this example you can see I'm trying to create a Stream object with the help of Stream.of().
[04:17] To this of() method, I'm trying to pass the elements directly, whereas in the other approaches
[04:24] we are trying to invoke the stream default method by using the collection object.
[04:29] So in this scenario, this Stream object, it is going to refer to the elements present inside the source,
[04:34] which is departmentList.
[04:36] But here there is no source for my Stream object to refer.
[04:40] Since we are trying to feed the data directly to the stream, you might be thinking that in this kind
[04:46] of scenarios, stream might be storing these elements somewhere inside the memory, but that's not the
[04:51] case.
[04:51] Like I said, always the thumb rule these streams
[04:53] they are not going to take the responsibility of storing the elements.
[04:57] They are always going to be memory less.
[04:59] But
[05:00] let's try to understand what is happening in this scenario.
[05:02] So if I open this of() method, if you see here behind the scenes, based upon that data that we are
[05:08] trying to pass, they are invoking a method which is Arrays.stream().
[05:13] That means all the values that we are trying to pass to this tree method, they are going to be stored
[05:19] inside an array.
[05:21] So by the time this tree() method is getting invoked, all our elements are going to be converted into
[05:27] an array like you can see here.
[05:28] So from the Stream class we are invoking the stream() method available inside the arrays.
[05:33] So these values, whatever we are passing it is going to be converted into an array of elements.
[05:39] This means even in the scenario of Stream.of() where we are trying to provide the data directly behind
[05:45] the scenes was all these elements are going to be stored with the help of arrays, and once these elements
[05:51] are stored inside an array from the source array, my Stream object is only going to refer the elements
[05:58] on the need basis or lazily.
[06:00] This is a very important concept, guys.
[06:02] That's why I'm trying to emphasize a lot around these concepts.
[06:06] I see many developers.
[06:07] They know how to use streams API to process the elements inside a collection object, but they lack
[06:13] these in-depth understanding around the stream. Inside the interviews
[06:16] also, they are going to ask these kind of in-depth questions.
[06:20] That's why I'm trying to share this important information, so that you're going to be ready for any
[06:25] kind of interview questions.
[06:26] I hope this makes sense to you.
[06:28] Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------

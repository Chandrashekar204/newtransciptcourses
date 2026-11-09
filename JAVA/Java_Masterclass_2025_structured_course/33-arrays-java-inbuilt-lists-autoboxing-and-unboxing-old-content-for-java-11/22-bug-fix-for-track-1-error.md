# 33.22 — Bug Fix for "Track 1" Error

> Section 33: Arrays, Java inbuilt Lists, Autoboxing and Unboxing - Old content for Java 11

Now, as I mentioned in the last video there is actually a problem with the method as written this is the add to playlist method as you can see on the screen there, now the problem is the if statement this statement here on line 40 that's incorrect and that's because in the index always starts from zero, so consequently when we're running the program if we enter track number one, the index value will be zero and that's because one take one is zero so what will happen there in that particular test is that track one will not be recognized, in other words the album will come up and say the this album does not have a track one and that's obviously incorrect.

So what we need to do is make a simple little change and basically make the greater-than here to be greater than equal to. Once we do that it'll correct correctly identify track number one as it should have done in the first place, so that's that small little bug fix. So let's move on now to the next video.

----------------------------------------

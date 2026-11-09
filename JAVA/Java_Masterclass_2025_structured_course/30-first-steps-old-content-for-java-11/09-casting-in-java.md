# 30.9 — Casting in Java

> Section 30: First Steps - Old content for Java 11

So let's have our discussion now about arithmetic with these different data types. Previous videos, we did some basic arithmetic using integers, and we can do something similar with these other data types, as I've mentioned. And just as a recap, let's start by going back here and typing int myTotal is equal to, and in parentheses, myMinIntValue divided by two using the slash operator. So that's just a simple bit of arithmetic that takes the value of myMinIntValue, which of course is the minus 2.147 billion number divided by two.

No problems with that. Let's try the same thing with the byte data type. So byte, myNewByteValue is equal to, then parentheses, myMinByteValue divided by two. Now suddenly we've got an error. So why have we got an error? We know that if we use a literal value and the number fits, then there's no problem, and clearly here now, we now that we're using the minimum byte value divided by two, which clearly would fit normally in a byte data type. But here we've got an expression that uses a variable that's been divided by two.

That's the difference compared to what we've done previously when we've used a literal value. Well, the problem comes about because the default whole number used by Java is an int, and that's why I've got an error here. And to see that, if we hover over it, that really gives it away. It says required byte. So it's looking for a byte to store the value into our byte variable, but it's found an int. So basically what's in parentheses is treated as an int by the computer, and that's why we're getting this error.

But we know the expression will result in a number that fits, so how do we tell Java that? Well, we do that by using a concept called casting. So casting means to treat or convert a number from one type to another. So we put the type we want the number to be in parentheses, like you can see on screen. So we've got byte in parentheses in front of our expression, which in this case was parentheses myMinByteValue divided by two. And I'll note there that other programming languages have casting.

This is not just a Java thing. So to do that, then, we'd look at line 40. We'll come in here and we'll put our left parentheses byte, right parentheses and a space, and you can see the error has now disappeared. And because we've used this cast, we've told Java treat this value following the parentheses byte parentheses as a byte, and the error then disappears. And we're really being specific here in telling Java that this is a byte, so treat it as a byte instead of the default, which was an integer.

And we can do this, exactly the same thing for a short. So I'm gonna come down here, and I'll just scroll up a bit. So I can type short myNewShortValue is equal to, we can start by putting myMinShortValue divided by two. That gives us the same type of error, but this time it's required a short and found an int again. Using a cast we can do left parentheses short, right parentheses and space, and the error then disappears. So generally speaking, an integer is the whole number you probably wanna use, and you can probably guess that now because Java is using an int by default, and that's more or less telling us that that's what it's expecting to use most of the time.

So if you don't specify a type that you actually wanna convert to, then the integer is assumed automatically by Java, and you saw that in these cases, we got an error because of that. In the case of the code on line 38, we are using an int variable, and that's why I didn't have any problem with the result also being an int. So in general, my advice is to always use an integer unless you've got a really good reason to not do that. All right, so let's end the video here, and in the next one, it's time for a challenge to solidify some of the information you've learned in the last few videos.

So I'll see you in the next video.

----------------------------------------

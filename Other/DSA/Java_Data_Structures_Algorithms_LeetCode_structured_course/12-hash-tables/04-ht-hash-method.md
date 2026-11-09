# 12.4 — HT: Hash Method

> Section 12: Hash Tables

So now we're going to create our hash method. I'm going to bring up our graphic that we've been using to represent our hash method. And then we'll start our code out like this. Notice that this method is not public. It is private. And the reason for that is the hash method is only going to be used by other methods in the hash table class. So we're going to pass this a key. And the thing that we're going to return at the end will be this hash integer.

We'll start it out at zero. So the first thing we're going to do is take that key and put it into a char array. So we'll do it like this. So let's walk through what is happening on the right side of the equal sign there. We're going to pass this a key. Let's say the key is paint. So when we say two char array it is putting this into an array of characters of chars. Then we're going to have a for loop that's going to loop through that array. So inside of this for loop is where we're going to create our calculation.

So this is just going to be my version that I came up with. You could do anything here you want. But let me walk through the logic that I used. So we're going to start out by creating this variable called Ascii value. It is of type int. Now the thing that is interesting here is we're setting it equal to a char. So if you're not familiar with Ascii character values you can do a Google search for Ascii value table. And if you click on the first thing it returns you're going to get something that looks like this.

So notice down here I have the letter P highlighted. The letter P in Ascii has a numerical value of 112, and it has a different value than a capital letter p. So now let's flip back here. So for the first iteration of this for loop this variable Ascii value is going to be set to 112. So then we'll say hash equals. And I'm going to set it equal to hash plus the Ascii value 112. For the letter p we're going to multiply it by the number 23. So y the number 23.

The reason is that it is a prime number. And if you multiply this by a prime number, the number that you get is more random. So you could stick any prime number in here. Or you could just leave the prime number out altogether. And then comes the part where the real magic happens. We're going to use modulo and then data map dot length. And remember data map dot length in this case is seven. Our array has a length of seven. So when we say modulo seven what it's doing is it's giving you the remainder.

If you did division. So anything that you divide by seven is going to have a remainder of zero at the lowest end and six as the highest number remainder that you can have. So this will make it where our range is zero through six, and our address space just so happens to be zero through six. So this equation is always going to return a number that is one of the indexes in this array. So then after we go through this for loop for all of those characters at the end of this we will return hash.

And when we do return that hash, it is always going to be a number that is zero through six. And that is all of our code. For our hash method.

----------------------------------------

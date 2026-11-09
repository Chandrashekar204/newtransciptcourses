# 13.10 — Set: Longest Consecutive Sequence

> Section 13: <> HT: Interview / LeetCode Exercises

Now we're going to look at how we determine what is the longest sequence in an array. And specifically this is going to be the longest consecutive sequence. And the thing that really threw me the first time I saw this problem is the numbers don't need to be sequential in the array. It just needs to contain the consecutive numbers. So in this case 123, four, which means that the longest consecutive sequence is four. It's four items. So I'm going to put these back.

And to make this more efficient because we're going to be doing a lot of looking up by value. We're going to use the array to create a set. And remember sets don't have indexes but they're very fast when looking up by value. So we're going to iterate over this. We'll start with this first item 100 Hundred, and the first thing we'll do with that is check to see if the number before 100 is in the set. So if it was if 99 was in the set, we would completely skip over that 100 because we want to find the first number in that sequence.

And if the next number below 100 is in the set, that means that 100 is not the first number in that sequence. I'm going to change this back to 200. And because a 99 is not in there, we're going to say that the current streak is one. And then we'll look for 101. But 101 is not in the set. So I'll put that back. And that means our longest streak that we've seen so far is one. So I'll take our current streak, put it at zero, and then we move to here and we'll check to see is the previous number to four in the set.

And it is. And we only want to work with the first number in the sequence. And we know that four is not the first number in the sequence. So we're just going to skip it. And then we go to 200 and we look for the previous number which would be 199. And 199 is not in the set, which means that 200 is the beginning of a new sequence. So I'm going to change the streak to one. And then we'll look for 201. And that is not in the set. So that one only has a sequence a streak of one.

So now I'll put the current streak back to zero. And then we'll look at the one. We'll check to see if the previous number to one is in the set, which would be zero. Zero is not in the set. So we'll change current streak to one. And now we'll see if the set has a two. It does. So current streak is two. Now we look for a three. Current streak is three. We look for a four. Current streak is four. We look for a five. And it does not contain a five.

So the streak ends at four. So we'll update the longest streak to four. And we'll put these all back and change our current streak to zero. And then we'll look at the three. Is the previous number to three. In the set. It is it's the two. So we're not going to even look at the three. And two is the previous number to two in the set. And it is. That's the one. So we're not going to look at this one. And now we've gone all the way through our set.

And our longest streak is four. And this is what you return at the end of the method. And that's how you use a set to very efficiently determine the longest sequence.


########################################

# 5.5 — LL: Binary to Decimal

> Section 5: <> LL: Interview / LeetCode Exercises

Now our next coding exercise is called binary to decimal. So you'll be given a linked list that looks something like this. And with binary all of the numbers are either going to be 0 or 1. So in this case this binary number with four ones would be equal to 15. But I know there's going to be a lot of people that are fairly new to binary, or they might have a basic understanding of it, but I want to talk about it a little bit deeper and talk about the pattern that we have with the numbers.

And in order to explain this, we're going to start out by treating this like a decimal number. So in decimal this would be 1111. And we know that this is worth one. This is ten. This is 100 and this is 1000. And the main thing I want to focus on here is the pattern. As we go from right to left, we start with that one and we go one to the left. That number is ten times as big. We go to the left again, and that 100 is ten times as big as the ten. And then of course, the thousand is ten times as big as the 100.

And the reason for that is each digit has ten possibilities. It's zero through nine. And because there are ten possibilities, this goes up a multiple of ten each time. And you can take all of these and put them together. And that gives you the number 1111. And let's put this back and let's say the one inch the 100th spot. We're going to change that to a zero. This becomes a zero and this becomes 1011. So now let's look at this in binary. And the main thing I'm wanting you to get is the pattern.

Because we're going to need to use this in our algorithm to solve this. So these are the numbers in binary and in binary. Instead of going zero through nine you're only going zero through one. There are only two combinations. So as we move from right to left the one doubles and becomes a two. The two doubles and becomes a four. And the four doubles and becomes an eight. And if you go through and add all of these up, they add up to 15. So it might look like all we need to do is have something that points to the first node and we take eight plus four is 12, plus two is 14 plus one is 15.

But here is the problem. You will not be given the length of the linked list, and you're not allowed to iterate through and calculate the length. So when you start here, you have no idea that this is an eight. This could be a 16, it could be a two. You're not going to have any idea of the actual value of this node. So I'm going to put this back. And so what you might want to do here is pause the video and see if you can figure out how to do this.

So now I'm going to walk through how to solve this. When current is pointing to the first node. We're just going to assume that the linked list has one node. And in this case that node has a one. So we'll say that the entire linked list is worth one. But then we're going to iterate current and go to the second node. Well, if the linked list has two nodes, that means that first node was actually worth two, not one. And we had stored this one up in the upper right.

That means we need to take that one and double it, because that's what we had stored for the first node. And then we're going to add the value of the current node. So we're going to add the one of the current node. And now it's three. And you can see that we have a two and a one. And that adds to three. But then we go to the next node. And we had stored this three to represent the first two nodes. But you can see that they are worth four and two now which add to six.

So we need to double that 3 to 6 and then add this one and make it seven. So the first three nodes are adding up to seven so far. But we have a fourth node. Now these three nodes are adding to 14. So we need to take that seven and double it to 14. And then we'll add the one and it's 15. So I want to emphasize something here. I'm going to remove this last one. And remember the linked list was worth seven at this point. If we were to add a node that was a zero, we would still take all of these and double them and make them 14.

But we're going to add the actual value that's in the node in this case zero. And in this situation this linked list would be worth 14. And that is the overview of the strategy for how to solve binary to decimal.

----------------------------------------

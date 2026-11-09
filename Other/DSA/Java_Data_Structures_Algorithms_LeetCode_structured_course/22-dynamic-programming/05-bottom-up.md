# 22.5 — Bottom Up

> Section 22: Dynamic Programming

When you're doing dynamic programming, your solution can either be top down or bottom up. When we did this recursively, it was top down. That is to say, the first thing that we looked at was the highest number. Then we moved down until we looked at fib of zero. But when we do it iteratively, we are doing this bottom up. We look first at the smallest numbers and then we start working our way up. So let's put this in an array. And once again I'm going to bring back our recursive solution.

When we did this recursively we started by looking at the index of seven. We started on the right side of the array. Now when we do this iteratively we're going to start on the left side of the array. Or you could say the bottom side and work up. So we'll start our iterative code out like this. So the first thing that we'll do is create an array. And the size of the array will be n plus one. So if we want to find fib of seven we're going to need an array that has eight spots because it is zero through seven.

And that is why it is n plus one. And we're going to create a new array every time we run this. The next thing we'll do is populate those first two spots in the array with a zero and a one. And then we're going to have a for loop. Notice that index starts at two. And the reason for that is the first open index that we need to fill is the index of two. Also notice this is less than or equal to n because we have to go up to and including the index of seven.

So now we have to add the values at index of zero and one. And put that at the index of two. Will do that with this line of code. So we're going to say fib list at index. And for this iteration of the for loop that's going to be two. At the index of two we're going to set that to be equal to the values at index minus one and index minus two, which is going to be one. Did we iterate through the for loop again? Now index is three and when we add the values at index minus one and index minus two, that is going to be two.

Then we keep iterating through the for loop until we get to the index of seven. And that gives us 13. So now we want to return that value of 13. We'll do it like this. We'll say return five less at the index of n, which in this case is the index of seven which returns that 13. So the big O for this is O of n minus one. So the index was seven. And we iterated through the for loop six times. But of course we'll simplify this and drop the non-dominant.

And this becomes o of n. So now let's take this code and we'll do the same thing we did in the last two videos and add a counter. And will increment this inside of the for loop. So now let's flip over to IntelliJ and take a look at this. So there is the code that we just wrote. And then I'm going to scroll up. And I'm doing the same thing here that I did in the last two videos, where I start out with n being equal to seven. And I'll run this. So fib of seven is 13 and the counter is six.

So now I'm going to come up here and change this to 40. Remember when we did this recursively without memoization there were over 300 million method calls. And when we do this bottom up, we have 39 method calls. So you're able to do this very efficiently by either doing this recursively with memoization or doing this iteratively. Now there's one more thing I want to point out about doing this iteratively bottom up. So I'm going to flip back when we look at the code the way that we have written it here, we're going to iterate through the for loop until we get to the index of n.

And then we return the value at the index of n. And as we discussed this is going to be o of n. But what if we want to find fib of seven a second time. Well the next time we run this these three lines will be the first thing that we run, which creates a brand new array that looks like this. Then we have to iterate through the for loop and populate that array. So the second time that we run this is also going to be o of n. So the question you might have is can we use memoization and preserve these answers just like we did with the recursive solution.

And the answer is yes. If you used memoization the second time you ran this and you ran fib of seven, the second time would be O of one, because we could just pull that value out of the array. But generally with an iterative bottom up solution, we don't do it that way. There is a downside to using memoization. And that is you have this array that is in memory. You're using up memory space. To be able to get a better time complexity. And when you do this iteratively, you have a pretty good time complexity of O of N.

So to simplify this and to not use the extra memory space, generally we don't use memoization in each additional time you call. This will also be o of n. And that's why we're going to leave our iterative solution just like this. And when we do dynamic programming iteratively, remember that is also known as bottom up.


########################################

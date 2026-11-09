# 2.11 — Big O: Wrap Up

> Section 2: Big O

So now let's wrap up big O. So I'm going to bring up our graph here and say n is a hundred. Let's look at what each of these four are when n is 100. So we start on the bottom there with o of one. And that's going to equal one. O of log n is going to be approximately seven. O of N is going to be 100 because n is 100. And O of n squared is 10,000. So you can already see that there's a very big difference between each of these. And that O of n squared compared to the other three is very inefficient.

But this spread becomes even bigger. When n becomes larger. So let's look at what happens when n is 1000. Oh of one down at the bottom, there is going to still be one. It's not affected by N becoming larger. O of log n is approximately ten because two to the 10th power is 1024, so 1000 is pretty close to that. So we'll call that approximately ten. But notice it only went from 7 to 10, even though n went from 100 to 1000. O of n is going to be a thousand, and O of n squared goes all the way to a million.

So as n grows. N squared is going to grow very, very fast. It's very inefficient compared to any of these others. So we'll see as we get into the course, there will be situations where you do something and it's O of n squared. And you can rewrite the code and make it O of n. That is a huge increase in efficiency when you can do that. So now let's look at some terminology for all of these. O of n squared is a loop within a loop. O of N is proportional, it will always be a straight line.

O of log n. Divide and conquer. When you hear that that is O of log n and o of one is constant time. So those are our four terms for our four big O's that we'll see for most of the course. So now I want to flip over to a website. This is called big O Cheat sheet.com. At the very top of the page you have this chart. These two over here were not going to see in this course. In fact o of n factorial the one all the way to the left. There is something that you would have to intentionally write bad code to achieve.

The worst one that we're going to see in this course is going to be O of n squared, which is in the horrible category. And we'll make our way across here. O of n times log n. Remember we're going to see this in a couple of sorting algorithms. And then down here is where we want to stay with these three o of n o of log n and o of one. So below the chart if you scroll. They have common data structure operations. So you have a variety of data structures on the left there.

And this whole area is time complexity and it's broken into average on this side. Notice these all start with the Greek letter theta. And then worst on this side, this is going to be. Oh, but also over here we have space complexity. And this just has big O for space complexity, not omega or theta. And you can see that except for one, the skipped list, which we're not going to build in this course, they're all O of N. And this is one of the reasons we're going to spend much more time on time complexity than space complexity, because in the entire data structure section, all the space complexity is going to be the same.

So then if we scroll again. You have array sorting algorithms. And this has best with omega average theta worst O for time complexity. And then the space complexities are all over the place. And this is where we will talk about space complexity. And one of the things that's interesting is quicksort and merge sort up here at the top for the most part is o of n times log n, but the space complexity is not the best. Whereas you get down here we're going to build these three bubble sort, insertion sort and selection sort.

And you can see the time complexities for the most part are not good. They're O of n squared. But all three of them have a space complexity of O of one. So these three are considered to be, shall we say, primitive sorting algorithms. But from a space complexity they're great also and a best possible scenario over here. They are more efficient than quicksort or merge sort. This situation, by the way, is if you have already sorted data or almost sorted data, then it's going to be in.

And that's also the situation up here for quicksort when it has its worst possible scenario. So let's say you have sorted data or almost sorted data. And that could happen if you have a sorted list and you add one item to the end and then you're going to sort it, it is almost sorted. Or it could be that that item on the end is the highest number and it's completely sorted. Quicksort is going to be terrible in a situation like that. But bubble sort and insertion sort are going to be very good.

So these are the kinds of questions that you're going to get in an interview. This is why you have to know the big O and for that matter, the theta or the omega, in this case for the time complexity and understand the space complexity to be able to answer these questions. But also, I would encourage you to go to this website and spend some time looking this over. After you start getting an idea of how this works in the course, I will add a link to this website in the resources for this video.

And that is our wrap up for big O.


########################################

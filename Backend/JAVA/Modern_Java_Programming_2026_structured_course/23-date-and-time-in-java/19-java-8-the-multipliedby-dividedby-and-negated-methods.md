# 23.19 — [JAVA 8] The multipliedBy(), dividedBy() & negated() methods

> Section 23: Date and Time in Java

[00:00] We are able to add and subtract date and time values and Duration and Period values with the help of
[00:08] plus and minus methods.
[00:10] In the similar lines, we also have methods that supports multiplication, division and negation.
[00:16] So these methods are available with the name multipliedBy(), dividedBy() and negated().
[00:21] But these methods don't apply to the date and time objects as they represent specific points of time
[00:28] on the timeline, and it is also not going to make sense.
[00:31] Suppose if I take today's date, and if I'm trying to multiply with two or 3 or 4, what should be the
[00:37] output?
[00:37] So it's not making sense.
[00:39] That's why these multiplication, division, negation, they are not going to applicable for date and time
[00:44] objects.
[00:45] Instead we can use these methods on top of the objects of Duration and Period.
[00:51] Like you can see here we have the code snippet.
[00:53] If we have a duration in your hand, you can multiply that with the help of this multipliedBy() method,
[01:00] dividedBy() method and negated.
[01:02] The same applies for the Period object as well.
[01:05] I'm going to show you the demo around these in few seconds before I show you the demo
[01:09] please note that that these methods are particularly useful when you want to perform some simple arithmetic
[01:16] operations on top of Duration and Period objects, such as scaling a duration or period up or down by
[01:24] a factor, or changing the direction with the help of negated() method.
[01:28] All these methods, they are providing a convenient way to work with time based intervals and adjust
[01:35] them according to your requirements in a clean and readable manner.
[01:40] I hope you're clear.
[01:41] Let's see the demo of these methods very quickly. To show you the demo
[01:44] first, let me try to create a new Java class with the name MultiDivNegateDemo.
[01:52] So these are random class name that I'm trying to choose here.
[01:56] Inside this class, let me create the main() method post that I'm going to create that Duration object
[02:02] with the variable name as original duration. To this variable
[02:07] I'm going to assign duration of 30 minutes by invoking these ofMinutes() method.
[02:12] And to this I'm going to pass the input as the t.
[02:15] With that, we are going to have the duration as PT30M, so m indicates minutes here.
[02:21] Now using this object, I can try to perform the multiplication operation by invoking the multiplied
[02:28] by to this multipliedBy() method.
[02:30] If I pass the factor as three this 30 minutes, it is going to be converted into 90 minutes.
[02:37] And with that we are going to get the output as 1H30M the same
[02:42] I can try to confirm by catching the output on the left hand side with the variable name, which is
[02:48] multipliedDuration.
[02:50] In the similar lines, let me try to invoke the dividedBy() method.
[02:55] So if I invoke that dividedBy() method and if I pass the factor as two, this 30 minutes is going to
[03:01] be divided by two.
[03:03] And with that we are going to get the output as 15 M the same
[03:07] I can try to catch inside a variable with the name dividedDuration, and at last I can also try to
[03:15] invoke the negated() method, which is going to change the direction of our duration.
[03:20] As of now, you can see we have plus 30 minutes as that duration.
[03:24] But with this negated() method we are going to get the output as -30 m the same I can catch inside a variable
[03:32] negatedDuration.
[03:34] Let me keep a breakpoint here and try to execute this program.
[03:38] You will be able to see under the original duration we have 30 minutes.
[03:42] Later on when we try to multiply with the three, we are getting the duration as 1H30M and when
[03:48] we try to perform the division by factor two, we are getting the output as 15 M and with the negated
[03:54] operation we are getting the output as -30 M.
[03:57] I hope you are clear on how to use these methods with the help of Duration.
[04:01] Very similarly, we can also use these methods by using the Period objects.
[04:07] I want you to pause this video and try these methods on top of a Period objects.
[04:11] I'm going to wait for you.
[04:13] You can press the pass button and with that you can make me wait for some time.
[04:17] I hope you are successful with your assignment around the Period objects.
[04:21] If not, don't worry.
[04:22] Let me show you very quickly how to do the same.
[04:24] What I'm going to do is I'm going to copy all these lines of code and paste it here and replace duration
[04:31] with the period.
[04:33] So in all the places I'm going to replace Duration with Period very quickly.
[04:37] And here instead of off minutes I'm going to invoke ofDays() method. To these ofDays() method
[04:43] I'm going to pass three days as an input.
[04:46] And with that we are going to get the period as P3D.
[04:51] Post that this variable
[04:53] I'm going to update two oirginal period, the same original period I can use in all these places.
[05:00] You can
[05:00] with the Period object
[05:01] we cannot invoke the divideBy() method because it is not supported.
[05:05] It is not going to make sense to divide the days with a factor.
[05:09] So that's why this operation is not supported.
[05:12] We can only perform multiplication and negation whenever we are trying to deal with the Period object.
[05:18] So let me update these variable names to multipliedPeriod the same here
[05:24] also I can mention which is negatedPeriod.
[05:27] So with this we are going to get the output as P9D.
[05:32] And here we are going to get the output as P-3D.
[05:37] So let me execute this program to confirm the output.
[05:40] You can see first we have period of three days.
[05:42] Later on based upon our multiplication it converted to nine days and at last based upon our negation
[05:48] operation the Period object holds minus three days.
[05:52] I hope this makes sense to you.
[05:53] Please use these methods whenever you are looking to scale up or scale down your Duration or Period
[06:00] based upon a given factor.
[06:02] We also have negated() method to change the direction.
[06:05] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------

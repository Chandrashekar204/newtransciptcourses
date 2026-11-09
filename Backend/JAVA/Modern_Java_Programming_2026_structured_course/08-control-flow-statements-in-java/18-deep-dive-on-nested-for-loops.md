# 8.18 — Deep dive on nested for loops

> Section 8: Control flow statements in Java

[00:00] Just like how we can write nested if blocks and nested while statements.
[00:05] Very similarly, we can also build nested for loops based upon our business requirements.
[00:11] Inside this lecture, I'm going to show you a demo of nested for loops.
[00:15] For the same, let me create a Java class with the name NestedForLoopDemo inside this class.
[00:23] First, as usual, we need to create a main() method.
[00:26] Once the main() method is created, I'm going to write an nested for loop.
[00:30] This time, the requirement that I have is to print that tables 1 to 10 by multiplying up to that ten
[00:39] multipliers like I want to display one table,
[00:41] two atble,
[00:42] three table .
[00:42] four table.
[00:43] 5, 6, 7, 8, 9 ten tables.
[00:47] So in each of the table I want to multiply that table number up to that ten multiplier.
[00:53] So in this kind of scenarios I can safely use nested for loop.
[00:56] Let me show you how to do that.
[00:58] First I'm going to declare an int variable with the variable name number.
[01:03] And to this I'm going to assign the value ten, because my requirement is to display that table numbers
[01:09] up to ten.
[01:10] So first I'm going to write a for loop.
[01:13] This for loop I can say it is a outer for loop.
[01:16] Inside the outer for loop I'll mention int i = 1, followed by i less than or equal to number,
[01:25] followed by i++.
[01:28] So this outer for loop represents the number of tables that I want to print.
[01:33] Like initially I'm going to print the one table followed by two
[01:37] table three
[01:38] table, four table.
[01:39] By the time my variable becomes 11, this condition will become false and the outer loop will stop execution.
[01:47] So that's what I'm trying to achieve with the help of this outer for loop.
[01:51] Now inside this for loop, I'm going to write one more for loop with the help of this inner for loop,
[01:57] I want to multiply each table number with its multipliers, like when my outer loop started,
[02:04] the initial table number is going to be one to this one table,
[02:08] I want to multiply with the multipliers like one, two, three, up to the 10. For the same,
[02:13] first, I'm going to declare a variable int j = 1, followed by j less than or equal to
[02:21] number.
[02:22] And after that I'm going to increment that j by one using the post increment operator.
[02:28] So let me introduce curly braces here.
[02:30] Here the nesting is done up to the two levels.
[02:33] But if needed I can do the nesting up to any level.
[02:37] I can introduce one more inner for loop inside the second for loop.
[02:40] So it's up to me based upon my business requirements.
[02:43] But with these two nested for loops, I should be able to solve my problem.
[02:48] So inside the inner loop I'm going to write an System.out.println().
[02:53] With the help of this println() statement, I'm going to display the table details along with their multiplier
[02:58] and the result.
[02:59] So what is the first variable I need to mention?
[03:01] I need to mention i because I represents the number of the table followed by
[03:07] I'm going to mention
[03:08] plus, since I want to do the String concatenation this time instead of asterisk, I'll try to use a
[03:15] small x so that it is going to look exactly like inside our mathematics books.
[03:19] Like one into one is equal to one, one into two is equal to two.
[03:23] So that's why I'm trying to use this small x here.
[03:26] And after that I need to mention the multiplier value.
[03:30] So what is the multiplier value variable
[03:32] it is the j.
[03:33] So I need to mention the j followed by plus symbol
[03:36] and after that I'm going to mention double is equal to.
[03:40] And at last I need to mention the result.
[03:43] So each time this inner loop executed the result, we can get by multiplying i * j.
[03:50] So let me mention i * j.
[03:53] So if I try to execute this program, you'll be able to see the tables right from one table to that
[04:00] ten table.
[04:01] If something is not clear don't worry, I'll try to debug this for loop and try to show you what is
[04:06] happening.
[04:06] So let me keep a breakpoint at multiple places.
[04:10] So if I try to start this program in a debug mode very first time, the breakpoint is going to stop
[04:16] inside my outer loop.
[04:18] So the outer loop right now has a value one inside the i variable.
[04:22] So for the one table the inner loop is going to be executed ten times because we have defined j <= number
[04:31] .
[04:32] So what is number,
[04:34] number is ten.
[04:35] So when the inner loop executed ten times using the same number one the multiplication is going to perform.
[04:42] That's what we are going to see inside the console.
[04:44] So let me try to mention this step over this time
[04:47] you can see the j is one.
[04:49] So i * j we are going to get the output as one.
[04:52] So let me try to press on this F8 multiple times,
[04:55] you can see the inner loop is keep executing multiple times till
[04:59] the j becomes 11, so as soon as the j becomes 11, the inner loop execution completed.
[05:07] Now the execution will go to the outer loop.
[05:10] This time the outer loop it is going to be incremented by one more value.
[05:15] And that's why the i number is going to become two.
[05:19] Even for the two, the inner loop is also going to be executed multiple times.
[05:24] I hope you are clear.
[05:25] Let me remove these breakpoints and resume my program.
[05:28] And inside the console we should be able to see the all the tables up to that ten number.
[05:34] Now let me show you one more example of the for loop.
[05:37] This time with the help of inner for loops, I'm going to display a pyramid or triangle with the help
[05:43] of asterisk symbol.
[05:45] Let me show you how this pyramid or
[05:47] triangle is going to look like you can see this is how we want the output.
[05:52] In the very first row
[05:53] we want only one asterisk, followed by
[05:55] in the second row we want two asterisx followed by three, four, five.
[05:59] So we want total five rows.
[06:01] And each of the row we want the asterisks equal to the row number.
[06:06] So to display the same pyramid I'm going to write an nested for loop inside my Java class.
[06:12] So here first let me create a variable with the name rows and assign a value five.
[06:18] Since my pyramid structure has total five rows, I have defined the rows as five.
[06:24] After this variable name, I'm going to write the outer for loop inside the outer for loop,
[06:29] first I'm going to declare a variable which is int i = 1, followed by i <= rows.
[06:37] .
[06:38] And after this I'm going to mention i++.
[06:42] After this outer for loop I'm going to write one more inner for loop and inside the inner for loop,
[06:48] also I'm going to create a variable with the name j.
[06:52] And to this I'm assigning initial value one, followed by I'm going to write an expression which is
[06:57] j less than or equal to i.
[07:01] So why I have chosen I because with the help of these inner for loop only, I'm going to print the asterisk
[07:08] symbol for each row.
[07:10] This inner for loop has to be executed based upon the current row number.
[07:15] So if you see here in the first row we have only a single asterisk, followed by
[07:19] in the second row we have two asterisks.
[07:21] That's why the inner for loop I want to control with the help of these condition, which is j <= i
[07:28] .
[07:29] And post that I'll just mention j++.
[07:32] And at last inside this inner for loop I'm going to mention a simple System.out.println().
[07:38] And with the help of this I'm going to print asterisk symbol.
[07:42] So with this my inner for loop is going to print the asterisk symbol based upon the current row number.
[07:49] So if my row number is two then this inner loop is going to be executed two times.
[07:54] Once my inner for loop is executed completely.
[07:58] After this I just wanted to mention System.out.println().
[08:02] The reason is after completing the inner loop execution completely, we want the cursor to move to the
[08:09] next line before the next row printing started.
[08:12] That's why I'm trying to simply mention println(),
[08:14] println() will move the cursor to the next line.
[08:17] So if I try to execute this program, we should be able to see the same pyramid symbol.
[08:22] But unfortunately we are getting a different pyramid symbol.
[08:26] Let me see what is the issue inside our program?
[08:30] The issue is we have used the println here.
[08:33] Instead we should use the print.
[08:35] If we use a print, the cursor is not going to move to the next line, so we should not use the println()
[08:40] inside the inner loop.
[08:41] This time I should get the correct output.
[08:44] You can see we are getting the correct pyramid structure.
[08:48] If you want to display the pyramid structure with the row number ten, you can simply update this value
[08:53] to the ten and you should be able to see a beautiful pyramid structure with the total ten number of
[09:00] rows, and inside each row we are printing the asterisk symbol based upon the row number.
[09:06] I hope you are clear on how to build a nested for loop inside the real projects you will see lot
[09:12] many times you will have lot of scenarios to use the nested for loop.
[09:16] That's why I'm putting enough efforts to explain about these nested for loop.
[09:21] If you closely observe these nested for loop, like I said, I'm trying to use the variable like i, j
[09:27] if I have one more nested for loop, then I'm going to use the k.
[09:30] So like this
[09:31] developers are used to the tradition of using I, j, k, l to a great extent.
[09:38] I would also recommend you to follow the same, because I don't want you to put into an embarrassing
[09:43] situation instead of I j k l.
[09:46] If you use some other characters or variables, I'm sure the other developers they are going to look
[09:51] you with a surprised look.
[09:52] I have few memes also around this, but before I try to show you those memes, let me highlight that
[09:58] these two examples that we.
[09:59] We have discussed as part of nested for loop.
[10:02] I have mentioned inside the slides as well, so please always refer to them if you have any questions.
[10:07] Now let me show you the funny meme images around the full loop very quickly.
[10:13] This is the first funny image that we have around the loops.
[10:17] Like you can see here, the developers are scared to use the do while loops.
[10:22] There is no reason that they are scared to use the do while loop, it's just that the developers will
[10:27] not have enough scenarios to use that do while loop.
[10:30] That's why even inside the real projects
[10:32] also, you will rarely see developers using that do while loops.
[10:36] Now let me show you the next funny image.
[10:39] So this is the funny representation of the for loop.
[10:42] So the for loop is going to start with the i variable zero.
[10:47] And it is going to execute up to the i value four.
[10:50] So i is equal to zero, i is equal to one, i is equal to 2, 3, 4.
[10:55] I think this i is equal to five should not be there.
[10:57] If this has to be there, then the condition should be i less than six.
[11:02] So someone prepared the funny image about the for loop with a defect.
[11:06] So hooray!
[11:06] we identified a defect inside this image.
[11:09] But the message from this image is pretty clear that if multiple people is trying to cut the cake at
[11:15] same time, it is a kind of for loop.
[11:17] Let me move to the next image.
[11:19] You can see the tension that developers are going to go through whenever they're trying to build a for
[11:25] loop, they're not sure whether they want to use i j k because developers think that these are the only
[11:31] valid characters to use as part of the for loops.
[11:35] But like I said, there is no hard rule that we need to use this.
[11:38] i j k this just a funny representation of tradition that we have as part of the for loop.
[11:44] On the similar lines, I have other images like developers, they always don't like to use other letters
[11:51] while building the for loop.
[11:53] They always like using i character or i letter for their for loops.
[11:58] So let me go to the next image.
[12:00] And this is one of the funny representation that for loop always like to use i variable, but not any
[12:07] other character.
[12:08] So whenever someone is building a for loop, they'll always give the first preference to the i character.
[12:13] I hope you like this image.
[12:14] Let me go to the next image and you can see this image conveys how embarrassing it is going to be if
[12:21] someone uses other than i character as part of for loop.
[12:25] Now let me go to the last image.
[12:27] Here you can see developers
[12:29] they would always love to start the i variable initialization with the zero.
[12:34] So both these for loops will have the same effect.
[12:36] Someone started i is equal to one they have used less than or equal to, whereas inside the second for
[12:42] loop we have declared i is equal to zero.
[12:45] But we mentioned i < n, so they both have same effect.
[12:49] But developers, they will always like to start from zero and they'll mention i < n.
[12:55] So this is the most preferred way for the developers because we as a Java developers used to the starting
[13:02] position always as zero long
[13:04] back when we're discussing about String, I said the first index is always going to start at zero.
[13:10] The same applies for arrays and collections.
[13:12] With that tradition developers, they would always try to initialize a variable as zero inside for loop,
[13:19] but there is no wrong if you start with one.
[13:21] But in that scenario, you may have to use <= instead of < n.
[13:28] I hope you like this discussion.
[13:29] Thank you and I'll catch you in the next lecture bye.

----------------------------------------

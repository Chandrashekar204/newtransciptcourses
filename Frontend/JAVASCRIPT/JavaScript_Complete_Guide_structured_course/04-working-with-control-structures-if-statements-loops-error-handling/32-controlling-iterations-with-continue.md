# 4.32 — Controlling Iterations with "continue"

> Section 4: Working with Control Structures (if Statements, Loops, Error Handling)

The continue keyword is a bit like break, it also stops the current execution of this code in your loop but it doesn't stop the entire loop, so instead it just moves on to the next iteration. I can best show how it works, here in the console if we add a quick for loop here, a normal for loop with i equal to zero, i smaller than 5 and i++ let's say, curly braces and then shift enter to write some code between, and now of course if I console log i here, unsurprisingly we print 0 to 4.

Now press the up arrow to be able to edit this again and now let's add a little if check in there where we check if i is equal to let's say three which is one of the values we're printing here. If that's the case, for whatever reason I don't want to print it here, well then of course we could use break, right, this will stop the loop execution. If we hit enter, now we see 0, 1, 2 but we don't see 3 but also not 4 because we cancelled function execution with break.

This might or might not be what you want because I actually only wanted to skip this three value, I didn't want to cancel the entire loop execution and that's exactly what continue does. If you use continue instead of break, you just skip this loop iteration, so all the code after continue will not be executed but for the next iteration it will continue as normal, so it will not break out of the loop, it just continues to the next execution. So if I now hit enter here, we see 0, 1, 2, 4, we don't see 3 because there we continue and as I said, this means this code is skipped for this loop iteration, subsequent iterations like the 1, 4, 4 are executed.

So break and continue give you some extra control over your loop execution, you definitely don't need them in every loop you write but sometimes, you have some code where you want to break out of a loop up on some condition being met or you want to skip an iteration based on some condition and then break and continue are your friends.

----------------------------------------

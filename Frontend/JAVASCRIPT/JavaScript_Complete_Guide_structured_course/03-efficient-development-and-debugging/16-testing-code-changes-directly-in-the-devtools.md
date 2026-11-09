# 3.16 — Testing Code Changes Directly in the Devtools

> Section 3: Efficient Development & Debugging

So now that we're able to find the error, let's fix it and let's say we think we know what the problem is but we're not sure yet. Of course we can always go back to our code and change it here and reload the page and try it again but you can also change your code here in the sources tab. There we have the suspicion that fetching our user input is the problem, so that this is a string instead of a number. So we could add parseInt here, like this to see what whether that does the trick.

Now you just have to save this by pressing command or control save so that the star disappears up there and you get a warning that this only was saved locally, so only here in the browser, not to your filesystem, so the code we have here still is untouched. If you go to get user number input here, you'll see that's untouched. So you don't change your local code but you change it here in the browser so that you can test changes here in the browser without facing the danger of changing your real code and maybe breaking things there.

So now if I add five again, now this is looking better because now you see this is not getting concatenated but instead, this really changes here at the end, it really adds five as a number. So now that we validated this fix, we can just take it and bring it to our real code and then apply it here, save and now reload and now we have the code we wrote and now we see this is now really working the way it should. So this is how we can work with the debugging tools.

Now you've got more tabs up there, we'll explore them later in the course, for example the elements tab once we work more with the DOM and the performance and memory tab, these are tabs I'll dive in later once we optimize performance and memory usage of our application. For now, the sources tab, breakpoints and the console here, these are your bread and butter tools for finding and fixing errors.

----------------------------------------

# Variable Scope

*Section: Advanced Jenkins*

1 So I mentioned before in the functions lesson 2 about variable scope, that we can do something up here. 3 And I'm going to use a shorthand for environments, 4 and we do something like def myNumber, 5 and set it to equal 123. 6 Now that will be available inside this pipeline block, 7 so I could use it down here. 8 The catch is it won't be available to myFunc. 9 So what I'll need to do is pass it in as a parameter.

10 And likewise, I can, inside myFunc, define variables. 11 So I could say define myName = myText. 12 And that's fine, but likewise, 13 that variable is only available inside this function block. 14 And this is called variable scoping. 15 One place it can get even more extreme, 16 and again, this is where engineers 17 sometimes really get caught out, 18 is we've seen before with the script block 19 that we might have inside here 20 if statements and else statements.

21 And what you can do in here 22 is even define variables in here. 23 So we do def myNumber again. 24 And what's the catch here? It's all about that scope. 25 This variable is only available inside this stage. 26 That's it. It cannot be used anywhere else. 27 And it sounds absolutely crazy, right? 28 That you can't then go ahead 29 and create another stage and use that variable. 30 Unfortunately, that's one of the limitations 31 with Groovy and Jenkins, and that is variable scoping.

32 So if ever you run into an issue and you're not quite sure 33 why some variables are working and some aren't, 34 definitely check out the scope. 35 Have a look at where you've defined it. 36 If you want it to be available on all stages, 37 then use the environment block. 38 This, in other words, makes it global. 39 If you want to use it in a function, 40 you're going to have to create a parameter to pass it in.

41 And there we go. 42 That is variable scoping, 43 and that will hopefully save you a lot of time 44 and a lot of pain when things don't work. 45 And I've seen it before where you'll define it, 46 and it'll be in the stage, and you'll go, 47 "Why isn't my variable working? Why isn't it accessible?" 48 And likewise, you'll define it at the top, 49 make it global, and you'll start wondering, 50 "Okay, why can't I use it in myFunc?" 51 Sadly, this is one of the limitations of Jenkins, 52 but now you're aware of it, 53 it's going to save you so much time.

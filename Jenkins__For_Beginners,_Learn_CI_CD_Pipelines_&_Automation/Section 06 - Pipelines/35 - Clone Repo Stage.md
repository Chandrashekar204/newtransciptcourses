# Clone Repo Stage

*Section: Pipelines*

1 So now what we're gonna do is type in stage, 2 again, in brackets, and we're gonna put "clone repo," 3 and again, normally, as I said before, 4 like in that GitHub repo when we saw it, 5 that you'd have a Jenkins file in there and the code 6 or files you wanted to build inside. 7 We're doing it slightly differently 8 by creating our own pipeline, 9 so we are going to need to clone down the repo.

10 Again, inside brackets, then add steps, 11 again, also in brackets. 12 So what we're gonna use now is another function called SH, 13 and what this does is it runs the shell for us, 14 a bit like in our first job, when we ran a Bash shell, 15 this does the same, and we denote it by using SH, 16 but in double quotes, we put what we want to execute. 17 So now, if we go back over to our browser, 18 go over to this repo, and again, I'll include a link to it, 19 click on clone or download and then copy it.

20 You can either double click inside and control C, 21 or you can click on this icon here, 22 which will copy it to your clipboard, 23 and then paste in the repo, 24 and before there, what we need to do is type in "git clone." 25 Now, let's work on the next stage of our pipeline.

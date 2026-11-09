# 40.11 — Challenge

> Section 40: Basic Input & Output including java.util - Old content for Java 11

So as I mentioned in the last video, it's time for a challenge, and the challenge is to rewrite the static initialization block that you can see on screen now using the try with resources that we've talked about and discussed in this section instead of the try finally code that we've actually got it here in place now. So pause the video and go away and convert this static initialization block into using try with resources instead of try finally.

And when you're ready to come back and check my solution start the video, so pause the video now. Okay. So how did you get on. Hopefully, you got the try with resources working. Let's go through now and get this set up. So what we need to do first is we're obviously in locations.java and we're in the static initialization block. I'm going to delete this first slide. We no longer need that anymore. Instead what we're going to do is put the code in the try block so we're going to come up here try and we're going to set up the scanner in the little in the brackets, scanner equals new scanner, new file reader locations and it's called big.txt, like so. And you can delete that line there because we've effectively done that on the previous line.

And we come down to leaving uh coming down to catch io exception we're going to leave that in place but we're going to delete the final block now because of course the closes now happens automatically with the scanner as we've talked about in previous videos. So that's that. That's the first one. Now the next time we're going to read the exits we need to do a similar initialization. So we come up to the start here scanner scanner equals new scanner.

This one's a new buffered reader. I guess, we could have just copied the line below, new buffered reader then it's new new file reader and it's directions. Let's call big.txt. So delete the next line now. Then again down to the finally we're going to delete the file because that's no longer needed no longer needed because it's automatically closed. So we just run this to confirm that it still works. Let's go say north south west and quit, so that's working okay.

So. That's the challenge. But just before I finish the video, you may have noticed that we actually stopped needing a scanner to read the exits when I change the code to read a line at a time and split it. So removing the scanner is actually quite easy. So what we can do is come up here to line 57 and get rid of the scanner all together. Instead make that buffered reader files equal to new buffered reader then get rid of one of the brackets, get rid of the scanner because of course we're no longer using that.

Then we're going to set up a string,so string input we can change the while now to be while input equals dir file dot read line.equal to null. We can delete the string input now because that's now been changed on line 59. And again I just wanted to say this isn't part of the challenge. So this is just an optional extra step that I'm just showing you at the end of the video. So don't think that you've missed out and I haven't told you how to do something with the challenges or just an extra section given that we weren't really using this scanner anymore it made sense to actually remove that.

So now that I've done that, we could have actually done that at the same time as I stopped using the scanner for parsing the data, but the buffered reader class closed method throws an unchecked exception. So I would have had to have caught that in the final block as well, so that's the reason why I didn't do that any earlier. But now that we've actually converted to the try with resources, so it's a simple change to make. All right. So that's actually it. That's the challenge over. Actually before I go, let's just run it to make sure that it still does work, obviously very important.

And let's try up, down, we'll go west, up and quit. That seems to be working fine. Okay this time. I'll see you in the next video.

----------------------------------------

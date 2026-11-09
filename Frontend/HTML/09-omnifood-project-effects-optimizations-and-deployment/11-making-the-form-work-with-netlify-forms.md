# 9.11 — Making the Form Work With Netlify Forms

> Section 9: Omnifood Project – Effects, Optimizations and Deployment

Narrator: So the last thing that we're gonna do here is to use the Netlify forms feature in order to make or sign up form work. So here in the menu of your site, So right now, remember our site or mine here it's called Omnifood-Jonas. And so right now we are in the site settings but here we have all these other things. And one of them is forms. Right? So here we see that we can manage forms and submissions without any server site code or any JavaScript.

And so that's what I mentioned also way back, which is that usually we need some code on some backend server site basically to then receive form submissions. But here a Netlify can basically do that job for us. So all we need to do is to add a name to the form like this and add the Netlify attribute, and that will be it. All right? And of course, this will only work if you deployed your site using Netlify. Right? But that's pretty obvious, I guess.

But anyway, here is our form. So the action we don't need in this case. But instead we need a name. So the name attribute on the form let's call it sign up, and then the Netlify attribute. So this is of course not a standard HTML attribute but simply when we upload the file, Netlify will then see that we added it and will then automatically start accepting submissions for this form. Now, in order to make this work, we also need to add a name attribute to each of these input fields.

And the name attribute is actually a standard HTML attribute for form inputs. So actually we should have done that earlier because even when we write our own server site code to accept the form submission, we still need that name because that is how we will then identify each of the input fields. So let's call this one here full name. So let's give them here a descriptive names because these names are actually what are going to appear in the Netlify dashboard.

So here, well here we can simply call it email as well. And yeah, here, let's also just give it the name with the same description as the ID. So name, just like this. Now, okay, and that's actually it. Now, just one important piece of advice here is that you should never use a Netlify form to handle real signups with passwords, or the same thing for logins. So Netlify has actually a separate feature for that but that is paid, and I did never use it.

But you cannot, or you should really not submit passwords through this. Alright, So really just something like a contact form or something around those lines. Alright. But anyway, we just prepared our form here. And now we of course need to deploy this one more time. So we need to submit the code basically again. And so for that, we come here to deploys. And then here we have again that area where we can simply drop our folder. So let's do that again.

And so you see that now we have a new deployment going on so it's still uploading. It's not done yet, so let's wait for it, Wow, that's taking a bit too long. That's strange. Now, so actually it is already done Alright, now our form here will still look the same of course but if we inspect it, then that attribute should be there. So actually it is not. And so what that means is, that Netlify did already change our HTML here a bit. So you see that even this method here of post I think that we don't have it in our code.

So. Right, you see that. So we don't have method post. And so Netlify, they added this part here. Okay? And so now let's try to fill this with something. Let's try my email here. And finally then let's say YouTube video. So sign up now and well, Netlify then takes us to this thank you message and we could also customize this. So basically lead the user to our own custom page. But well, that's just too much work for now. So, we can just go back and now in our Netlify dashboard that submission should be here in forms.

And indeed here we get active forms, which is called Signup which is exactly the name that we gave it here. And so if you had multiple forms on your page, then you would of course have to give them different name. But anyway, let's now click here and then we will get that submission that we just made. So you see we have the full name that I created, the email and also where did you hear from us? So Netlify even takes this text here from our labels, which is really, really helpful.

Right? So you can then also download these results as a CSV file. But just one thing that I wanted to make clear here is that you can only take 100 submissions per month on this form. So what that means is that if you have a lot of traffic then at some point you might have to sign up for a paid plan if you want to keep using the form. And if you want to get ahold of form submissions right here into Netlify. Okay? But if you just have a couple of visitors and just want to use this, let's say for fun then you can use the free version still and get up until 100 submissions.

And as you see, this is really really easy to do and can become quite handy alright? And with this, let's now close it up because now a project is indeed finished. There's nothing more we can or we should do. And yeah, so we've come a really long way here together and I hope that you're just as happy as I am with how this project ended up. So congratulations once more. And of course, make sure to share this with all your friends and make them maybe a little bit jealous.

So anyway, take care, and I see you next time.


########################################

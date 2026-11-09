# Discover Additional JavaScript Functions in n8n

*Section: JSON, JavaScript & Data Manipulation - Go Beyond Basic n8n*

In the previous videos of this section, we covered all formats of functions we have inside Nadine. So we've covered string, number, array, object, and boolean. Um. However, there are additional functions that are pretty useful to use. I use them and basically this video will be kind of like a bonus to our functions we have inside Nadine. So right away let's start with the function that I use almost every day.

And it's dollar sign now. So basically what it does, it returns for you the time, the exact date of um, when like this, um, code snippet is triggered. So let's say you are triggering some automation. Like I use it basically to give AI, um, like the date background, what's the time of this automation being triggered? And then, um, we can just based on it and just maybe retrieve some information or do other stuff.

So how it works, it returns for you the exact date with the hour and it changes, as you can see right here. Uh, also we've got another function which is called today, but you only return with, with this function today's date. But with now you can do a lot of crazy things. So basically you can type two date time. And now um, actually for example, what you can do, you can type format and then just retrieve the specific day along with for example, let's say um, here, hour and minutes.

I believe it's this way. Yeah. So we can just return this specific date and it's totally great. The format is pretty cool. And yeah, it works this way. Additionally, you can perform a lot of different actions. So for example, I believe we can click on plus or no. Um, maybe we can do it this way. So we've got a date and um, yeah, we can just click on plus just provide this specific function. Maybe let me return.

Okay. So I've got the format, uh, which is this one? Um, okay. Uh. What's wrong? Okay, I've got this format, and now I can type here plus. Plus. Uh, perfect. Click here on dot. And basically what plus allows you to do is to add certain amount of something. So let's say I can add seven days to the date. Okay. And now uh, seven days. Um, let's see what's wrong. Okay. I need to provide the apostrophe right there.

Yeah. And now I've got seven days. I can provide seven hours. I can, let's say seven months. So it will be another, uh, basically year. Um, also we can minus this is another option. You can minus and now you will have oops. Now we will have another date. So as I said, when you know, uh functions how to use them, you can provide multiple functions at once. So I've got here now to date time minus format.

And basically I can provide endless and functions here. Um until it makes sense obviously. Um, but maybe let's, let's go back here. Let me show other functions when it comes to the time. Um, so if I go here, I provide a dot we've got here minus plus uh, different to extract and a lot of functions. So set set set locale set zone. Um, so here you can set your very own zone as you can see here. Let's see what we have.

So let's say UTC UTC plus two. Well it works. Yeah it works plus three plus four plus five six whatever. We can set the zone. But what I mean with the time we've got a lot of different functions. So maybe let me cover, um, different tool and now maybe let me clean the data. So basically what I can do here. Let me provide some date. So maybe 808 2025. And here maybe let me remove the format. And now actually you can see like difference between I believe it's August 12th, 2025.

And there we've got a time which is um, which is August um, 16 and 16th. Okay. So the difference is four days. However, we can provide also the hours in that specific case. So -111 hours. But to make it more clear. So let's put it in the apostrophe. Uh, I should work. Yeah. So now what we have, um, let's say we've got 11th. So 24 days, I believe. Yeah, 24 days. Um, is it this way? Uh, okay. Yeah, it works this way.

All right. So basically, you you just return the difference between these two dates, like in this, in this kind of way. And the next parameter is if and it's super useful. So if we go here uh, we provide like the dollar sign if it works like an if node. So basically inside if you can provide the specific condition so we can go ahead and type. If now let's say um dot day um is bigger than um 15 then return I don't know maybe.

Hello. But if no uh, return goodbye. Okay. So basically it works this way. You've got other examples right here. So it works like an if node if something this is the condition. If something is let's say bigger you can type. Maybe it's not equal I believe it's this way. So exclamation mark and and actually, um, yeah, a question mark. If it's, if it's not equal 15, then go ahead with the true value which is hello.

If it equals 15, um, if it doesn't equal 15 okay. Then go with the value. If it equals 15 then go with goodbye if that makes sense. Today we've got 16th. So now it should provide goodbye. Yeah it works this way and it's super useful. Um, you can provide multiple conditions, but, um, I wanted to show you that you can do it also with JavaScript function, not only with the node you're using every time.

Probably next function, which I really love is json.stringify. So basically if you go here, um, you provide the dollar sign, you go ahead and let's say we just return, um, our object, um, basically what we do, we just turn our object into a string. Let's say I want to take an array. The entire array and turn it into a string and feed it to ChatGPT. I can do this. And it's a string. Let's say we've got maybe we have the variable with a lot of like a variable in an array form with a lot of information.

Then we can turn it into a string and just feed ChatGPT with it. We don't need to like, like do some crazy things like, I don't know, maybe go to the code node or just to set edit fields node. Um, just we can do it with this single code snippet. So Json.stringify. And actually it's pretty the same as the function that um, is. Let me show you. We go JSON and now um to JSON string. So it's the same.

And this is the same function. So we can use both of them. Next what we have we've got actually max and minimum okay. So if I go here I provide some numbers one, two, three, four, five, six. And we provide a dot max. Then it returns the biggest value. Um, likewise, if we go ahead with minimum, it returns the minimum value. Afterwards we have the function which is workflow. And by using it you can return the workflow name workflow ID or if it's active or not.

Uh, I don't know, maybe it's useful for you. It's kind of sophisticated. Uh, but by this way, you can return the workflow information in the last function, which is extremely useful, is the function that returns for you all information from the specific node. So if I go ahead here I provide a dollar sign. I open the brackets and I provide the apostrophe I click on edit field. So I provide here the name.

And let's say I would like to return all of the information I have. I type all and then I return everything okay. Basically I can also provide first. And for that case, it won't do anything because actually we've got only one item. But let's say if you have ten items, then it returns the first item. Also, when you provide last, um, it returns the last item. Um, but also it's useful, um, when you actually have multiple items.

So let's say 10 or 15 or even 100. But basically if you would like to return all the information from the specific node, you provide a dollar sign, brackets, apostrophe, the name of the specific node, and then all first or even last. And that we have it right now we are at the end of learning JavaScript functions inside this section. I hope you enjoyed it. You enjoyed the time together with me. I had a lot of fun and I can say JavaScript functions are really important in terms of just simplifying our work, just working faster.

And for sure you may not be using code inside Nadine. However, if you are not a Kodi person, you are not. Um, actually, you don't have the experience. Also remember you can learn this, um, code snippets or even after this section, you know that you can search them inside an addon and use them right away. So maybe, as I said, I encourage you to know 5 to 10 code snippets, JavaScript functions that you will be using all the time.

But for the rest you can go ahead to documentation and then just read it. Um, but the main point now you know that some functions even exist. So then afterwards you have the specific circumstance. You just can recall yourself. Okay, I've covered it. I can do it this way. Just go ahead to do documentation, search how to use it, or even just go back to the specific section and just recall all of the information we've covered here.

Thank you so much for this time. And as usual, I will see you in the next video.

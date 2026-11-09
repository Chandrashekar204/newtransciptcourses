# Create an AI Agent That Tracks Your Finances

*Section: Business & Support AI Agents*

Tracking our finances is really important, so why wouldn't we create the entire automation that handles the entire process? Therefore, in this video, we'll be creating this project and which is very simple, that handles actually our expenses and income. And now with all that being said, before creating that, let me show you how it works. So we've got two different automations inside one workflow. And now we can open the chart because this is the trigger.

And here let's say I can type I bought a car for let's say $12,000 at I don't know, 16th of May. All right. Let's run it. And now the entire automation runs. And afterwards the data should be saved inside here. So here we've got description, car purchase cost, date and expense. Also let's say. All right. Yeah. Um, at um all right. Let's say 1st of May. I received $1,000 from my from my side hustle.

Let's actually run it and see what happens. So here we've got the cart car purchase. And now let's see. Let's wait. All right. We've got here the in comma which is different type of actually of actually amount. So there we've got the cost here we've got 1000. However it's the income. And in this video we'll be creating this automation. So with all that being said I'm actually let's get started and let me show you how to create it.

So first things first let's start with the trigger which is actually on a chat message. So whenever we've got, um, our new message inside the chat, we would like to trigger this automation right away. What we can do we can go ahead to our agent. So let's provide our agent here and there what we want to do here. And the options we would like to add the system message. And now in general, let me actually copy my message that I have here.

So you're a helpful assistant. You are used to save expenses or income. Always refer to 2025 year. All right. And then also we can add an option so max iterations and which is free. All right. And now what we can do we can go over there and open the chart. And for yeah for actually setting up the entire automation we need to provide a trigger. So sample message. And there I can type I bought a let's say a bike for $1,200.

All right. At let's say June 16th. Okay. We can just run it and see. All right. So this data now is as provided there. And now we can provide the model which is OpenAI. Um, let's go over with OpenAI. Um, here GPT four or mini. And now it should work again so we can run it. Um. Let's see. All right. So as you can see right there, we've got our output. So it works. Nevertheless, we can also add the memory.

So our agent knows, um, what we typed in the past. Right. And here, for example, let's type the five. And also we can go over and add the tool that will allow us to call another workflow. Because here in general. Um, yeah. We'll be right there. I'm calling the next, um, yeah. The next automation right here that will save for us the data. And now inside what we can do, we can name it as the expense, um, database.

Database. Base and here actually provide a description. So call this tool to save the expense. Um expenses or income to database. That's right. And there we need to provide the workflow. So from which workflow we would, we would like to trigger um like take the um like the parent. Um automation. All right. So here let's go over and provide ID and now go over to the URL and copy this entire ID so I can just paste it here.

Um we can click back back to canvas. And there what we can do we can go over. Close the chart and now provide our um yeah. Our second automation that will save the expenses or income inside Google Sheets. So let's add the note and there type X execute. All right. However here we would like to go ahead to triggers and click when executed by another workflow. And there what we actually need to do. However, before let's add the last step which is edit yeah which is edit fields.

Um it's not necessary. However I would like to add it. So here we can type the response. And there we can map it as the response response and also provide here the variable from there. So when I run it I can see I've got the response which is response. I bought a bike for $1,200 at June 16th. All right. So it's not necessary. However we can add it to make it just better. Nevertheless, for now, let's go over here.

And what we need to do in general for testing purposes, um, we need to set up mock data. Afterwards, we'll change it and we'll connect like this to, um, automations together so they will work nevertheless for now. Before that, we need to provide our custom data. And now what we can do? Let's delete it. Let's provide here the curly bracket and do it by this way so we can provide right now the query query.

All right let me write it. Query colon. And there what we can do we can provide here inside collocation. Um all right um let's save it firstly and um take the data from here. So from the chart let's open the chart. And there let's take this data. So we'll be using that for setting up the entire workflow. And then I will just delete it. So again let's go over there and here again do this stuff. So query inside the quotations.

All right. Here provide a colon. And there again provide the quotation mark and just put it here after we do this and we saved it. Um, and then you can see we've got our query, so we can just pin this entire note. And afterwards what we can do, we can go over to our extractor extractor. Information extractor. And there and we can just separate these specific fields. So there we'll have actually our description.

So and we bought we bought a bike there. Um the cost and also the date. So what we can do we can go over here and provide the following data. So firstly we'll have the description. So convert expense to JSON. All right. And then we need to just provide the query from our trigger. So here um afterwards what we want to do um we want to add our attributes. The first attribute will be cost and this is the number.

And here we can add the description. So expense cost or income actually or income. Then we can enable that as required. We can provide another attribute which is description. We can leave the string and add expense or income description okay. Then we can enable that again as required we can add attribute which is the date. So here date of the operation. And at the end operation. Uh yeah. Be sure you didn't misspell anything and click required.

And at the end we can provide the type. So type of the operation. All right. This is a string. And this is even either expense or income. Yeah, and now we can run it. So we've got a problem. A model subnet must be connected and enabled. All right. So here we need to provide our model I forgot about it. So there let's provide the OpenAI model here GPT four or mini. And now let's again test the step.

So let's actually click here and see. All right so we've got the cost description date and expense. It's nice. All right. What we can do. Else we can go over here and add our step for Google Sheets. And there we can provide up and row and sheet. And here in general I prepared for you the template. And that actually you can download from the resources of this material. And in general you will have here the link.

You can click on file and you can click on make a copy a copy. All right. So then after you do this is. You go over here to document and you pick my expenses template there. You just click sheet one and you just connect the description. So here description cost date. And lastly let's provide a type. And let's test the step and see if the data is fulfilled inside our Google Sheets. Yeah. So we've got a description I bought a bike cost date and type.

And now that's pretty it. Now we need to do something very important. Firstly let's go over and save actually this entire workflow. And now what we can do. We can go over here and then we can unpin the data. All right. And we can provide accept all data. And then we can again save it. So now what it will do. It will save actually map all of these parameters and actually variables from here. And then it will just um, you know, work as a whole.

Let's go over here. Click click reload. And now let's provide open chat and let's test it out. So here I bought a bike for let's say not a bike, maybe a, uh, maybe flowers for $20 on May 14th. All right, let's run it and let's see if that works. So here, as you can see. Uh, yeah, it's connecting to our second automation. So there when executed by another workflow, let's now click on the Google Sheets and see what flowers $20 date and type.

So we've got here the expense and that's pretty it. Afterwards you can just chat with your model. And they're just you know it's simpler than just going here to Google Sheets and just um, yeah, fulfilling all of the brackets and so on. For me it's much better. So there for an example here you can type. Mhm. I earned let's say $2,000 um on June let's say first you can just type it there. Wait for the model.

So let me show you. And there you should have the income actually you've got um do you have the income. Um, no. All right. What's what happened actually here? Um. All right, we didn't provide, um, their the specific case from my work. All right, let's go ahead and, um, let's run it from my, uh, work. Um, I earned from my work $2,000 on June 1st. Let's see how it works. Um, well, we have that. We've got the income, so you need to just specify that it's very important and you need to provide all of the details.

And that works. Again, let me actually show you. I received $1,000 from my side hustle because otherwise we don't have the description. All right. From my side hustle up on June 12th and let's go over here again. Let's provide that and we'll get the income. Let's wait. We've got the income. And now lastly let's provide another case. So I bought a what we can buy I bought a computer for us I don't know $2,000 at on.

Um yeah September September 23. Let's run it. And this is the last example for now. So you see the real data and how it works. We've got the expense. And there where do we have that. Um we've got here the computer. Where do we have the computer. Um let's see, I bought a computer for 2000 on September 23rd. Um, for a computer. All right. We bought a computer. So it takes some time. Um, actually, to perform, however everything works.

You can even go over here actually to executions and there, see how it performed, what it provided. And for sure, the system works perfectly. Uh, yeah. That's it. In this video, we build our expense tracker. And remember, you can download the template in the resources of this material so you can just, you know, import this into your workflow and then use it. It's really useful. It's very nice to build.

So I hope you enjoyed this automation and I will see you in the next video.

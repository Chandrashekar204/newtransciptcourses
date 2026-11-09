# Use Built-in Ask AI Feature in Code Node + Chat with N8N Docs Assistant

*Section: JSON, JavaScript & Data Manipulation - Go Beyond Basic n8n*

Hi there! Something I didn't mention in the previous tutorial is the built in Sky feature that team recently added to the code node. This is actually really cool and can save you a lot of time. As you can see here, when you open the code node, you'll notice there are two tabs code and Sky. I think it's also good for beginners who want to learn how JavaScript works in Ie10 without leaving the platform.

If you need more help, you can click on the help button in the right corner to open the documentation. So this takes you to the official documentation about coding with GPT. Here you can see they give you a complete overview of how to use this feature. How to use it effectively. So they explain the limitations like the fact that it's only available for cloud users, not self-hosted instances. They also mentioned that Python is not supported, on JavaScript.

Also really important to mention I generated code overrides your code. If you have already written some code on the code tab, the AI generated code will replace it. So Nathan recommends using AI as a starting point to create your initial code, then editing it as needed, so you need to keep it in mind. Now the documentation includes some really helpful tips for writing good prompts, so let me walk you through the key sections here.

So first first they emphasize providing examples of your expected output. So instead of just saying format the data, you would show exactly what format you want. Like we did in the previous tutorial. So this helps the AI understand exactly what you are looking for. They also they also mention describing your processing steps in sequence. So if you want to fit the data and then sort it you would say first, filter out all users under 18, then sort the remaining users by their last name.

So this step by step approach gets much better results. Another important tip is avoiding ambiguities. So instead of saying something vague, be clear and direct to ensure that you get the most accurate code. So instead of saying get all the users, you might say Twitter users who are 60 years old and above. Now scrolling down, you can see some practical examples that shows you exactly what kinds of prompts work best.

So the first example shows you how to find data inside datasets. So if you have slack data and notion data and you want to match them by email address, there is a specific prompt that shows you how to ask for that. In the second example, this example is data transformation. Like taking a list of usernames and combining them into a single comma separated line with quotes around each name. So this is exactly the kind of thing we did in our previous tutorial.

Now the third example. So this example shows you how to create a formatted slack messages by counting different types of submissions and listing the top ones by votes. This presents how you can combine data analysis with text formatting in a single prompt. Now what's really useful is that each example shows both the prompt and the actual JavaScript code that get generated. So you can see the pattern on how to structure your request.

There is also a section about referencing data explicitly using dot notation. So if you have nested data, you can tell the AI exactly where to find the information it needs. As we could see here. Tell AI what you want the to achieve. You can reference input data fields using dot notation for example user dot email. Now this is something really cool. You can click on this chat with the button at the bottom.

And this opens up an intense documentation assistant where you can ask for. You can ask specific questions about any ten features. You can use this for troubleshooting when your code is not working, or if you want to dive deeper into documentation, for example, to explore some concepts and features, or for learning more about anything in general or specific functions, and so on, you can chat with the documentation.

I think this is really cool because this bot is specifically trained on the official docs. So instead of searching through through pages of documentation manually, you can just ask your questions here and get accurate answers based on the documentation. So yes, you can use this ask feature in the code node. I think it might be really useful for some scenarios and use cases.

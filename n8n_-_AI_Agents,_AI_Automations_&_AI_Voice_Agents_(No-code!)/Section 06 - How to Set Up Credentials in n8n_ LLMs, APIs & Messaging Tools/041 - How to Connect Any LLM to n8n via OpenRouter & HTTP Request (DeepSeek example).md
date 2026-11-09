# How to Connect Any LLM to n8n via OpenRouter & HTTP Request (DeepSeek example)

*Section: How to Set Up Credentials in n8n: LLMs, APIs & Messaging Tools*

Using it as a chat model to your agent, or making direct HTTP requests to Leipzig for specific tasks. So let's walk you through both methods. First is add the OpenAI chat model. So search for OpenAI. By default this points to OpenAI, but we will redirect it to Leipzig using the base URL. Next, go to open router and create an account. Once login, look for the DB six v3. And you will need the base URL.

So click on API. And copy this base URL. Go back to. And paste it here. Next we need to replace the model name with Db6 specific identifier. So copy the model name from. Leipzig Leipzig. Chart. Switch to expression and paste it here. Now we have to set up credentials. So go back to open router. Create API key. Create key. Give it a name. Create. Copy your new key. Go back to N810 and paste it here.

Now save. Don't worry about this message. It's just a bug. Everything will work fine. Now you can test the chat model. So click on the chat. You can ask it anything. Really. I ask it to write me a LinkedIn post about agents for small businesses in 2025. And as you can see, it's pretty good. Remember we did not provide any prompt to our agent. So we can achieve a lot better output. Now we will set up deep in HTTP request node.

This method allows us to send prompts to seek and retrieve responses dynamically. So go to the deep sitcom. Create an account sign in and go to API platform. This will bring you to the API settings and here you can see your usage details. I just added two bugs for testing and it will go a long way. You will be able to process millions of tokens. You can top up your account using PayPal or debit or credit card.

We need to create a new API key. So go to this section. Create new API key. Name it and copy it somewhere secure. You will need it for authentication. At HTTP request nodes to your canvas. Import curl. Paste it here. Click on the import. This will automatically set the method to post. Add the correct endpoint and pre-fill the required headers. So scroll down. And in the header section replace the placeholder.

With your API key you generated earlier and make sure there are no extra spaces. It should look like that.

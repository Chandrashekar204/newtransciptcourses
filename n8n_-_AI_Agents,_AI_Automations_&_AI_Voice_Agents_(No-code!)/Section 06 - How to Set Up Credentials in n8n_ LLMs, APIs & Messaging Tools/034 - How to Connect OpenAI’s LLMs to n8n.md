# How to Connect OpenAI’s LLMs to n8n

*Section: How to Set Up Credentials in n8n: LLMs, APIs & Messaging Tools*

Today, I'm going to show you how to connect OpenAI models to your AI agents in N810 in just a few minutes, so you can build your first agent. We'll cover how to generate API keys and set up credentials so you can use models like GPT four or GPT for mini voice models and embeddings. Models. First, we need to add the AI agent to our canvas. On the canvas, click the plus button and search for AI agent.

Now you can choose between different types of agents. For now, let's keep it simple and stick with the truth agent. So now let's configure the AI agent. Scroll down. Click on add option. And you will see an option for the system message. So this is where you tell the agent how it should behave. For example, you can start with something simple like you are a helpful assistant. Next we need to choose our chat model.

So let's click this plus button. Let's search for OpenAI chat model. So we can scroll down. It's the last one. So now we need to connect our agent to one of the OpenAI's powerful models. So to do this you will need to set up credentials. So click this little pen. As you can see we need API key to set up a connection. So head over to OpenAI. Com forward slash API. Create an account and login. When you first create an OpenAI account, you receive $5 of free credits.

Valid for three months. Now click on settings. Under the usage section. You can see how many tokens you have used and how much you have left. This helps you keep track of your usage. Now navigate to API keys section on the left hand side. And click on Create New Secret key. Give it a name for example Nathan demo. Select project can be default project and hit create secret key. Now copy your API key.

Go back into N810. And place it right here. Itself? Yes. That's great. Now we are successfully connected. So now. Let's add a memory. So the agent can remember previous messages thanks to this node. And finally, let's test it. So click on chat. And now you can ask agent whatever you want. For example. What's. The capital. Of Thailand. Yes. That's it. You only need to go through this process once, as your credentials will be saved and used in other workflows.

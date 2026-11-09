# How to Connect LLMs to n8n Using Grok Fast AI Inference

*Section: How to Set Up Credentials in n8n: LLMs, APIs & Messaging Tools*

In this tutorial, I'm going to show you how to integrate large language models like Deepsee R1 using Grog's fast AI inference. In the case of Deepsee Karen, it's actually faster than using their official API platform and even supports tool usage, which is pretty cool because Typekit R1 is designed as a reasoning model, so it was built mainly for complex problem solving tasks. When you are using it through their official API platform, or by using operator or even self-hosting it on your own machine, you will likely run into errors when trying to use tools with your agents.

I would not recommend using it to call tools directly. You can still get the best out of it by combining it with models that do support tools like GPT four or cloth. Think of Leipzig or one as the brains of the operation is great at planning making decisions, while another model takes care of two based tasks like API calls or data lookups. So just for the sake of this video, I've created two simple agents.

In the first one, I've connected Leipzig, or one through grok, which is a fast AI inference platform. I will explain how it works and how you can connect to it in just a sec. And in the second agent, I'm using deep seeker one through open rotor. So I'm using the exact same model. So it's called Leipzig or one distilled llama 70 b. And the same in the second agent as our chat model. In both agents.

I have connected two simple tools, one to fetch emails from my Gmail inbox, another to send emails. Okay, now let's test them. I'm going to prompt both agents with the same task. So let's ask the first agent. Give me our unread emails from today. So this agent makes API calls to Leipzig or one through grok. And as you can see, it successfully fetched all my unread emails. Nice. Now let's test the second agent which connects to Deepsee R1 to open rotor.

I prepare the query inside the when clicking Test Workflow trigger node. So the query is the same. Give me all unread emails from today. So let's test our workflow. And as you can see we've got an error. So if you are using Deepsee or won by making API calls to the platform to operate on locally, and wondering why your tools are not working is not a bug. The model just doesn't support tool functions.

So as you can see, no endpoints found that support tool use. Now how to use Deepsee R1 to grok. So to get started with grok, go to console.com and you will land on this page. So it's a super fast AI hosting platform around ten times faster than most services. They host a lot of models themselves. So click on the console to access the playground sign up. Head over to API keys. Create a new API key.

Give it a name. Copy it. Now if you want to learn more about these services and what models they offer under documentation, Click on models. And you can see all the models they they host. So we are interested in this one. You can even use their API for free for some time on the free plan which is great. Now go back to n810. Let's remove this node so I can show you from scratch. Ah, the new chat model.

Search for grog. Grog. Chat model node. Create new credential and paste your API key right here. It's safe. Now you'll have access to all the models. So just select Leipzig or one distill llama 70. And you are all set. Here is a quick comparison of the deep sea or 170 model when hosted on different platforms, including grok Operator and Deep Six official API. And for reference, OpenAI's own model.

When you look at the relative cost grok operator and Deep Six official API are about 25 to 27 times cheaper than OpenAI one. So that's a massive difference. And that's pretty much it.

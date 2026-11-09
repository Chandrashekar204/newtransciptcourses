# Build a DeepSeek R1 WhatsApp AI Agent to Plan and Research Anything for You

*Section: RAG & Research AI Agents*

In this tutorial, I'm going to show you how to build a WhatsApp AI agent that can plan everything for you. We'll be using Deep Sigrun as the brain for our AI planner agent. It's an amazing reasoning model that's great for planning, decision making and complex reasoning tasks. The planner agent will analyze your requests and craft a detailed plan to our second agent, which is a research agent. Now let's do a quick demo.

Let's say I wanted to plan a budget friendly one month stay in Thailand as a digital nomad. I need a cheap place to stay, good wifi, coworking spaces and some great attractions to visit. Let's test the workflow. Normally you wouldn't do this if the setup is active, but I wanted to show you the flow. So I'm going to hit this workflow. And send the message. Our agent is now analyzing the request and preparing a plan, passing it to our second agent, which is research agent.

The research agent uses Serp API to search the web. We should get a response in WhatsApp in a sec. So let's just wait a moment. All right. Great. Let's have a look for a budget friendly one month stay in Chiangmai. So as you can see, our agent recommends Chiang Mai as a city to stay. It has prepared affordable accommodation options with website links. It also suggests that negotiation can help lower the price, which is really good point.

Actually, it remembers that we are looking for a place with good wifi, which is great. It also funds coworking spaces. And provides website links with addresses. Top attractions. Cooking classes. Transportation options. It recommends to rent a scooter. Or. I really like this. It even provided a total cost estimate so you know exactly what to expect, which is impressive. You also have additional tips.

All right. Great. So this is just an example. You can use this agent to plan anything both for personal and business use cases. For example you can use it for market analysis or competitors research. You can plan whatever you want with this agent. So just to quickly show you, when we open our Typekit R1 planner agent, we can see all the reasoning steps. So okay, so I need to plan a budget friendly one or stay in Thailand as a digital nomad.

And 3D days. So you can check exactly the thinking process of this agent. That I should update a local events or festivals happening during my stay. So this agent really helps to plan our trip to Thailand And it passed all this information to our research agent, which has performed the web search. Okay, now let's jump into A10 and build these agents from scratch. Now let's start building our agents.

So usually the first thing we need to do is add our trigger node. In this setup we'll be using WhatsApp. And some time ago I recorded a video on how to easily connect WhatsApp to your agents in an A10 in just six minutes. So I'll play that later. For now, let's focus on building our agents first, and then we'll integrate WhatsApp as an input and output for the first and last nodes in our workflow.

So let's search for agent node. Click on add node button. Search for Agent. Let's close it for now. So as I said, we trigger our workflow, uh, in WhatsApp. So we need to remove this node. Now we need to add the chat model. So as the brain for our planner agent we'll use R1 through grok the host distilled version of this model which we can use. So add chat model search for grok. Now to get started with grok go to console.com.

And you will land on this page. So it's a super fast AI hosting platform around ten times faster than most services. They host a lot of models themselves. So click on the console to access the playground. Sign up. Head over to API keys. Create a new API key. Give it a name. Copy it. Now if you want to learn more about these services and what models they offer. Under documentation click on models. And you can see all the models they they host.

So we are interested in this one. You can even use their API for free for some time on the free plan, which is great. Now go back to N810. Create new credential and paste your API key right here. Hit save. Now you will have access to all the models. So just select Dopesick or one distiller llama seven TB. And you are all set. We want the planner agents output to be retained and passed to the research agent.

So we need to add some kind of memory. So let's add the window buffer memory node. So click on this small plus button. Select window buffer memory, which is the easiest way to give our agents a memory. Let's keep the context window length to five, which means our agent will be able to remember the five last interactions. Let's close it. Now let's set up our research agent. So click this plus button to add nodes.

Search for agent again. Let's rename it to. Research agent. Confirm. And let's close it for now. Let's get rid of this friend chat. Message received. Trigger note. Now we also need to decide which large language model we want to use for the brain of our research agent. I want to use OpenAI's GPT four. For this tutorial, we'll use GPT four mini because it's fast and cost effective. Let's close it. Now we need to give our research agent access to some tools.

In that case, we need to connect it to CEP API. So click on this plus button. Search for Serp API. Serp API basically allows the agent to search the web. So select this node. Now we need to create an account and provide credentials to connect our account to this node. So click on this dropdown Create new credential. As you can see we need API key. So go to Serp API. And you will land on this page.

So this tool allows to scrape search engines using the API service. Create an account. Go to API key. Create your API key, copy it and paste it into an A-10. So we need to create a credential. And paste it right here. Then click save. And it should show as successful. Now that we have set up the planner agent and research agent, let's complete the workflow by integrating WhatsApp so you can communicate with your planner agent.

So now I'm going to play a video on how to do it in a few minutes. Before we jump into configuration, just quickly to give you some insights, why using WhatsApp as a communication channel is so important, and why almost every business should use it. Did you know that WhatsApp is one of the fastest growing communication channels for businesses? Over 50 million businesses are already using WhatsApp to connect with their customers, and the app has over 3 billion users globally.

WhatsApp messages have a 98% open rate, compared to just 21% for email, and 68% of users say WhatsApp is the easiest way to reach a business. It's less common in the US but is very popular in Europe, South America and Asia. Now let's move on to the integration part. First, we need a trigger to activate our workflow. So we'll start with the WhatsApp business cloud node. So search for WhatsApp. Choose WhatsApp Business Cloud.

And choose on messages. Basically this node acts as a trigger it listens to for incoming messages on your WhatsApp account. Now we have to set up credentials to connect to our WhatsApp business account. So we will need our client ID and client Client's secret, so we need to get it from Facebook business account. Since WhatsApp business is managed under meta. So go to business.facebook.com and log in with your Facebook account.

If you are already logged in, it will take you to your Business Manager dashboard. If you have never used Facebook Business Manager, you will need to create a business portfolio. So go to business facebook.com slash settings and provide all the required details like your business name, email and any other information requested and click Create Business. Now choose the business portfolio you have created.

And in your Business manager, look for the account section on the left hand menu and click apps. Now click add and create a new app ID. Here you have to provide an app name. So let's say an app contact email. So. Then click on next. Scroll down. Choose. Other. Next. Business. Next. And create the app. Now click on the app you created. App settings. Basic. If you remember, we are looking for an app ID and app Secret.

So this is our app ID. Copy it. Go back to Nan. Paste it here. Show up secret then copy up secret. Paste it here and test connection. So now let's set up WhatsApp node to send replies back to the user. So this will allow your agent to respond to messages automatically. Search for WhatsApp. And choose send message node. Now you have to provide access token and business account ID. So let's go back to our Business Manager account.

go through API setup. And here you have to generate access token and then copy this access token to place it here. And you can find business account ID. Right here just copy it and paste it here. Then hit Test Connection. Just the last step. You need to choose your business mobile number. Or you can use the test number to test the connection. Now a key part of building AI agents is giving them a clear, well-designed prompt to guide what they do and how they respond.

I've put together prompts for both agents, and I will share them with a template so you can easily copy and paste them. Let me just quickly show you what it looks like. So for our planner agent. You might say something like you are an AI planner agent responsible for generating structured, actionable task plans. Your goal is to break down objectives into clear steps that guide execution and instructions.

And for our research agent. The prompt is more complex. So the role instructions use API to search for relevant results. Avoid special characters, etc..

# Optimizing Workflow Testing: Pinning & Editing Data in n8n

*Section: (Optional) Beginner Theory and Foundations - Fundamental Concepts*

In today's lesson, we are going to talk about two super useful features in any ten being data and editing output data. So by the end of this video, you will know how to pin data and why it speeds up workflow building. How to edit output data to test different scenarios and how to use past execution data for debugging. Let's jump right in. When you are building a workflow, you don't want to rerun everything from scratch every time, especially if some nodes take a while to execute or depend on external services.

So this is where ping data comes in because it saves time by avoiding unnecessary executions. It prevents making multiple API calls when testing so you can save a lot of money. If you are using base services and lets you build and test faster with saved data. For example, if you are using a webhook node instead of sending a request manually Manually each time you can pin the response and continue testing the next steps.

So how do you pin data? In this example, I've sent a message in telegram. So we already have data in the flow. So after a node runs you need to click. This pin icon in the output panel. And you can also simply unpin data. As by clicking here. So the blue pin indicator shows that the node's data is locked. And now every time you run the workflow, the pinned output is used instead of running the node again.

So in that case we have first name and second name. Now let's go back to our representation. Lets you manually modify a node's output. So it's useful for testing different data scenarios. And you can avoid unnecessary API calls by simulating responses. Now you can use fast execution data. So let's say your workflow failed at some point and you need to debug it without recreating the issue. So you can go to execution History in N810.

Now let's jump into N810 so I can show you. So in every workflow you have access to editor. So this is our canvas and two executions. So you can check the history of the executions. Actually you can check every execution of the workflow. So you can select a specific time of the execution. And you can find the node where the error occurred. So in this example. An error was caused by HTTP request node.

When we try to create an audio. So you can see all the details and find what causes the error. It really helps with debugging so you can easily fix errors without waiting for new data. Now let's go back to our presentation. So you can navigate to Execution History. Find the node and copy JSON data. You can pass it into the nodes Edit output section. And you can copy error data to debug without. So imagine you have a workflow that listens to a webhook and processes the data and sends a slack message.

Then it updates a record in Google Sheets. So to speed up testing, you can pin the webhook output to avoid manually triggering it every time. Edit output. So to test different responses like handling missing fields, and then you can even use mock data to simulate various user inputs. And this saves a lot of time. Now why you should care. Because big data makes workflow building faster and prevents unnecessary API calls and editing output.

Lets you test different scenarios without new data. Also, using past execution data helps debug errors quicker. So if you start using these features, you'll build workflows faster and debug smarter. All right. That's it for today's lesson. Now you know how to pin data and edit outputs. See in the next lesson.

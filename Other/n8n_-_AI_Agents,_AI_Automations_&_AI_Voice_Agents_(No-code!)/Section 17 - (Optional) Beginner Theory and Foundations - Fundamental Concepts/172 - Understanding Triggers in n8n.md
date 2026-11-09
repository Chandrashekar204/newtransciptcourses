# Understanding Triggers in n8n

*Section: (Optional) Beginner Theory and Foundations - Fundamental Concepts*

Welcome back. In this video we are going to focus specifically on triggers in A10. Before we build full automations and agents, we need to understand what triggers are, how they work, and why they are so important. Remember, triggers are what start your automation. Think of them as the starting point that tells your automation is time to run. There are different types of triggers. So let's go back to our overview.

And create workflow from scratch. It's good practice to give your workflow a name. For example triggers. Email and hit enter and just click on the canvas. Workflows are successfully created. Now. Always remember to set your time zone correctly in the settings. That's important for any time based triggers later on. So click on these three dots. Select settings. And choose your time zone. Save. The workflow settings saved.

Now we can explore different types of triggers. So simply put a trigger is the first step in your automation workflow. It tells Nathan when or how to start your automation. And there are many kinds of triggers in N810. You can add the trigger by simply clicking on this plus button. And here you can see the different types of sugars you can choose from. The first one is manual sugar, so you start the workflow yourself by clicking on the Test Workflow button.

And this is useful for testing or workflows. You want to control yourself. So your automation starts as soon as you click the Test Workflow button. Next we have an app event trigger, so this triggers starts the automation. Whenever something happens in another app like telegram, Airtable, notion, Gmail, Google Sheets, etc. so these triggers are very powerful because they allow you to connect to many different apps instantly.

And N810 has built in integrations for many apps, which means these are the dedicated nodes for these services. So you don't have to use a webhook node and set up the connection yourself manually. So N810 handles it for you. And as you can see, I'm scrolling down and there are plenty of on up event triggers available for you to choose from. So this triggers are very powerful. Next we have on Schedule Trigger.

So let's choose this one. And as you can see this trigger automatically run workflow. On a specific on a specific interval. For example every couple of days. Every minute. Once per hour. Every day at midnight. On custom schedules. Like every Monday at 8 a.m., for example, you might schedule a daily email summary at eight in the morning automatically. Next we have. On call, which means this trigger starts workflow when it receives an HTTP request from another system.

So if you are looking for an app to connect to in an A-10 and there is no direct integration. When you check on app event triggers, you can connect to any app that provides access to an API by using this. By choosing on a webhook call trigger. So it's useful when you need to connect custom applications, external services, or APIs. For example, a payment system like stripe sends data to an A10 and when a new transaction is completed, triggering an automation that logs the payment in Google Sheets.

So here you have to configure the webhook node and provide a URL and choose the method. And we'll go how to do it in detail in the next lesson. Next we have. On form submission trigger. So this trigger allows you to create simple web forms inside an A10. And your workflow runs whenever someone submits the form. And you can embed this form into your website so there is no need for external form services, and they then can handle form submission on its own.

Also you have when executed by another workflow trigger. So this allows one workflow to trigger another so you can connect multiple workflows multiple automations. So it's easy to break complex automations or agents into smaller workflows. It helps keep your automations modular and organized. And the last one on chat message. So when you choose this trigger, you can start the workflow by paying this chat module.

Chatting for example, with your agent. All right. These are different types of triggers available in N810. We'll go through each of them in more detail in next lessons. So don't worry this is just an introduction. Action. Just to quickly summarize what you have covered in this episode, manual trigger runs whenever you want to start your automation manually on app event when something happens externally in different apps.

Scheduled trigger is time based and automatic repetition. So every two hours, every day on a specific interval webhook trigger run from external HTTP calls. So there is no dedicated node to use as a trigger to connect to an external app. You can configure a webhook trigger node to make API calls and connect to different apps. Form submission trigger automatically run when someone fills out your form.

And triggered by another workflow. Connect multiple workflows together.

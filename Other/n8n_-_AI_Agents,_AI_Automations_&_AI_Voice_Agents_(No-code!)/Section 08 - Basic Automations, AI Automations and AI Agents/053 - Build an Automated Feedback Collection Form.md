# Build an Automated Feedback Collection Form

*Section: Basic Automations, AI Automations and AI Agents*

In this lesson, we are going to create a feedback collection form for your friends. Customers or clients can easily leave their feedback and all the responses will automatically appear in a Google Sheet organized and ready for you to review. So let's get started. First, open your dashboard. Click on Create Workflow. Now give your workflow a name. Let's say feedback collection form. Press enter. Now we need to start our workflow with some type of trigger.

So in this particular scenario we are going to use on form submission trigger. So let's search for this node by clicking on this plus button and select on Form Submission trigger. Now any time you see that something is highlighted in red or there is an exclamation mark, that's mean, there is something wrong. There is some issue we have to fix. So in that case, we need to provide at least one field in our submission form.

So first let's ask for a name. What's. Your first name. Now let's. Now let's add another field. So what's your email? Now let's ask about the feedback. So please give us. Your feedback. And let's change element type to the drop down list. And as the first option. Our customer is happy. The second option let's say good. Neutral. And but. Also you want our customer to leave a comment. So let's let's add the last field.

Please leave a comment. All right, let's close it for now. As you can see, there is still something wrong. Which means our automation will not be executed successfully. Because there is an issue we have to fix. So let's open this node. And as you can see, we have to give this form a title. So let's call it feedback form. Now we have our trigger. So when we click Test workflow the submission form will pop up.

So let's quickly fill it out. Damon. And now when I click submit, this data will be passed into our node. As you can see, the workflow was successfully executed. Now let's open this node. And on the right hand side and the output you can see all the information we just submitted. Alright. Awesome. Now before we connect our workflow. To pass all this data to Google Sheets, let's quickly create a simple spreadsheet to store all the feedback responses.

So I'm just going to my Google Drive. And creating a Google Sheets. Now let's call it feedback collection. And we need four columns. The first one is name. The second one email. Feedback. The last one is comment. All right. Great. So now let's go back to our Na ten. Now we have our trigger node. So we need some type of action. So let's search for an action node. In that case you want to use Google Sheet to pass all this information into Google Sheet.

So let's let's search for a Google Sheet node. Now here you can choose a specific action you want to perform. In that case we want to append row in a sheet. So let's select this one. Now if you are using a cloud version of an A-10 in order to connect your Norton account into your Google Sheet app. You can just simply sign in. So just simply sign in with Google and you don't need to do anything else.

You are all set up. But if you are self-hosting, then you have to provide credentials by clicking on this drop down menu and creating credentials. And you will see that you will have to provide client service and client client key. So if you are self-hosting and then go to Setup Credentials section and you can find a separate tutorial on how to connect your Google account into N810 and how to find client service and client API.

For now, let's close it. And let's sign in with Google because this is the cloud version of N810. Now, as a resource, we want to use a specific sheet within document and the operation we want to append row. But if you want to create a row or bilateral or retrieve information from a specific row or update row, you can switch over to a different operation. Now let's choose our document from list because this is the easiest option.

So we name our Google Sheet feedback collection. So let's choose this one. And the sheet is sheet one. Now, as you can see, any ten loaded or our columns automatically. So now let's go back to our canvas. And let's connect on submission trigger note to our Google Sheets note. Now when we click Test Workflow, we need to fill out the form to add some data to our workflow. And hit submit. Now as you can see, there is a problem in Google Sheet because we need to drag and drop dynamic variables into those fields.

Because every time a new customer fills out the form, they have different name, different email. They can give you different feedback and leave different comments, right? So we can simply drag and drop these dynamic variables into those fields. So what's your first name? What's your email. And also the feedback. Now when I click test step my response is from submission form should be added into a Google sheet.

So let's check our Google Sheet for now. Every column is empty. But when I click the step. We pass all the information into our Google sheet. Let's check it again. As you can see, we have Damon email and feedback. And there is a small issue because one column is missing. And as you can see here, columns are outdated. So you have to refresh it to see the changes. So let's click refresh. And now the last column comment appeared.

So we need to drag and drop this dynamic variable as well. And now when I click the step. We should receive a comment as well. So our last row will be updated. Let's check our Google sheet. And as you can see now all the columns have been populated. Let's go back to Nathan. And let's close it for now. Now, in order to make this workflow for real world use, we can change the workflow status from inactive to active.

So you don't need to click on Test Workflow to activate this automation. And every time when someone submits the form, it will trigger automatically. So let's do it now. Confirm. Now let's open on submission form. And now we need to use the production URL because this is a production ready automation. As we change the status to active. Proactive. We can use the production URL. And send it to our friends or customers.

And we can add this form into our website just to demonstrate it to you. I'm going to open this form in a separate window. And now when I fill out the form let's do it. And submit the form. We receive responses in our Google Sheet. As you can see, We collected a new feedback from a new user without testing our workflow, because we changed the status of the workflow to active and use production URL to open the submission form.

We are using confirm submission just for the sake of this tutorial, but you can use different form builders to make a beautiful forms and and added them to your website or funnels. For example, you can use you can search for form and you can use type, form, short form, tidy and any other form builder that provides access to the API. Congratulations! You have built your fully functional feedback form automation in just a few clicks, so well done.

Now let's move to the next lesson.

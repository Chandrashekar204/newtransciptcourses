# 1.5 — Definition of Microservices

> Section 1: Introduction to Microservices Architecture

So far in this course, we have spent quite some time understanding how microservices evolved from monolithic architecture and so on. But now imagine you are in an interview talking to your client or having a discussion with a business stakeholder. Someone suddenly asks you a very simple question, can you define microservices? You probably don't want to spend the next 20 minutes explaining monolithic architecture, SOA, and all the concepts we have discussed so far.

Instead, you need a short, professional, and easy to understand definition. That's exactly what we will learn in this lecture. One of the most widely accepted definitions of microservices was given by James and Martin in one of their well-known articles. Let's read that definition first, and then we will break it down into simple language. Microservices is an approach to developing a single application as a suite of small services, each running in its own process and communicating with the lightweight mechanisms, built around business capabilities and independently deployable by fully automated deployment machinery.

Now, let's understand what this really means. The first phrase says, a suite of small services. Instead of building one large application, we divide it into multiple smaller services. For our EazyBank application, these services are accounts, cards, and loans. Each one focuses on solving one specific business problem. The next phrase says running in its own process. This simply means every service is independent. If one service needs to be restarted, upgraded, or scaled, it does not require restarting the entire application.

Next comes, communicating with the lightweight mechanisms. In modern applications, these services usually communicate using REST APIs or other lightweight protocols. Instead of making method calls inside the same application, they communicate over the network. The definition also says, built around business capabilities. This is one of the most important characteristics of microservices. We don't divide services based upon technical layers. Instead, we divide them based on business domains like accounts, cards, loans, payments, customers, and so on.

Finally, one of the biggest advantages, independently deployable. Imagine a developer makes a change to the accounts microservice and pushes the code to GitHub. An automated CI/CD pipeline builds the application, runs the test, and deploy only the account service without affecting the cards or loan services. That's the power of independent deployment, and it's one of the key reasons why organizations adopt microservices. So if someone asks you for a simple definition of microservices, this is the one I would recommend you remember.

As we continue through this course, you will see every part of this definition come to life through practical examples. So don't worry if every sentence does not make perfect sense yet. By the end of this course, this definition will feel completely natural. Thank you, I will see you in the next lecture.


########################################

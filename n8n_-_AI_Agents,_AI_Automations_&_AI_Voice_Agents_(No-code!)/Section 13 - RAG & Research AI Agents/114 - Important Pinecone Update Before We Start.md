# Important Pinecone Update Before We Start

*Section: RAG & Research AI Agents*

Hi! This quick tutorial is just a brief update to show you one important thing before we build our first rack agent in the next video. In the next tutorial, we are going to build this rack system and we'll be using pinecone as our vector database to store the knowledge base. So the data for our agent I will explain everything step by step. In the next tutorial, I just want to show you and let you know that pinecone changed one thing since I recorded the tutorial.

So if you follow what I'm doing in the next tutorial and we create an index on pinecone, please note that after selecting the embedding model, we'll be using this one text embedding model from OpenAI. Before you click Create Index after select. After selecting this model, before you click on Create Index, there is an extra step you need to take. You need to click on Custom Settings right here and in the dimension field.

Change it to 1536, which is the vector size that OpenAI's text embedding model produces. If you don't do this, you will get an error in N810. So please, before you click Create Index, make sure you add this dimension value. In the next video we will build this system from scratch. So see you there!

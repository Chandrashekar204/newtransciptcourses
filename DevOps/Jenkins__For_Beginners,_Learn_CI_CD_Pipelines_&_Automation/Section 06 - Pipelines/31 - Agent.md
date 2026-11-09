# Agent

*Section: Pipelines*

1 With any Jenkins pipeline, 2 it always starts with a pipeline statement, 3 which is pipeline {}. 4 As you can see, my curly braces are yellow. 5 I'm using that colorizing plugin. 6 And trust me, this is going to be so useful 7 for when you're setting up Jenkins pipelines 8 because it is so easy to miss a step or miss a curly brace 9 and wonder why everything isn't working. 10 So next up, we need to specify an agent.

11 And this is what node or Jenkins slave should this run on. 12 Now, because we only have one setup, we're going to use any. 13 And again, if you have a look at the links I provided, 14 what you'll see is you can configure these 15 to run on specific nodes or Jenkins instances. 16 So if you have a team that runs Maven 17 and a team that runs Gradle, 18 rather than having one generic image or node 19 set up specifically with both, you can now isolate it.

20 And this is really good for if you have teams 21 with different requirements. 22 So some might need additional plugins, some might need less, 23 there may be security concerns with another. 24 So what you can do is configure custom instances 25 for whatever the requirement is.

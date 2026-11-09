# Docker and Devops

*Section: Introduction*

1 If you look at it, traditionally, developers developed applications. 2 Then they handed it over to the ops team to deploy and manage it in production environments. 3 They did that by providing a set of instructions, information about how the host must be set up, 4 what prerequisites are to be installed on the host, how the dependencies are to be configured, and so on. 5 Since the ops team did not really develop the application on their own, 6 they struggled with setting it up.

7 When they had an issue, they worked with the developers to resolve it. 8 With Docker, the developers and operations teams work hand-in-hand to transform the guide into a Dockerfile 9 with both of their requirements. 10 This Dockerfile is then used to create an image for their applications. 11 This image can now run on any host with Docker installed on it, 12 and it's guaranteed to run the same way everywhere.

13 So the ops team can now simply use the image to deploy the application, 14 since the image was already working when the developer built it, 15 and the operations have not modified it, 16 it continues to work the same way when deployed in production. 17 And that's one example of how a tool like Docker contributes to the DevOps culture. 18 This is it for now. 19 Next, we will look at how to get started with Docker.

# Credentials

*Section: Advanced Jenkins*

1 I wanted to touch quickly on credentials. 2 I'll include a link to this page 3 because you can see with different ways of handling secrets 4 and credentials in Jenkins. 5 Normally, when connected to GitHub, 6 we might use a username or password 7 or we'll set up an SSH key. 8 Again, it's completely dependent 9 on what platform you're using, 10 and there are loads of guides. 11 So if you're using GitLab, or Bitbucket, or GitHub, 12 there'll be a guide of exactly how to set up the access.

13 The bit we're looking at here is if we have things 14 that we need to connect to, like other resources. 15 And all though it'd be worth touching on this 16 because this is a really prime example here 17 of setting up the AWS access. 18 One of the most common ways I've seen this done 19 is not like this. 20 So with AWS, we can assign roles 21 to the specific nodes Jenkins is running on, 22 that way we don't have to insert any credentials.

23 This now makes it infinitely more secure 24 than this approach here. 25 Now, Jenkins does have secret management to an extent, 26 and this is some general advice coming from someone 27 who's a DevOps consultant saying, 28 normally, if you want to do something like this 29 and you've got Jenkins running on EC2 instances on AWS, 30 and the same applies to many cloud platforms, 31 instead of using credentials, 32 what you could do is assign the role to the node, 33 and that will grant you the same access you need.

34 Again, I'll include a link to this 35 because everyone has got different secret requirements, 36 but I thought I'd pick up on this one 37 because the example here, although good, 38 there's better ways you can do it. 39 That wraps up this video, 40 I look forward to seeing you in the next one.

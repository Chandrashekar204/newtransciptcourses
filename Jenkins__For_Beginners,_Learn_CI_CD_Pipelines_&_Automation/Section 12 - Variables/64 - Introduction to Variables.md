# Introduction to Variables

*Section: Variables*

1 Hi, and welcome to this section. 2 You're going to be learning about variables in Jenkins. 3 With variables, they are so easy. 4 This section is going to be a lightning fast. 5 You're gonna learn about them so quickly. 6 They are so easy to set up. 7 Now, what variables allow us to do 8 is help keep our code neat, 9 and we can use and store information 10 that we're going to use repeatedly. 11 Now, one of the most common uses 12 for these I've seen in industry has especially been 13 with pipelines working with Docker.

14 So, what you might do is you would set up one variable 15 for the repository URL, 16 and you might set up a second one for the image name, 17 which is usually the same name as the application. 18 So, the way some teams did it 19 is they had one pipeline per application, 20 but using variables, you could create a template 21 so then the DevOps engineer could take this template, 22 swap out the URL, swap out the application name, 23 and that was it, done.

24 So, throughout the entire pipeline 25 with all the different steps, 26 so the building, the testing, 27 the pushing up, the building the image, 28 all of those were taken care of 29 because all we had to do was swap out two variables. 30 Again, these are so easy, 31 and you're gonna see how fast it is 32 to set them up in this demo, 33 but this section is going to be a breeze, 34 so let's jump into it and let's get started.

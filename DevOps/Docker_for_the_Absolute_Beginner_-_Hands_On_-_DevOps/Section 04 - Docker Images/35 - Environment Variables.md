# Environment Variables

*Section: Docker Images*

1 Let us start with a simple web application written in Python. 2 This piece of code is used to create a web application that displays a web 3 page with a background color. 4 If you look closely into the application code, you will see a line that sets 5 the background color to red. 6 Now that works just fine. 7 However, if you decide to change the color in the future, you will have 8 to change the application code.

9 It is a best practice to move such information out of the application code 10 and into say an environment variable called app color. 11 The next time you run the application, set an environment variable called app 12 color to a desired value, and the application now has a new color. 13 Outside of Docker, you would set the variable inline before launching the app. 14 Once your application gets packaged into a Docker image, it would then run with 15 the Docker run command followed by the name of the image.

16 However, if you wish to pass the environment variable as we did before, 17 you would now use the Docker run commands dash e option to set an environment 18 variable within the container. 19 To deploy multiple containers with different colors, you would run the 20 Docker command multiple times and set a different value for the 21 environment variable each time. 22 So how do you find the environment variable set on a container that's 23 already running, use the Docker inspect command to inspect the 24 properties of a running container.

25 Under the config section, you will find the list of environment 26 variables set on the container. 27 The output includes a section similar to the following, the exact Python 28 version and Python PR version values vary depending on which version of 29 the Python base image was pulled. 30 Docker keeps them in sync with the image. 31 The numbers above are from Python 3.12 pip 24. 32 Well, that's it for this lecture on configuring environment variables in Docker.

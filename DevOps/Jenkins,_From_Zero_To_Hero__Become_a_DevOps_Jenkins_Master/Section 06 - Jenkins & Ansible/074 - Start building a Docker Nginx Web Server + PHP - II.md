# Start building a Docker Nginx Web Server + PHP - II

*Section: Jenkins & Ansible*

Instructor: Hello, and welcome back. In this video, we're going to be creating the Docker container to host our web server. So we already created our Dockerfile and all the things needed for this to work, so it's time to start dividing our service in the docker-compose file so we can create a container from this. So, we're going to head to this directory, where we have the docker-compose file. We're going to modify this.

And we're going to create a new service. So, I think that you already know how to create services, so let's go ahead and create a new service, which is going to be called web, to keep it simple. And under web, we're going to give you a container name. And that name is going to be, for example, web. And then we're going to define the image. So remember that the image, it's going to be a custom image that we're going to build.

So we can call it as we want. Let's call it, for example, ansible-web. And then remember that we want to build this image because it doesn't exist. So we say build, and then we specify the context for this. And we're going to look for the context. So, where is our Dockerfile located? Remember, from here, if we do an ls jenkins-ansible/, the Dockerfile is not there. But if we go to the web folder, the Dockerfile is there.

So if we do a cat jenkins-ansible/web/Dockerfile, we're going to have the NGINX Dockerfile. So this is actually the context where Docker should look for the Dockerfile. So let's modify our docker-compose file in here. And let's add this folder as the context. So now, we need to expose some ports because we want to be able to access this service using the jenkins.local VS. So we want to expose the port 80 to our 80 port.

And that way, we can access it from the browser. And finally, we want to join this service to the network net so all of the other services can reach this new service. So this is pretty cool. So let's save this. And now, we want to build this new image. So we do a docker-composed build. We hit Enter. And as you can see, this entire process is going to be starting. So Docker is going to start installing NGINX, PHP, and doing all of the things that we specify in the Dockerfile.

So this may take a while, depending on your internet connection. So I will pause the video, and I will come back when it has finished. The process already finished. As you can see, everything was built successfully. So now, we can create this service using the docker-compose file. Remember that if we do a docker ps, we still don't have that service here because we haven't created it, we only built the image for the service.

To create a container, we need to do a docker-compose up -d. And then it's going to create the web server right away. So, let's wait. Now, let's hit a docker ps. And now, you're going to see your web server in place. Cool. So remember that we exported the port 80 of the container to our machine. So in this way, we can access the server on port 80. So let's go to our browser. Let's hit the jenkins.local, and hit the port 80.

And then you're going to have an NGINX web server up and running here. This already is cool, don't worry. It's because we don't have an index yet. So let's head to google.com, and let's look for the phpinfo function. I don't remember how the function is written. So, we are going to look for PHP Manual. No, I think this is not here. Oh, this is it, actually. So we can copy this. And now, we're going to exec inside of the web container that we created.

And if you read a little bit the configuration files that we created, the root folder for this web server is located on var/www/html, where typically files are stored in a web server. So in here, we don't have an index, that's why you're having the Forbidden error. But if we create an index.php, and then we paste the code. We're going to remove this last line. And then we save this. Remember that we're inside of the container, so we're modifying the source code that the web server is serving.

If we now go to the jenkins.local on port 80, we're going to have an nice screen telling us that our PHP installation on NGINX was successful. So, cool. Our server is ready to start displaying our table. So this is it for this video. I'll see you in the next lesson.

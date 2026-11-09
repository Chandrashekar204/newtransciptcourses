# Inspect and Logs

*Section: Docker Run Commands*

1 The docker ps command is good enough to get basic details about containers like 2 their names and ids but if you'd like to see 3 additional details about a specific container use the docker inspect command 4 and provide the container name or id it returns all the details of a 5 container in json format state mounts configuration data network 6 settings and more remember to use it when you need to find 7 details on a container and finally how do we see the logs of a 8 container we ran in the background for example i ran my simple web 9 application using the d parameter and it ran the container in 10 detach mode how do i view the logs which happen to be the contents written 11 to the standard out of that container use the docker logs command and specify 12 the container id or name an example output might look like this 13 well that's it for this lesson head over to the challenges and practice 14 working with docker commands

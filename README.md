
Get Started with Docker


![](./icons8-docker-480.png)


## What is Docker?

In a practical viewpoint, it is just a way to package software,so it can run on any hardware.

In order to know how this works, you need to understand three things: DockerFile, Docker Image and Docker Container.


1.DockerFile: It is a text document used to build Image.

2.Docker Image: It Docker image is a template for running Docker Container.

3.Docker Container: It is an executable package of software, that includes everything needed to run 
an application.

## Why Docker?
Say, we have a node application and we need a server to have the same version of node
and have all dependencies requiered. It will work on my machine but this may not work on yours.
Docker has been created to solve this types of problem specifically by producing similar environments.



## Installation
 
If you are in Windows/Mac install Docker Desktop, then you will have access to docker from CLI.

You can also practice your docker skills here: https://killercoda.com/playgrounds/scenario/kubernetes 

## Docker Commands

1.docker version
#docker version

2.docker #get a list of all commands

3.docker ps

4.docker container ls #shows all the running containers

5.docker container rm -f <container-Id> #removes the container forcefully

6.docker container stop <container-Id>

7.docker container start --help

8.docker container exec --help

9.docker container start -ai <container-Id> # start a stopped container again


10.docker pull alpine

11.docker image ls #see size of images

12.docker container run -it alpine sh

#inside container run 'apk'

#inside container run 'exit'


13.docker container run --rm -it centos:7 bash

#in container run 'yum update curl'

#in container run 'curl --version'

#in container run 'exit'








## DockerFile

example dockerfile: https://docs.docker.com/get-started/02_our_app/

docker image build -t custom. #build image (Dockerfile has to be in current dir)

docker image build -t custom . # rebuilds with a change to a line in the Dockerfile (e.g. add expose port 8080)

#keep the things that change the most at the bottom of the dockerfile for a faster build

docker container run -p 80:80 --rm nginx

docker image build -t nginx-with-html

docker container run -p 80:80 --rm nginx-with-html

docker image ls


## Docker Images
docker pull nginx

#union file system - making layers 

docker history nginx:latest

#containers start with a layer called "scratch"

#copy on write - when changes to the base image, container updated in real time, but base image never changes

docker history mysql #see the copy on write 

docker image inspect nginx

docker image tag --help

#just because you tag an image, doesn't mean that it changes the image Id.





## Videos
https://www.youtube.com/watch?v=Gjnup-PuquQ

https://www.youtube.com/watch?v=gAkwW2tuIqE&t=156s

https://www.youtube.com/watch?v=eGz9DS-aIeY


##### Assignment 2.b
1.	Create a DockerFile.
2.	Use Ubuntu latest image.
3.	Add your name as a Manintainer.
4.	Update local packages using command (apt-get update).
5.	Install nodejs package.
6.	Install npm package.
7.	Create a symlink using command (ln -s /usr/bin/nodejs /usr/bin/node).
8.	Trigger a command (npm install -g http-server)
9.	Add any test index.html file from local at /usr/apps/hello-docker/index.html on container.
10.	change your working directory to /usr/apps/hello-docker/.
11.	Run a command (http-server -s) on every container initialization.
12.	Build your dockerfile and tag it with “yourname:docker-web”
13.	Run a docker container from the image that you have just created and map container 8080 port to host 8080 port.(8080:8080)
##### Dockerfile
    FROM ubuntu:latest
    MAINTAINER Dev Ji Gupta
    RUN apt-get update
    RUN apt-get install nodejs -y
    RUN apt-get install npm -y
    RUN npm install -g http-server
    ADD . /index.html /usr/apps/hello-docker/index.html/
    WORKDIR . /usr/apps/hello-docker/
    CMD http-server -s
    docker build -t devjigupta:docker-web .


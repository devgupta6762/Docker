• Create a file named Dockerfile and write code as per the steps mentioned.
•	Use alpine image.
•	Add Author/Maintainer name in DockerFile
•	run commands -> apk update & apk add nodejs
•	copy current directory to /app
•	change your working directory to /app
•	specify the default command to be run upon container creation as mentioned below. node index.js
• Build image from Dockerfile.
• Tag image with name “hello:v0.1”
 #### DOCKERFILE
      mkdir ops1
      cd ops1
      gedit Dockerfile
      FROM alpine:latest
      MAINTAINER devgupta67621@gmail.com
      RUN apk update && apk add nodejs
      COPY . /app
      WORKDIR /app
      CMD node index.js
      docker build -t hello:v0.1 .

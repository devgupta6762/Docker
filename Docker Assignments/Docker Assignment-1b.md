#### Assignment 1.b
##### 1.	Again pull “alpine” image from docker registry.
     docker pull alpine
##### 2.	Take interactive login to bash while running docker container from “alpine” image.
	 docker run -it --name devalpine alpine:latest


##### 3.	Run command inside container: echo “hello world” > hello.txt ls
     cat hello.txt
##### 4.	Take exit from same container without killing the container.
     ctrl p+q
##### 5.	Run another container using below command and check if you can find hello.txt within this container. You should find container isolations from step 3-5. docker container run alpine ls
    no i can't find |
##### 6.	Stop a container using Container ID.
     docker stop <container id>
     docker ps //To show only running containers.
     docker ps -a //To show all containers.
     docker ps -l //To show the latest created container.
     docker ps -n=-1 //To show n last created containers.
     docker ps -s //To display total file sizes.
##### 7.	Start same container using ID and exec a command “echo ‘hello world!’” in docker container without instantiating a new container.
    docker start <container name>
    docker attach <container name>
##### 8.	Inspect already downloaded “alpine” docker image using docker inspect command.
     docker inspect alpine
##### 9.	Tag your local “alpine” image with name “myimage” along with version 1.0
     docker commit snehaalpine myimage:1.0
#### Docker Installation Assignment-1.a
##### 1.	Run a docker container from “hello-world” image.
     docker run hello-world
    
##### 2.	Pull “alpine” image from docker registry and see if image is available in your local image list.
    docker pull alpine (Alpine, Linux is a security-oriented, lightweight Linux distribution  based on musl libc and busybox.)
    docker ps(yes)

##### 3.	Pull some specific version of docker “alpine” image from docker registry.
     docker pull alpine:(20210212, edge
     3.13.4, 3.13, 3, latest
     3.12.6, 3.12
     3.11.10, 3.11
     3.10.8, 3.10)
##### 4.	Run a docker container from local image “alpine” and run an inline command “ls      -l”while running container.
     docker run -it --name devalpine alpine:latest|ls-l
    
##### 5.	Try to take login to container created using “alpine” image.

##### 6.	Detach yourself from the container without making it exit/container kill.
     ctrl + p +q
##### 7.	Check running containers and see if you can find out the stopped containers.
     docker ps|docker ps -a(list of stopped containers)
##### 8.	Stop running container.
     docker stop devalpine
##### 9.	Start container that was stopped earlier.
     docker start devalpine
##### 10.	Try to remove “alpine” image from your local system.
     docker image rm alpine -f

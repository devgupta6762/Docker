## Docker Port:
##### 1.	Pull nginx image from dockerhub.
     docker pull nginx
##### 2.	Run a container from nginx image and map container port 80 to system port 80.
     docker run --name mynginx1 -p 80:80 nginx
##### 3.	Display all mapped ports on nginx image.
     docker ps
##### 4.	Run a docker container named “containexpose” from nginx image and expose port 80 of container to outer world without mapping it to any of system port.
    docker run -it --name containexpose -p 8080:80 nginx
    Then you can hit http://localhost:8080
## Docker Volume:
##### 1.	Create docker volume named “dbvol”
     docker volume create dbvol
##### 2.	Run docker container from wordpress image and mount “dbvol” to /var/lib/mysql
     docker run -it --name assb -v dbvol:/var/lib/mysqlwordpress

##### 3.	Display all docker volumes.
     docker volume ls
##### 4.	Create another docker volume named “testvol”
    docker volume create testvol
##### 5.	Remove docker volume “testvol”
     docker volume rm testvol
     docker volume ls
## Docker Linking:
##### 1.	Run a container in detached mode with name “db” from image “training/postgres”
    docker run -it -d --name db training/postgres:latest
    Means that a Docker container runs in the background of your terminal. It does not receive input or display output.
##### 2.	Run another container in detached mode with name “web” from image “training/webapp”, link container “db” with alias “mydb” to this container and finally pass an inline command “python app.py” while running container.
    docker run -d -P --name web --link mydb training/webapp |python app.py
    docker inspect -f "{{ .HostConfig.Links }}" web
    [web container is linked with db]
    
##### 3.	Take a bash terminal in “web” container.
     docker exec -it web /bin/bash
##### 4.	Test container linking by doing a ping to “mydb”.
     ping mydb
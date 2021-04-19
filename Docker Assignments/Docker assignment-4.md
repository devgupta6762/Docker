
##### 1-	Install docker-compose on your machine, if not already installed.
     sudo curl -L "https://github.com/docker/compose/releases/download/1.29.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
     sudo chmod +x /usr/local/bin/docker-compose
##### 2-	Check docker-compose version.
    docker-compose --version
##### 3-	Create a directory named nginx in your root.
    mkdir nginx
##### 4-	Switch to that directory and create a file named docker-compose.yaml
    cd nginx
    vim docker-compose.yml
### Docker-compose
    version: '2'
    services:
      databases:
        image:mysql
        ports:
          -3306:3306
        environment:
          MYSQL_ROOT_PASSWORD: arimagupta262701
          MYSQL_DATABASE: mydb
          MYSQL_USER: dev
          MYSQL_PASSWORD: 4108
    docker-compose up -d
          
##### 5-	Use docker-compose version 2 to create docker-compose.yaml file.
##### 6-	Create a service named “databases”.
##### 7-	Use image named “mysql”
##### 8-	Map container 3306 port to host machine 3306 port.
##### 9-	Add environment variables named “MYSQL_ROOT_PASSWORD”, “MYSQL_DATABASE”, “MYSQL_USER” and “MYSQL_PASSWORD” along with corresponding values for all.
##### 10-	Add another service named “web”

    
   
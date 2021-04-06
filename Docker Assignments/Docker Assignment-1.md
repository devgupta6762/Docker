#### Assignment-1
##### 1.   Use official shell script to install and configure Docker on your control machine.
     copy the script into host machine and save it in .sh format,
     execute permission on your script using chmod command :
     chmod +x script-name-here.sh
     To run your script :
    ./script-name-here.sh
##### 2. Start Docker service and check status of the same.
    systemctl start docker | systemctl status docker
##### 3. Enable Docker service to start at every machine reboot.
    systemctl enable docker
##### 4. Display Docker version.
    docker --version
##### 5. Configure non root user to run docker commands without sudo.
    add the name of user in etc/sudoers file from root user and give priviledges to use docker command
##### 6. Type docker on commandline and read output i.e containing related commands.
    docker
##### 7. Display System information using Docker.
    docker system info
##### 8. Check whether you can access/download images from DockerHub or not.
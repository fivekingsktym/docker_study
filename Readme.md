# Docker Basic Commands

```bash
docker images # showing all previous installed images

# Showing running commands
docker ps #showing current running containers
docker ps -a #showing all current and previous runned containers

<or> # both are same ["container ls" is the modern command, old "ps" is also working a command]

docker container ls #showing current running containers
docker container ls -a #showing all current and previous runned containers

# downloading a container from dockerhub
docker pull techtvm/mysql_techtvm

# running a docker image ------------------
# running in attach mode
docker run <image_name:version>
# running in detach mode
docker run -d <image_name:version>

<or>
# run a container using their id
docker start <container_name_or_id>
# running a docker image ------------------


# map and run a host port to running container port
docker run -d -p <host:container_port> <image_name:version>
# example
docker run -d -p 5000:6379 redis
docker run -d -p 6000:6379 redis:5.0

# running a docker container with a dedicated name
docker run -d -p <host:container_port> --name <custom_container_name> <image_name:version>
# example
docker run -d -p 6000:6379 --name redis_fivekings redis


# login to running docker container (like:- accessing to a remote system(os))
docker execute -iterative_terminal <container_name_or_id> <shell_path>
# example
docker exec -it redis_abhi bash #bash will locate to root directory
docker exec -it redis_abhi /bin/bash
# exiting from loggined container or remote system
"ctrl+d" or type "exit"

# stoping a running container
docker stop <container_name_or_id>

# stoping all running containers
docker stop $(docker ps -q)

# deleting all unused containers history from docker
docker container prune

# printing docker running logs
docker logs <container_name_or_id>


# building a custom docker file(Dockerfile with no extension)
docker build -t(flag_to_tag_the_image_name) <image_name> <path_of_dockerfile>
# example
docker build -t getting-started .



# creating a docker image in the root folder like env
docker save -o filename.tar image_name
docker load -i filename.tar
docker run hello-world:latest

# removing a docker image file
docker rmi --force image_name_or_id

# removing a docker container file
docker rm <container_name_or_id>

# network commands - start
# creating network in docker
docker create <name_of_network>
# showing all networks
docker network ls
# others network commands
connect     Connect a container to a network
create      Create a network
disconnect  Disconnect a container from a network
inspect     Display detailed information on one or more networks
ls          List networks
prune       Remove all unused networks
rm          Remove one or more networks
# network commands - end

```

# How to use docker compose
- check weather the docker-compose is properly installed in your system
- Installation process in Ubuntu and Debian is as follows :-

```bash
# updating sudo
sudo apt-get update
# installing docker-compose
sudo apt-get install docker-compose-plugin

# checking docker-compose version
docker compose version
```

## Running docker-compose file

```bash
# running a docker-compose
docker-compose up -d

# stoping a docker-compose
docker-compose down # if the file name is docker-compose, 
# or
docker-compose down -f <filename>

```



# linux commands
```bash 
pwd  #present working directory
ls #listing contents inside a directory 

lscpu # showing system details
lsb_release -a # showing linux version

cd # change directory
touch file_name.extension #creating a file in linux

mkdir folder_name # creating a folder in linux
# creating both folder and file inside the created folder
mkdir folder_name && touch file_name.extension
# example 
myfolder && touch myfolder/file.txt

# writing a line to a file 
echo "print("hello world")" > sample.py
# showing the contents from a file
cat sample.py

# elevate privileges and obtain a root or superuser access.
# By default, if you execute su without specifying a username, it will switch to the root user.
# <SuperUserDo> <Substitute User>
sudo su



# extrating tar file to a directory
tar -xf <file_for_extraction.tar> -C <fullpath_or_folder_name>
# example
tar -xf php-crud-app.tar -C php-crud-app
```
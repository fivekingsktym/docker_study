# Docker Basic Commands

```bash
docker images # showing all previous installed images

# Showing running commands
docker ps #showing current running containers
docker ps -a #showing all current and previous runned containers

<or> # both are same ["container ls" is the modern command, old "ps" is also working a command]

docker container ls #showing current running containers
docker container ls -a #showing all current and previous runned containers


# running a docker image ------------------
# running in attach mode
docker run <image_name:version>
# running in detach mode
docker run -d <image_name:version>

<or>
# run a container using their id
docker start <container_id>
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
docker execute -iterative_terminal shell_path
# example
docker exec -it redis_abhi /bin/bash
# exiting from loggined container or remote system
"ctrl+d" or type "exit"

# stoping a running container
docker stop <container_id>

# printing docker running logs
docker logs <container_id>


# running a custom docker file
docker build -t container_name path
# example
docker build -t getting-started .

```



# linux commands
```bash 
pwd  #present working directory
ls #listing contents inside a directory 
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

```
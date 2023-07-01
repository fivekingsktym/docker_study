# docker volumes

A volume is a directory that exists on the host machine and can be mounted into one or more containers. 

![Structure](9_video_docker_volumes/Docker-Volumes-Docker.png)


## 3 Types of docker volumes
- 1. Host volumes

```bash
docker run -v <host_directory_path> : <virtual_container_path>
# example
docker run -v /home/docker_study/data: /var/lib/mysql/data
```

- 2. Anonymous volumes 

docker will create an anonymous path in host machine like /var/lib/docker/volumes/random-hash/_data

```bash
docker run -v <virtual_container_path>
# example
docker run -v /var/lib/mysql/data
```

- 3. Named Volumes

docker will create folder with user defined name like /var/lib/docker/volumes/<user_defined_name>/_data

```bash
docker run -v name:<virtual_container_path>
# example
docker run -v name:/var/lib/mysql/data
```
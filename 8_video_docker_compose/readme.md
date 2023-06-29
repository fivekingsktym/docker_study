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
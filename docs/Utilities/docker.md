# Utilities / docker

**Table of contents**
  * [List Docker CLI commands](#list-docker-cli-commands)
  * [Display Docker version and info](#display-docker-version-and-info)
  * [Execute Docker image](#execute-docker-image)
  * [List Docker images](#list-docker-images)
  * [List Docker containers (running, all, all in quiet mode)](#list-docker-containers-(running,-all,-all-in-quiet-mode))
  * [Run ubuntu container and login](#run-ubuntu-container-and-login)

---

### List Docker CLI commands
```
docker
docker container --help
```
---
### Display Docker version and info
```
docker --version
docker version
docker info
```
---
### Execute Docker image
```
docker run hello-world
```
---
### List Docker images
```
docker image ls
```
---
### List Docker containers (running, all, all in quiet mode)
```
docker container ls
docker container ls --all
docker container ls -aq
```
---
### Run ubuntu container and login
```
hmoats@ubuntu:~$ docker run -it ubuntu bash
Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
f476d66f5408: Pull complete 
8882c27f669e: Pull complete 
d9af21273955: Pull complete 
f5029279ec12: Pull complete 
Digest: sha256:ff716f1a3077cbd7108fb10091f6f403cc0e7aec23f1f0202f408d7f81a0d0d0
Status: Downloaded newer image for ubuntu:latest
root@6b5537141201:/# 
```

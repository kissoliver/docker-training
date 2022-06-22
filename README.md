# docker-training


https://www.katacoda.com/courses/docker/playground

Alapműveletek
------------------
docker
    
docker version

docker ps

docker images

ps -ef | grep dockerd

Hello world
--------------------------
docker run hello-world

docker ps -a

docker images

Image műveletek
----------------------
docker tag hello-world hello-world:1.0
	
docker inspect hello-world 
    
docker save hello-world -o hello-world.tgz

tar  -tvf  hello-world.tgz

docker pull mysql 


Konténer indítás paraméterekkel
---------------------------------
docker run -d --name nginx -p 80:80 nginx

docker logs nginx 

docker stats 

docker top nginx 

docker exec -it nginx  bash

docker rm -f nginx 

docker volume használata
-------------------------
docker volume create testvolume

docker run -d -v testvolume:/opt nginx

Docker image építés
--------------------
Dockerfile létrehozása 

```
FROM alpine
run echo hello > /hellofile
```
  
docker build . -t myhello 

docker run myhello cat /hellofile

Podman használata
------------------
podman ps

podman images

podman run -d --name nginx -p 80:80 nginx

podman ps 

podman images

podman exec -it nginx sh

podman rm -f nginx

Podman podok használata
-------------------------
podman pod create --name testpod

podman run -d --pod testpod nginx

podman pod ps

podman ps --pod


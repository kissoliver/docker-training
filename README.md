# docker-training


https://www.katacoda.com/courses/docker/playground

Alapműveletek
------------------
docker
    
docker version

docker ps

docker images

Konténer műveletek
--------------------------
docker run hello-world

docker ps -a

docker images

docker logs <hello world container id>

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

docker stats 

docker top nginx 

docker rm -f nginx 

docker exec -it nginx  bash


Docker image építés
--------------------
Dockerfile létrehozása 

```
FROM alpine
run echo hello > /hellofile
```
  
docker build . -t myhello 

docker run myhello cat /hellofile




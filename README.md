# docker-experiments

https://www.youtube.com/watch?v=fqMOX6JJhGo&ab_channel=freeCodeCamp.org - Docker Tutorial for Beginners - A Full DevOps Course on How to Run Applications in Containers
https://www.youtube.com/watch?v=P4ZC3cFN0WQ&ab_channel=overment - Docker dla webdevelopera
https://kodekloud.com/p/docker-labs

Docker — это платформа, которая предназначена для разработки, развёртывания и запуска приложений в контейнерах. Слово «Docker» в последнее время стало чем-то вроде синонима слова «контейнеризация». И если вы ещё не пользуетесь Docker, но при этом работаете или собираетесь работать в сферах разработки приложений или анализа данных, то Docker — это то, с чем вы непременно встретитесь в будущем.


Container - completely isolated environment.


Installation:

https://docs.docker.com/engine/install/ubuntu/

Useful: 
https://coderwall.com/p/ewk0mq/stop-remove-all-docker-containers

# Image vs Container

An instance of an image is called a container. You have an image, which is a set of layers as you describe. If you start this image, you have a running container of this image. You can have many running containers of the same image.

You can see all your images with docker images whereas you can see your running containers with docker ps (and you can see all containers with docker ps -a).

So a running instance of an image is a container.

# Docker Commands

`docker run` - run container from an image

`docker ps` - list running containers

`docker ps -a` - list all containers

`docker stop <container_id/container_name>` - stop container

`docker rm` - remove container

`docker rmi` - remove image

`docker pull` - pull image (without starting)

`docker run -i` - interactive mode


# Port configuration

docker run -dit --name my-running-app -p 8080:80 my-apache2 // localhost:8080 is where application will be available

# DB connection locally

host: localhost
port: from docker-compose

# useful commands 


Stop and remove containers, networks
https://docs.docker.com/engine/reference/commandline/compose_down/
```
docker-compose down --volumes --remove-orphans
```

Create and start containers
https://docs.docker.com/engine/reference/commandline/compose_up/
```
docker-compose up -d --build
```

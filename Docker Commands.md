# Docker Commands:

### Show commands & management commands

```
$ docker
```

### Docker version info

```
$ docker version
```

### Show info like number of containers, etc

```
$ docker info
```

# WORKING WITH IMAGES

### Create an run a container with name

```
$ docker build -t <image-name> .
```
### View all Images,load, delete, save image

```
$ docker images
$ docker load -i <images-file>.tar
$ docker rmi <img-id>
$ docker save <images-file>.tar > <img-name>
```

# WORKING WITH CONTAINERS

### Create an run a container with name

```
$ docker run -d --name <conatiner-name> -p 80:80 <image-name>
```
### View all Containers,stop and delete
```
$ docker container ls
```

OR

```
$ docker ps
$ docker stop <conatiner-name/id>
$ docker rm <conatiner-name/id>
```


### Stop all running containers

```
$ docker stop $(docker ps -aq)
```


### Get logs (Use name or ID)

```
$ docker container logs [NAME]
```
### Get into docker container id:

```
$ docker exec -it <container_id_or_name> sh
```
### Some useful commands while deploy and debug:

```
$ docker logs <my-container>
$ docker inspect <my-container> | grep HostPort
$ wget http://<public-ip>:<hosted-port>/
```


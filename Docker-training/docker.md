# Docker Learnings

Docker image: it is the package with all the dependencies, application package and configuration packages. It is the artifact that is moveable.

Docker container: it is when the image is pulled on a local computer and it started so that all the applicationsin it is started and running.

Docker helps to run diferent versions of the same application in a local machine without conflict.

Docker virtualize in the application layer while virtual machine virtualize in the application and OS kernel.

Characteristics of Docker

> > > > > > > > > > > > > > > > > > > > > > > > > > > > > >

Size: Docker images are the smaller than that of virtual machine.

Speed: Dcoker container start and run much faster.

Compatibility.

`Docker ps` - This is to show all the running containers

`Docker images` - This shows all the running images

`Docker network ls` - shows all the available docker networks

`Docker ps -a` - shows all the containers available on the local computer.

Stop delete an images, the container connected to the image must be stopped and deleted.

Command to stop and remove the container

```
docker stop <xontainer id or name>
docker rm <container id or name>
```

Command to remove the image

```
docker rmi <image id or name>
```

To check the list of docker networks

`docker network ls`

To add a port to docker

docker run -p <port number> --name <name for container>

To get logs

docker logs <container id or name>

docker exec -it <container id or name>

# Docker Notes.

## Why Docker

> > > > > > > > > > > > > > > > > > > >

- it is a lighweight approach than virtual machines to isolate coding and project environments.

- It is portable

- It helps achieve continuous integration and deployment for development operations.

## Main features

- Create containers and images.

- Docker compose allows for multicontainer applications.

- Docker swarm to utilize multiple machines running Docker.

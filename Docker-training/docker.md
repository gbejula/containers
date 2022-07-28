# Docker Learnings

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

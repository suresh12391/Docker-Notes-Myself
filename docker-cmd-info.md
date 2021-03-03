### Docker Commands:
```
docker -v
docker info
docker ps
docker ps -a
docker kill {ID}
docker stop {ID}
docker stop $(docker ps -q)
docker rm $(docker ps -a -q)
docker logs 85a71207308c
docker stop <container-id>
docker inspect CONTAINER
docker inspect {CONTAINER_ID} | grep HostPort
```

```
docker exec  -it mongo-express /bin/bash
docker run  -it mongo-express /bin/bash
docker exec -it {CONTAINER_NAME} /bin/bash;
docker exec -u {USER_NAME} -it {CONTAINER_NAME} /bin/bash;
```

**Note:** Docker `run` is for creating containers. It is important to differentiate it from `exec`, which is used to interact with containers that are already running.

```
docker images
docker images --filter reference=bulletinboard
docker run {IMAGE_NAME}
docker image tag IMAGE IMAGE
docker image prune. NOTE: (Caution): Be aware before use this.
```

```
docker history test
docker restart mysql-host
```

```
docker container list
docker container prune (Remove stopped container)
docker container logs {CONTAINER_NAME}
```

```
docker network ls
docker network ls --format
docker network ls --filter type=custom
docker network connect net_default abc-docker
```

```
docker volume ls
docker volume ls -qf dangling=true
```

```
docker ps -a -q -f status=exited
docker images -f "dangling=true" -q
```


TODO:
```
docker service ls
docker node ls
docker system events 
```

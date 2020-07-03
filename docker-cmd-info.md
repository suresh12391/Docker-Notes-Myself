#### Docker Commands:
docker -v
docker ps
docker ps -a
docker kill {ID}
docker images
docker images --filter reference=bulletinboard
docker run {IMAGE_NAME}
docker container list
docker container prune (Remove stopped container)
docker container logs {CONTAINER_NAME}
docker exec -it {CONTAINER_NAME} /bin/bash;
docker exec -u {USER_NAME} -it {CONTAINER_NAME} /bin/bash;
docker inspect {CONTAINER_ID} | grep HostPort


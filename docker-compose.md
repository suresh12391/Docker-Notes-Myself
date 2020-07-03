#### Docker-Compose Commands:
docker-compose -v
docker-compose up
docker-compose down
docker-compose -f {COMPOSE_YAML_FILE}.yml up -d
sudo docker-compose run web django-admin startproject compose-example .



Finally, execute the below comment to go into the container.

docker run -d --name=test-mysql --env="MYSQL_ROOT_PASSWORD=mypassword" -P mysql

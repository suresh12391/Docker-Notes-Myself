#### Docker-Compose Commands:
```
docker-compose -v
docker-compose -f {COMPOSE_YAML_FILE}.yml up -d
docker-compose up
docker-compose stop
docker-compose {COMPOSE_YAML_FILE}.yml down
docker-compose run web django-admin startproject compose-example .
```


Finally, execute the below comment to go into the container.

```
docker run -d --name=test-mysql --env="MYSQL_ROOT_PASSWORD=mypassword" -P mysql
docker exec -u docker-name -it abc /bin/bash
```


[В начало](README.md)

# Docker Compose

#### Удалить volume
```sh
# Stop and remove container's using the target volume
docker-compose stop NAME_OF_CONTAINER

# We need the force flag, "-f", as the container is still bound to the volume
docker-compose rm -f NAME_OF_CONTAINER

# Next find your volume name in the following list
docker volume ls

# Finally remove the volume
docker volume rm VOLUME_NAME
```
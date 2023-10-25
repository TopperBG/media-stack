# media-stack
- Install **docker-compose** script
```
sudo curl -L "https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```
 
- Build containers with .yml file and detach from containers
```
docker-compose up -d
```
or if your .yml is not standart (eg. docker-compose.yml) name:
```
docker-compose --file your-docker-compose-file.yml up -d
```
or don't want to run a container, for example portainer:
```
docker-compose up --scale portainer=0 -d
```

- Check builded stack
```
docker-compose ps
docker-compose start
docker-compose start service
docker-compose stop
docker-compose stop service
docker-compose logs -f
docker-compose logs -f service
```
- Remove all containers in stack (NOTE: all containers should be stopped with docker-compose stop)
```
docker-compose stop
docker-compose rm
```

- If you edit your docker-compose.yml should rebuild whole stack
```
docker-compose up -d --force-recreate
```
or recreate just one of services
```
docker-compose create service --force-recreate --remove-orphan
```

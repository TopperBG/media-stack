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
or if your .yml is not standart docker-compose.yml name:
```
docker-compose --file your-docker-compose-file.yml up -d
```

- Check builded stack
```
docker-compose ps
docker-compose start
docker-compose stop
docker-compose logs -f
```

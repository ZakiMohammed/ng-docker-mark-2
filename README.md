# NgDocker - Mark 2

Gzip project for Angular and Docker powered by Cirrus UI.

## Build Docker Image and Run Docker Container

```
# build image
docker build -t ng-docker:mark-2 .

# run container
docker run -p 3300:80 --name ng-docker-mark-2-container-1 ng-docker:mark-2

# list images
docker image ls

# stop container
docker stop ng-docker-mark-2-container-1

# remove container
docker rm ng-docker-mark-2-container-1
```
# NgDocker - Mark 2

Check out the CodeOmelet blog post for this project.

Link: https://codeomelet.com/posts/gzip-dockerized-angular-app-with-nginx-ngdocker
___

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

## Add Web Pack Bundle Analyzer

Install package:
```
npm i webpack-bundle-analyzer -D
```

Add commands:
```
"scripts": {
  "build:prod-stats": "ng build --configuration production --stats-json",
  "analyze": "npm run build:prod-stats && webpack-bundle-analyzer dist/ng-docker-mark-2/stats.json",
}
```

Run command:
```
npm run analyze
```
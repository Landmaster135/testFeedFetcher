# FeedFetcher_Development
This repository is to test "[feed-fethcher](https://github.com/Landmaster135/feed-fetcher)".

# Test

## Build Docker

```dosbatch
# DockerイメージをBuildする
docker build -t my-nodejs-app .
# Dockerイメージを起動する
docker run -it --rm --name my-running-app my-nodejs-app
```

## Test with Docker

### Execute in the machine via docker image.

```shell
npm run start
```

### Execute in the windows machine while the machine being booted by docker.

```dosbatch
docker ps
docker cp <container ID>:/usr/app/testtest.md .
```

## Test with Jest
Put test file into `__test__` folder to test with Jset.
Input this command to test with jest.

```dosbatch
npx jest
```

# Docker Push
## Push to Docker Hub.

### check whether login docker hub or not.
```shell
echo a | docker login
```

#### Answer in the case logged in.
```shell
$ echo a | docker login
　Authenticating with existing credentials...
　Login Succeeded
$ echo $?
　0
```

#### Answer in the case not logged in.
```shell
$ echo a | docker login
　Error: Cannot perform an interactive login from a non TTY device
$ echo $?
　1
```

### docker login
```shell
docker login --username="" --password=""
```

### image ls
```shell
docker image ls
```

### tag
```shell
docker tag my-nodejs-app:latest landmaster135/build-nodejs-in-ubuntu:latest
```

### push
```shell
docker push landmaster135/build-nodejs-in-ubuntu:latest
```

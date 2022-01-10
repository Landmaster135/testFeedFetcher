# FeedFetcher_Development
This README.md file shows about the development for "FeedFethcher".

# Test

## Build Docker

```dosbatch
# DockerイメージをBuildする
docker build -t my-nodejs-app .
# Dockerイメージを起動する
docker run -it --rm --name my-running-app my-nodejs-app
```

## Test with Docker

### Execute in the machine by docker.

```shell
npm run start
```

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

```

### push
```shell

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

# Memo of index.js

## writeFeedToText()

![](memo_writeFeedToText.jpg)

# docker-springboot

Docker image for Spring Boot with openjdk 8.

## Description

Spring Boot is the starting point for building all Spring-based applications. Spring Boot is designed to get you up and running as quickly as possible, with minimal upfront configuration of Spring.

## Build

You can pull the image from `hub.docker.com`.

```sh
$ docker pull bingozb/springboot
```

Or, you can build with source repository by yourself.

```sh
$ git clone https://github.com/bingozb/docker-springboot.git
$ cd docker-springboot
$ docker build -t bingozb/springboot .
```

## Usage

Run the container and volume your fat jar to `/app/app.jar`.

e.g.:

```sh
$ docker run --restart always -d \
--name springboot \
-p 8080:8080 \
-v /path/to/app.jar:/app/app.jar \
bingozb/springboot
```

## TODO

Maven and Gradle support, if they are necessary.


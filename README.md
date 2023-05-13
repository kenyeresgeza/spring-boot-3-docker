# Spring Boot 3 with Docker

Simple overview how to create a Spring Boot 3 application with a custom Docker file 

## Description

Spring Boot 3, REST, Java 17

## Getting Started

### Dependencies

* Java 17
* Docker

### Installing

* Set Java 17
```
sudo update-alternatives --config java (select Java 17)
```
* Build application (you should use gradle 7.3 version)
```
gradle clean bootjar
```
* Create Docker image
```
gradle clean bootjar
```
* Create Docker image
```
docker build --build-arg JAR_FILE=build/libs/*.jar -t sb3-docker-demo .
```
* Verify Docker image
```
docker images
```

### Executing program

* Run container from sb3-docker-demo image
```
docker run -p 8585:8080 sb3-docker-demo
```
* Test application
```
http://localhost:8585/greeting?name=John
```

## Author

Kenyeres Géza
https://hu.linkedin.com/in/g%C3%A9za-kenyeres-17341631

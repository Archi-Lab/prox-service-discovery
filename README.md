# PTB Service Discovery
The purpose of this service is to provide a service discovery where clients can register themselves and look up how to reach other clients (e.g. host and port).

## Installation
```
mvn clean install
```
Executes the [Maven default lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html) up to the install phase. During package phase a runnable JAR is created and during install phase a docker image is build.

## Usage
```
docker-compose -f docker-compose-service-discovery.yml up
```
Starts a Docker container based on the compose file and the image. A Docker network named `ptb` is required for the communication between services:
```
docker network create ptb
```
It is also possible to run the JAR directly with specific Spring profiles:
```
java -jar -Dspring.profiles.active=local target/service-discovery-0.0.1-SNAPSHOT.jar
```

## Documentation
You can view the full documentation under the following [GitHub Wiki](https://github.com/Archi-Lab/ptb-documentation/wiki).

## Contributing

## About the Team
This service is currently developed by the PTB Team composed of students from [TH Köln](https://www.th-koeln.de/):

- Julian Lengelsen ([@jlengelsen](https://github.com/jlengelsen))
- Mansoor Rahmati ([@ManSoorSour](https://github.com/ManSoorSour))
- Jan Seidler ([@janseidler](https://github.com/janseidler))

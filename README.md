FROM openjdk:8
EXPOSE 1234
ADD target/spring-boot-docker.jar spring-boot-docker.jar 
ENTRYPOINT ["java","-jar","/spring-boot-docker.jar"]


# spring-boot-dockerize
How to Dockerize Spring Boot Application 

first go to location 
$ docker -v


# Build Docker Image 
$ docker build -t spring-boot-docker.jar .

# Check Docker Image 
$ docker image ls

# Run Docker Image 
$ docker run -p 1234:8080 spring-boot-docker.jar

In the run command, we have specified that the port 8080 on the container should be mapped to the port 1234 on the Host OS.

localhost:1234/info

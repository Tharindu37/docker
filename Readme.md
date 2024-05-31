### Install Docker (EC2)
```
sudo yum update -y
sudo yum install docker -y
docker --version
sudo systemctl start docker
sudo systemctl status docker
docker images
sudo docker images
docker info
sudo docker info
sudo usermod -aG docker ec2-user
docker images
exit
docker images
sudo systemctl enable docker
```

### Docker Commands
```
docker -v
docker info
docker images
```
```
docker search ubuntu
```
```
docker pull ubuntu
docker pull ubuntu:22.04
```
```
docker --help
```
```
docker run -it ubuntu
docker run -it --name myUbuntu ubuntu
ctrl+p+q
```
```
docker ps
docker ps -a
docker ps -q
docker ps -qa
```
```
docker exec -it a2e223a32bf /bin/bash
```
```
docker commit -m "filget image" a2e223a32bf filget_41:v1
```
```
docker rm -f a2e223a32bf
```
```
docker stop a2e223a32bf
docker rm a2e223a32bf
```
```
docker logs a2e223a32bf
docker logs -f a2e223a32bf
docker logs -f --tail 1 a2e223a32bf
```
```
docker rmi ubuntu
docker rmi -f ubuntu
docker rmi ubuntu ubuntu:22.04
docker rmi -f ubuntu ubuntu:22.04
```
```
docker push ubuntu:v1
```
```
docker tag ubuntu:v1 tharindu37/ubuntu:v1
docker full tharindu37/ubuntu:v1
```
```
docker login
```
```
docker kill <containername/containerid>
docker stop <containername/containerid>
docker start <containername/containerid>
```
### Dockerfile
It's plain text file it contains set of instructions to run application
 --> os
 --> jdk
 --> copy
 --> javac HelloWorld.java
 --> java HelloWorld
```
FROM --> define a base image ex: FROM ubuntu:20.04 ex: FROM openjdk
ENV --> environment
ARG --> arguments (this instruction can define before FROM)
EXPOSR --> documentation about ports are using in your application
WORKDIR --> create folder and cd
LABEL | MAINTAINER --> author
RUN --> any commands to be run at the of build
COPY --> copy the files from src to dest ex: COPY HelloWorld.java HelloWorld.java
ADD --> copy the files from src to dest
VOLUME --> to peristance our container data
USER --> which user
ONBUILD --> triggers
HEALTHCHECK --> to check application is healthy or not
CMD --> executables
STOPSIGNAL --> 
ENTRYPOINT --> executables ex: java HelloWorld
```

### Port forwarding (EC2)
```
docker pull tutum/hello-world
docker images
docker run -d --name webapp tutum/hello-world
dokcer ps
```
Go to Security Groups
```
docker exec -it <containerid> /bin/sh
curl http://localhost:80
exit
```
```
docker exec -it <containerid> /bin/sh
netstart -nlpt
exit
```
```
docker ps
docker run -d -p 80 --name webapp1 tutum/hello-world
```
Go to Security Groups
```
docker run -d -p 80:80 --name webapp2 tutum/hello-world
docker run -d -p 8081:80 --name webapp3 tutum/hello-world
```
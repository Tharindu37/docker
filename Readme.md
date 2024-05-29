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

### Dockerfile
It's plain text file it contains set of instructions to run application
```
FROM --> define a base image ex: FROM ubuntu:20.04
ENV --> 
ARG
EXPOSR
WORKDIR
LABEL | MAINTAINER
RUN
COPY
ADD
VOLUME
USER
ONBUILD
HEALTHCHECK
CMD
STOPSIGNAL
ENTRYPOINT
```
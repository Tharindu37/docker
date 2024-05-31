# FROM busybox
# RUN apt install openjdk
FROM openjdk
# LABEL name="tharindu lakshan"
# LABEL mail="tharindut520@gmail.com"  
COPY HelloWorld.java .
RUN javac HelloWorld.java
CMD java HelloWorld


# Create Dockerfile (EC2)
# mkdir example_1_java_app
# cd example_1_java_app
# vi HelloWorld.java
# copy and paste the java code
# wq
# ls -lrt
# vi Dockerfile
# copy and paste the docker code
# wq
# docker build -t javaapp:v1 .
# docker images
# docker run -it --name myjavaapp javapp:v1
# vi HelloWorld.java
# edit the java file
# docker build -t javaapp:v1 .
# docker run -it --name myjavaapp javaapp:v1
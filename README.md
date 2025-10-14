# jenkins-installation

# docker-compose.yaml
version: '3.8'
services:
  jenkins:
    image: jenkins/jenkins:2.516.1-lts-jdk21
    privileged: true
    user: root
    ports:
     - 8080:8080
    container_name: jenkins
    volumes:
     - /home/jenkins-vm/Jenkins:/var/jenkins_home    #--> change this path accordingly
     - /var/run/docker.sock:/var/run/docker.sock

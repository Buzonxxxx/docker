#Docker Commands
###Execute
```
# start process
docker run -p 9090:8080 tomcat:latest
(docker run -p host-port:container-port tomcat:latest)

# start process in background
docker run -d -p 9090:8080 tomcat:latest

# enter container
docker exec -it [container ID] /bin/bash
// -it: provide input to the container
```
###Process
```
# list running process
docker ps

# list all process
docker ps -a

# kill process
docker kill [container ID]

# kill all process
docker kill $(docker ps -q)

# stop process
docker stop [container ID]

# stop all process
docker stop $(docker ps -q)
```
###Container
```
# Create container and start
docker create [image name]
docker start -a [image id] // -a: attach, output to terminal

# list container
docker container ls

# Stop container
docker stop [container ID] 

# Kill container 
docker kill [container ID]

# Remove container
docker rm [container ID]

# remove all container
docker rm $(docker container ls -aq)
```
###Image
```
# remove img
docker rmi -f tomcat

# remove all image
docker rmi $(docker images -a -q)

# build image
docker build . 

# build specific Docker file
docker build -f Dockerfile.dev .

docker build -t {image_name} [PATH]
//e.g docker build -t buzonliao/redis:latest 
```
###Others
```
# Logs
docker logs [CONTAINER ID]

# Delete all stopped containers/build cache/not used networks/dangling images
docker system prune

# Volume mapping
docker run -v /opt/datadir:/var/lib/mysql mysql

# Inspect
docker inspect [CONTAINER ID]

# Jenkins example
docker run -p 80:8080 -v /root/my-jenkins-data:/var/jenkins_home -u root jenkins
docker exec [CONTAINER ID] cat /var/jenkins_home/secrets/initialAdminPassword
```
###Docker Compose
```
# run image
docker-compose up 

# building image and run
docker-compose up --build

# stop and remove Container
docker-compose down

# List all running processes
docker-compose ps
```







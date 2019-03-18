# Commands

# create volume
docker volume create vol-temporary

# list the volume
docker volume ls 

# create volume while running container
docker run -d --volume vol-ubuntu:/tmp ubuntu

# inspect a volume
docker volume inspect vol-temporary

# remove a volume
docker volume rm vol-ubuntu

# creating container with volume
docker run -itd --name cont-ubuntu --volume vol-ubuntu:/var/log ubuntu:16.04

# insepcting volume of a container
docker container inspect --format "{{json .Mounts}}" cont-ubuntu | python -m json.tool

# executing a container and do certain changes 
docker exec -it cont-ubuntu bash

# check volume in ubuntu
cd /var/lib/docker/volumes/<vol-name>

#check volume in mac
screen ~/Library/Containers/com.docker.docker/Data/com.docker.driver.amd64-linux/tty  


cd /var/lib/docker/volumes/<vol-name>


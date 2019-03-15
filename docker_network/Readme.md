# Commands

# network create bridge
docker network create --driver bridge my-bridge

# network creat bridge with subnet range
docker network create --driver bridge --subnet=192.168.0.0/16 --ip-range=192.168.5.0/24  my-bridge-1

# connect running container
docker network connect my-bridge-1 cont_expose

# disconnect
docker network disconnect my-bridge-1 cont_expose

# inspect bridge
docker network inspect my-bridge-1

# inspect the container
docker container inspect cont_expose

# run without connecting
docker container run -itd --network host --name cont_ubuntu ubuntu:16.04




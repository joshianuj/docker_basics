# Commands

# build image
docker build -t img_apache .

# list image
docker images

# run image as container and auto remove when stopped
docker run -itd --rm --name cont_apache -p 8080:80 img_apache

# execute container
docker exec -it img_apache bash
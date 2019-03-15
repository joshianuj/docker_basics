# Commands

# build image
docker build -t img_expose .

# list image
docker images

# run image as container and auto remove when stopped
docker run -itd --rm --name cont_expose -p 8080:80 img_expose

# execute container
docker exec -it cont_expose bash
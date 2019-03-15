# Commands

# build image
docker build -t image_run-env .

# run image as container
docker run -itd --name cont_run-env img_run-env

# execute container
docker exec -it cont_run-env bash
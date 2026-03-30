# docker


Docker Install commands
-------------------------
sudo dnf -y install dnf-plugins-core
sudo dnf config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ec2-user

docker images
docker build -t from:1.0.0 .
naveenkumarvelanati


docker build -t <image_name:tag> .
docker images
docker run -d -p <host_port>:<container_port> --name <container_name> <image_name>
EX: docker run -d -p 8080:80 --name my-nginx nginx
docker container ls
docker ps -a
docker inspect <container_id> # Docker container details
docker exec -it <container_id> bash # Login to docker container
EX: docker exec -it my-container sh
docker stop <container_id>
docker rm <container_id>
docker rmi <image_id> or docker rmi <image_name:tag>

# Docker tag's and push to docker hub
docker tag <image_name:tag> <dockerhub_username>/<image_name:tag>
docker tag from:1.0.0 naveenkumarvelanati/from:1.0.0
docker push naveenkumarvelanati/from:1.0.0
# teste123
docker build -t meres-app .
docker network create meres-rede
docker volume create meres-volume 
docker tag meres-app lucasfreire97/meres-app
docker run --name meres-container -v meres-volume:/app -p 8090:8090 --network meres-rede meres-app

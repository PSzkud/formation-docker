


docker network create -d bridge hub

docker run --network hub -d --name db training/postgres
docker run --network hub -d -P --name web training/webapp python app.py

docker exec web ping db
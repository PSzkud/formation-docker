docker network create pgadminnet

docker run -d --name demopgadmin -e POSTGRES_PASSWORD=mypasword -v demopgadmin:/var/lib/postgresql/data --network pgadminnet postgres

docker run -d -p 5002:80 --name pgadmin4 -e PGADMIN_DEFAULT_PASSWORD=mypassword -e PGADMIN_DEFAULT_EMAIL=pierre.szkudlapski@labom2iformation.fr --network pgadminnet dpage/pgadmin4


docker run -d -it --name db -v ${pwd}:/app training/postgres

docker run -d -it --name dbtp5 -e POSTGRES_PASSWORD=postgres -p 5432:5432 -d -v ${pwd}:/app postgres
docker exec -it dbtp5 bash

# En route sur le conteneur
psql -U postgres

# Dans Postgres
\dt
\c <nom_db>

CREATE TABLE table_test ( column1 int, column2 int, column3 int);
INSERT INTO table_test VALUES (1, 2, 3);
SELECT * FROM table_test;




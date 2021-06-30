# POSTGRES

- docker volume create --name postgres_data
- docker run --name my_postgres_container -e POSTGRES_PASSWORD=root -v postgres_data:/var/lib/postgresql/data -p 5432:5432 -d postgres

- docker run -d --name posttest postgres:alpine -e POSTGRES_PASSWORD=root -p 5432:5432
- docker exec -it postgres_container psql -U postgres

<p align="center">
   <img src="https://i.imgur.com/q1ueccH.png" width="300">
</p>

# Description

Docker using compose, configuration file with environment variables and creating a container,
in addition the data are present on the local machine even after restart or re created the container :

- postgres:12

# Postgres Container Configuration

1. Expose port

   - 5432

2. Volume (Note: check if in the docker configuration -> shared drivers, the units are enabled)

   - Application database: ./docker/postgres/data -> /var/lib/postgresql/data
   - Automatically create schema: ./docker/schema.sql -> /docker-entrypoint-initdb.d/0.schema.sql

# How to use

1. Clone the repository using the command:

```
$ git clone https://github.com/jadilson12/docker-compose-postgres
```

2. Enter the folder docker-compose-postgres copy the files

```
$ cp env-example .env
$ cp docker-compose.yml-example docker-compose.yml
```

3. Run your container:

```
$ docker-compose up -d
```

4. Access the container shell:

```
$ docker exec -it app-database sh
```

## Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/jadilson12/docker-compose-postgres/issues).

## Show your support

Give a ⭐️ if this project helped you!

## Author

Jadilson Guedes <jadilson12@gmail.com>  
License MIT <https://jadilson12.mit-license.org/>

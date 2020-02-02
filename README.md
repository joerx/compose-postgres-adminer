# Compose Stack for Postgres and Adminer

Provides a simple docker-compose env running PostgresSQL and [adminer](https://www.adminer.org/), a minimalist web-based managed GUI

## Usage

Using the default app database name and password:

```sh
docker-compose up
```

Database name will be `myapp`, database password `default`. Admin user/password will be `postgres`/`postgres`

To customize the app database, set the `DB_APP_NAME` and `DB_APP_PASSWORD` variables:

```sh
DB_APP_NAME=lolcatz DB_APP_PASSWORD=s3cr3t docker-compose up
```

Note: once the database has been initalized, setting these vars will have no effect. To reset, run `docker-compose down -v` to delete the DB volume. Unsurprisingly this will result in loss of all data.

## pgbouncer

docker image for pgbouncer based off of ubuntu:14.04

To pull this image: docker pull unicolet/ubuntu-pgbouncer

Example usage:

```sh
docker run -it -rm --net=host -e PG_PORT_5432_TCP_ADDR=1.2.3.4 -e PG_PORT_5432_TCP_PORT=5432 -e PG_ENV_POSTGRESQL_USER=user -e PG_ENV_POSTGRESQL_PASS=secret  unicolet/pgbouncer
```

pgbouncer can then be accessed locally, for example at `localhost:6432`.

This image to work requires a link (named pg) to a postgres container or manually configured environment variables as follows:

**Mandatory**

PG_PORT_5432_TCP_ADDR

PG_PORT_5432_TCP_PORT

PG_ENV_POSTGRESQL_USER

PG_ENV_POSTGRESQL_PASS

**Optional**

PG_ENV_POSTGRESQL_MAX_CLIENT_CONN (default: 10000)

PG_ENV_POSTGRESQL_DEFAULT_POOL_SIZE (default: 400)

PG_ENV_POSTGRESQL_SERVER_IDLE_TIMEOUT (default: 240)

PG_POOL_MODE (default: session)

PG_LOG_VERBOSE (default: 0)

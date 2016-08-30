# docker-zipkin-dependencies

This repository contains the Docker build definition and release process for
[openzipkin/zipkin-dependencies](https://github.com/openzipkin/zipkin-dependencies).

The zipkin dependencies job pre-aggregates data such that `http://your_host:9411/dependency` shows links
between services.

## Running

To use MySQL as storage, there are some environment variables need to be set to docker container:  
* STORAGE_TYPE=mysql
* MYSQL_HOST=xx.xx.xx.xx (default is localhost)
* MYSQL_USER=xxx (default is zipkin)
* MYSQL_PASS=xxx (default is zipkin)
* MYSQL_PORT=xxx (default is 3306)
* MYSQL_DB=xxx (default is zipkin)

### On-demand
To process all spans since midnight UTC, run the default entrypoint of this image pointed at your storage backend.

```bash
$ docker run ... zipkin-dependencies
```

### Cron
To process spans since midnight every hour, and all spans each day, change the entrypoint to cron.

```bash
$ docker run ... zipkin-dependencies sh -c 'crond -f'
```


<img src='https://user-images.githubusercontent.com/1423657/99822833-f9504780-2b53-11eb-8b28-99484eab6157.png' width=250>

## [cLoki](https://github.com/lmangani/cLoki) + Clickhouse using S3/MINIO storage

This docker compose bundle will spin up a cLoki + Clickhouse stack w/ MINIO/S3 object storage

For more details about Clickhouse and S3 storage support check out this [Altinity Blog](https://altinity.com/blog/clickhouse-and-s3-compatible-object-storage) and the [relevant documentation](https://clickhouse.com/docs/en/engines/table-engines/mergetree-family/mergetree/#table_engine-mergetree-s3)

#### THIS EXAMPLE IS INTENDED FOR TESTING PURPOSES!


## Components

#### Core
* cLoki [yml](https://github.com/metrico/cloki-docker-s3/blob/main/cloki.yml)
* clickhouse-server [yml](https://github.com/metrico/cloki-docker-s3/blob/main/clickhouse-service.yml)
* minio [yml](https://github.com/metrico/cloki-docker-s3/blob/main/minio-service.yml)
#### Add-Ons
* pastash [yml](https://github.com/metrico/cloki-docker-s3/blob/main/pastash.yml)

### Setup

```bash
docker-compose up
```

#### Usage

* Connect your Grafana instance to the Loki API on port `3100`
* Start browsing your cheaper tags and labels

##### AWS S3
* Use with any S3 compatible storage using the settings in [storage.xml](https://github.com/metrico/cloki-docker-s3/blob/main/configs/clickhouse/config.d/storage.xml)

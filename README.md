<img src='https://user-images.githubusercontent.com/1423657/147935343-598c7dfd-1412-4bad-9ac6-636994810443.png' style="margin-left:-10px" width=220>

## [qryn](https://github.com/metrico/qryn) + Clickhouse using S3/MINIO storage

This docker compose bundle will spin up qryn + Clickhouse stack w/ MINIO/S3 object storage

For more details about Clickhouse and S3 storage support check out this [Altinity Blog](https://altinity.com/blog/clickhouse-and-s3-compatible-object-storage) and the [relevant documentation](https://clickhouse.com/docs/en/engines/table-engines/mergetree-family/mergetree/#table_engine-mergetree-s3)

#### THIS EXAMPLE IS INTENDED FOR TESTING PURPOSES!


## Components

#### Core
* qryn [yml](https://github.com/metrico/cloki-docker-s3/blob/main/qryn.yml)
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

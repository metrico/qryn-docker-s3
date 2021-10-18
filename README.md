<img src='https://user-images.githubusercontent.com/1423657/99822833-f9504780-2b53-11eb-8b28-99484eab6157.png' width=250>

# cLoki + Clickhouse using S3/MINIO storage

#### THIS EXAMPLE IS INTENDED FOR TESTING PURPOSES!

This docker bundle will spin up a cLoki + Clickhouse stack w/ S3 or MINIO object storage

## Components

#### Core
* clickhouse-server
* cLoki
* minio
#### Add-Ons
* pastash
* grafana

## Setup

```bash
docker-compose up
```

#### Usage

* Connect your Grafana instance to the Loki API on port 3100
* Start browsing tags and labels

#### AWS S3
To use with S3 replace the settings in `configs/clickhouse/config.d/storage.xml`

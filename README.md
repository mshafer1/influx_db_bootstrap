# InfluxDB BootStrap

To make bringing up an [InfluxDB](https://docs.influxdata.com/influxdb/v2) extremely simple.

# Steps:

1. Clone repo

`git clone https://github.com/mshafer1/influx_db_bootstrap.git influx_db` 

1. CD into repo

`cd influx_db`

1. Use text editor to configure .env

Required variables:
```bash
# .env
DOCKER_INFLUXDB_INIT_MODE=setup
DOCKER_INFLUXDB_INIT_USERNAME=my-user
DOCKER_INFLUXDB_INIT_PASSWORD='...'
DOCKER_INFLUXDB_INIT_ORG=my-org
DOCKER_INFLUXDB_INIT_BUCKET=my-bucket
V1_DB_NAME=v1-db
V1_RP_NAME=v1-rp
V1_AUTH_USERNAME=v1-user
V1_AUTH_PASSWORD='...'
TZ='...'
```

(replacing `...` values with your own secret values, keeping quotes if needed)

1. Bring up server

`docker compose up -d`

1. Login to `http://localhost:8086` (using `my-user` and what you set the password to above) and enjoy


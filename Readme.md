# loki-stack

A docker-compose stack with loki in microservice mode.

```sh
docker-compose up --scale loki-querier=3 --scale loki-distributor=3 --scale loki-ingester=2
```

## Services

* Loki in microservice mode
* Grafana - add Loki datasource http://queriers
* Promtail tailing `/var/log/`
* Traefik load balancer for distributors and queriers
* Scylla as index store
* Minio as block store
* Consul as keyring store

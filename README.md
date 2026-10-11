# Monitoring Stack

Monitoring stack based on Prometheus, Grafana, Node Exporter, cAdvisor and
Alertmanager.

## Project structure

```text
.
├── config/
│   ├── alertmanager/
│   │   └── alertmanager.yml
│   └── prometheus/
│       ├── alert.rules.yml
│       └── prometheus.yml
├── docker-compose.yml
├── .gitignore
└── README.md
```

## Start the stack

```bash
docker compose up -d
```

## Access services

| Service | URL |
| --- | --- |
| Prometheus | http://localhost:9091 |
| Grafana | http://localhost:3001 |
| Node Exporter | http://localhost:9101 |
| cAdvisor | http://localhost:8080 |
| Alertmanager | http://localhost:9093 |

The host ports for Prometheus, Grafana and Node Exporter are intentionally
different from their defaults because the host installation already uses
ports `9090`, `3000` and `9100`.

## Stop the stack

```bash
docker compose down
```

Persistent Prometheus and Grafana data are stored in Docker named volumes.

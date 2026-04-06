# AGENTS.md

## Purpose
Public self-hosted deployment template for monitoring stack (Prometheus + Grafana).

## Repository Role
- Category: `*-self-hosted` (public GitHub repository).
- Related local stack: `../monitoring-docker`.
- Main entrypoint: `docker-compose.yml`.

## Stack Summary
- Services: `prometheus`, `grafana`.
- Exposed ports: `9090` (Prometheus), `3000` (Grafana).
- External network: `shared_network`.

## Data and Config
- Prometheus config: `./prometheus/prometheus.yml`.
- Prometheus data: `./data/prometheus`.
- Grafana provisioning: `./grafana/provisioning`.
- Grafana data: `./data/grafana`.

## Operations
- Restart stack: `./restart-docker.sh`.
- Update images and restart: `./update-docker.sh`.

## AI Working Notes
- Keep Grafana admin credentials in `.env` (`GRAFANA_ADMIN_USER`, `GRAFANA_ADMIN_PASSWORD`).
- Treat provisioning files as declarative source of truth.
- Preserve persistent data mounts to avoid dashboard and metric loss.

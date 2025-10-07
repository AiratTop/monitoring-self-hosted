# Monitoring Self-Hosted with Docker

This repository provides a Docker Compose setup for running a self-hosted monitoring stack using [Prometheus](https://prometheus.io/) and [Grafana](https://grafana.com/).

## Features

- **Works out of the box:** Just configure the `.env` file and run a start script.
- **Pre-configured:** Prometheus is set up to scrape itself, and Grafana already has Prometheus added as a data source.
- **Ready-to-use Scripts:** Includes simple scripts to start, restart, and update the application.
- **Persistent Data:** Data for both services is stored in local directories to ensure persistence across restarts.

## Prerequisites

- Docker and Docker Compose installed.
- A `.env` file with the required environment variables (you can use the one provided).

## Usage

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/AiratTop/monitoring-self-hosted.git
    cd monitoring-self-hosted
    ```

2.  **Create the shared network:**
    This setup uses a shared network to easily connect to other services. If you haven't already, create the network:
    ```bash
    docker network create shared_network
    ```

3.  **Configure the environment:**
    The `.env` file contains the default admin credentials for Grafana. You can change them if you wish.

4.  **Start the application:**
    ```bash
    docker compose up -d
    ```

5.  **Access the application:**

-   **Prometheus**: [http://localhost:9090](http://localhost:9090)
-   **Grafana**: [http://localhost:3000](http://localhost:3000)

## Usage

The repository includes several scripts to simplify management:

-   **Start:** `docker compose up -d`
-   **Restart:** `./restart-docker.sh`
-   **Update:** `./update-docker.sh` (Pulls the latest Docker images and restarts the services)

## Services

- `prometheus`: The Prometheus monitoring server.
- `grafana`: The Grafana visualization dashboard.

## See Also

Check out other self-hosted solutions:

-   [**postgresql-self-hosted**](https://github.com/AiratTop/postgresql-self-hosted): A simple and robust PostgreSQL setup.
-   [**mysql-self-hosted**](https://github.com/AiratTop/mysql-self-hosted): A self-hosted MySQL instance.
-   [**clickhouse-self-hosted**](https://github.com/AiratTop/clickhouse-self-hosted): High-performance columnar database for analytics.
-   [**metabase-self-hosted**](https://github.com/AiratTop/metabase-self-hosted): Self-hosted Metabase on Docker for business intelligence and analytics.
-   [**qdrant-self-hosted**](https://github.com/AiratTop/qdrant-self-hosted): A vector database for AI applications.
-   [**redis-self-hosted**](https://github.com/AiratTop/redis-self-hosted): A fast in-memory data store, often used as a cache or message broker.
-   [**caddy-self-hosted**](https://github.com/AiratTop/caddy-self-hosted): A modern, easy-to-use web server with automatic HTTPS.
-   [**wordpress-self-hosted**](https://github.com/AiratTop/wordpress-self-hosted): Production-ready WordPress stack with MySQL, phpMyAdmin, and WP-CLI.
-   [**n8n-self-hosted**](https://github.com/AiratTop/n8n-self-hosted): Scalable n8n with workers, Caddy for auto-HTTPS, and backup scripts.
-   [**monitoring-self-hosted**](https://github.com/AiratTop/monitoring-self-hosted): Self-hosted monitoring stack with Prometheus and Grafana.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Author

**Airat Halitov**

- Website: [airat.top](https://airat.top)
- GitHub: [@AiratTop](https://github.com/AiratTop)
- Repository: [monitoring-self-hosted](https://github.com/AiratTop/monitoring-self-hosted)

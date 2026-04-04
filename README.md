Docker Service Discovery and Container Monitoring Dashboard

A lightweight, container‑aware dashboard that automatically discovers all running Docker services and displays real‑time system metrics, per‑container resource usage, and external uptime monitoring. Built with [Homepage](https://gethomepage.dev/), [Glances](https://nicolargo.github.io/glances/), and [Uptime Kuma](https://github.com/louislam/uptime-kuma).

## Key Features

- **Auto‑discovery** – Mounts the Docker socket (read‑only) to list every running container without manual configuration.
- **System & container metrics** – Glances provides per‑container CPU, memory, disk, and network usage.
- **Service uptime tracking** – Uptime Kuma monitors internal and external services, with a widget showing real‑time status.
- **Modular widgets** – Displays system resources (CPU, RAM, disk), search bar, and optional integrations (Grafana, VictoriaMetrics).
- **Secure by design** – Host validation (`HOMEPAGE_ALLOWED_HOSTS`) prevents header injection; Docker socket is read‑only.
- **Infrastructure as code** – All services defined in a single `docker-compose.yaml` with environment variables for secrets.

## Tech Stack

| Component | Purpose |
|-----------|---------|
| [Homepage](https://gethomepage.dev/) | Main dashboard UI, auto‑discovers containers |
| [Glances](https://nicolargo.github.io/glances/) | Real‑time system & container metrics |
| [Uptime Kuma](https://github.com/louislam/uptime-kuma) | Service uptime monitoring & status page |
| Docker Compose | Container orchestration |
| Docker socket | Enables container discovery |

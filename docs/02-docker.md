# 🐳 Docker Platform

> [!NOTE]
>
> **Service:** Docker Engine  
> **Status:** ✅ Operational  
> **Platform:** Debian 12  
> **Hostname:** home-lab  
> **Purpose:** Container Platform for Self-Hosted Infrastructure

---

# 📖 Overview

Docker is the core platform of this Home Lab.

It provides a lightweight and isolated environment for deploying infrastructure services without modifying the base operating system.

Using Docker allows every application to run independently while sharing the same Linux kernel, making deployment, maintenance and updates significantly easier.

Almost every service in this Home Lab is deployed as a Docker container.

---

# 🎯 Objectives

- Deploy a containerized infrastructure.
- Simplify service deployment.
- Improve scalability.
- Isolate applications.
- Reduce maintenance complexity.
- Learn enterprise container management.

---

# 🏗️ Environment

| Component | Value |
|-----------|-------|
| Operating System | Debian 12 |
| Platform | Docker Engine |
| Installation | Native |
| Hostname | home-lab |
| Network Driver | Bridge |
| Compose Support | Docker Compose |

---

# 🌐 Architecture

```text
                  Debian 12
                      │
                Docker Engine
                      │
      ┌───────────────┼────────────────┐
      │               │                │
   Pi-hole       Homepage       Netdata
      │               │                │
      └───────────────┼────────────────┘
                      │
               Uptime Kuma
```

Docker acts as the orchestration layer for every containerized application deployed inside the Home Lab.

Each service runs independently while sharing the same Docker Engine.

---

# ⚙️ Installation

Docker Engine was installed using the official Docker repository for Debian.

Main installation steps included:

- Docker Engine
- Docker CLI
- Docker Compose Plugin

Official documentation:

https://docs.docker.com/engine/install/debian/

---

# 🔧 Configuration

The Docker platform was configured following good infrastructure practices.

## Docker Network

The default Bridge network is currently used.

Future versions of this Home Lab will implement custom Docker networks to isolate services.

---

## Persistent Storage

Persistent Docker volumes are used to preserve application data.

This ensures that services continue operating correctly after updates or container recreation.

---

## Docker Compose

Every deployed application is managed using Docker Compose.

Benefits include:

- Easy deployment
- Easy updates
- Simple backups
- Infrastructure reproducibility

---

# 📦 Current Containers

| Container | Status |
|------------|--------|
| Pi-hole | ✅ Running |
| Homepage | ✅ Running |
| Netdata | ✅ Running |
| Uptime Kuma | ✅ Running |

---

# ✅ Validation

Docker installation was validated using several commands.

## Docker Version

```bash
docker --version
```

Expected result:

- Docker Engine installed successfully.

---

## Running Containers

```bash
docker ps
```

Expected result:

All infrastructure services appear with **Up** status.

---

## Docker Compose

```bash
docker compose version
```

Expected result:

Docker Compose plugin installed successfully.

---

# 📊 Results

Current operational status:

- ✅ Docker Engine Installed
- ✅ Docker Compose Operational
- ✅ Containers Running
- ✅ Persistent Volumes Configured
- ✅ Container Networking Operational

---

# 📸 Screenshots

The following screenshots will be added when remote access to the Home Lab is available.

- Docker Containers
- Docker Networks
- Docker Volumes
- Docker Images
- Docker Compose Deployment

---

# 🧠 Lessons Learned

During this deployment I gained practical experience with containerized infrastructure.

Key takeaways include:

- Difference between containers and virtual machines.
- Docker networking fundamentals.
- Volume persistence.
- Container lifecycle management.
- Docker Compose workflows.
- Infrastructure modularity.
- Easier application maintenance.

---

# 📚 References

- https://docs.docker.com/
- https://docs.docker.com/engine/install/debian/
- Debian Documentation

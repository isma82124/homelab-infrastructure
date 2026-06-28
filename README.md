# 🏠 Home Lab Infrastructure

> **Personal infrastructure laboratory focused on Linux, Docker, networking, monitoring and self-hosted services.**

![Debian](https://img.shields.io/badge/Debian-12-A81D33?logo=debian)
![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?logo=docker)
![Linux](https://img.shields.io/badge/Linux-Debian-FCC624?logo=linux)
![Status](https://img.shields.io/badge/Status-Active-success)
![Documentation](https://img.shields.io/badge/Documentation-Completed-success)
![License](https://img.shields.io/badge/License-MIT-green)

---

# 📚 Table of Contents

- [📖 Overview](#-overview)
- [🎯 Objectives](#-objectives)
- [🏗 Infrastructure](#-infrastructure)
- [📦 Current Services](#-current-services)
- [📖 Documentation](#-documentation)
- [🌐 Network Topology](#-network-topology)
- [📸 Screenshots](#-screenshots)
- [📁 Repository Structure](#-repository-structure)
- [🚀 Roadmap](#-roadmap)
- [🧠 Skills Demonstrated](#-skills-demonstrated)
- [📄 License](#-license)

---

# 📖 Overview

This repository documents the design, deployment, maintenance and continuous improvement of my personal Home Lab infrastructure.

The laboratory was built to gain practical experience with Linux administration, Docker containers, DNS infrastructure, monitoring, networking and self-hosted services.

Every deployed service follows a structured workflow inspired by enterprise infrastructure projects:

- Planning
- Installation
- Configuration
- Validation
- Documentation
- Continuous Improvement

This repository serves as both a technical portfolio and a long-term learning project.

---

# 🎯 Objectives

The main goals of this project are:

- Learn Linux server administration
- Deploy self-hosted infrastructure
- Practice Docker containerization
- Improve networking knowledge
- Deploy monitoring platforms
- Document real infrastructure
- Develop troubleshooting skills
- Build a professional portfolio

---

# 🏗 Infrastructure

| Component | Technology |
|-----------|------------|
| Operating System | Debian 12 |
| Container Platform | Docker Engine |
| Container Orchestration | Docker Compose |
| DNS Filtering | Pi-hole |
| Dashboard | Homepage |
| Infrastructure Monitoring | Netdata |
| Uptime Monitoring | Uptime Kuma |
| Remote Administration | OpenSSH |

---

# 📦 Current Services

| Service | Status | Documentation |
|----------|--------|---------------|
| Debian 12 | ✅ Operational | Base Operating System |
| Docker Engine | ✅ Operational | docs/02-docker.md |
| Pi-hole | ✅ Operational | docs/01-pihole.md |
| Homepage | ✅ Operational | docs/05-homepage.md |
| Netdata | ✅ Operational | docs/03-netdata.md |
| Uptime Kuma | ✅ Operational | docs/04-uptime-kuma.md |

---

# 📖 Documentation

Each deployed service has its own technical documentation.

| Document | Description |
|----------|-------------|
| 📄 01-pihole.md | Local DNS Server and Advertisement Blocking |
| 📄 02-docker.md | Docker Platform Deployment |
| 📄 03-netdata.md | Infrastructure Monitoring |
| 📄 04-uptime-kuma.md | Service Availability Monitoring |
| 📄 05-homepage.md | Infrastructure Dashboard |

Future services will follow the same documentation standard.

---

# 🌐 Network Topology

Current infrastructure:

```text
                    Internet
                        │
                 Cloudflare DNS
                        │
                TP-Link Router
                 192.168.1.1
                        │
              Debian 12 Home Server
                 192.168.1.10
                        │
         ┌──────────────┼──────────────┐
         │              │              │
      Docker         Netdata      OpenSSH
         │
 ┌───────┼──────────────────────────────┐
 │       │              │               │
Pi-hole Homepage    Uptime Kuma    Future Services
```

A detailed infrastructure diagram will be added in future updates.

---

# 📸 Screenshots

Screenshots will be uploaded after secure remote access to the Home Lab becomes available.

Planned screenshots:

- 🛡 Pi-hole Dashboard
- 🏠 Homepage Dashboard
- 📊 Netdata Monitoring
- ❤️ Uptime Kuma Dashboard
- 🐳 Docker Containers

---

# 📁 Repository Structure

```text
homelab-infrastructure/
│
├── README.md
├── LICENSE
│
├── docs/
│   ├── 01-pihole.md
│   ├── 02-docker.md
│   ├── 03-netdata.md
│   ├── 04-uptime-kuma.md
│   └── 05-homepage.md
│
├── diagrams/
│
├── images/
│
└── scripts/
```

---

# 🚀 Roadmap

## ✅ Completed

- Debian 12 Installation
- Docker Engine
- Docker Compose
- Pi-hole
- Homepage
- Netdata
- Uptime Kuma
- Infrastructure Documentation

---

## 🚧 In Progress

- Vaultwarden
- WireGuard VPN
- Documentation Improvements

---

## 📅 Planned

- Authentik
- Grafana
- Prometheus
- Nginx Proxy Manager
- Wazuh SIEM
- Ansible Automation
- Network Automation
- Infrastructure as Code

---

# 🧠 Skills Demonstrated

This project demonstrates practical experience with:

- Linux Administration
- Docker
- Docker Compose
- DNS Infrastructure
- Infrastructure Monitoring
- System Documentation
- Infrastructure Troubleshooting
- Networking Fundamentals
- Service Deployment
- Self-hosted Applications
- Technical Documentation
- Continuous Learning

---

# 📄 License

This project is licensed under the **MIT License**.

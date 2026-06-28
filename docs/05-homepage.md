# 🏠 Homepage Dashboard

---

> [!NOTE]
>
> **Service:** Homepage  
> **Status:** ✅ Operational  
> **Platform:** Docker  
> **Hostname:** home-lab  
> **Purpose:** Home Lab Dashboard

---

# 📖 Overview

Homepage provides a centralized dashboard for accessing every service deployed in the Home Lab.

Instead of remembering multiple IP addresses and ports, all infrastructure services are available from a single web interface.

The dashboard also displays Docker information and system widgets.

---

# 🎯 Objectives

- Centralize infrastructure access.
- Improve usability.
- Organize Home Lab services.
- Display Docker widgets.
- Simplify administration.
- Learn dashboard management.

---

# 🏗 Environment

| Component | Value |
|-----------|-------|
| Operating System | Debian 12 |
| Platform | Docker |
| Port | 3000 |
| Container | homepage |
| Theme | Dark |

---

# 🌐 Architecture

```text
             Homepage
                 │
     ┌───────────┼────────────┐
     │           │            │
 Pi-hole      Netdata    Uptime Kuma
                 │
              Router
```

Homepage acts as the main entry point of the Home Lab.

---

# ⚙ Installation

Homepage was deployed using Docker Compose.

Configuration files:

- docker-compose.yml
- services.yaml
- settings.yaml
- bookmarks.yaml

Official documentation:

https://gethomepage.dev/

---

# 🔧 Configuration

Configured services:

- Pi-hole
- Netdata
- Uptime Kuma
- Router

Dashboard URL:

```

http://192.168.1.10:3000

```

Local DNS:

```

dashboard.casa

```

---

# ✅ Validation

Verify container:

```bash
docker ps
```

Verify dashboard:

```text
http://192.168.1.10:3000
```

Expected result:

Homepage dashboard loads correctly.

---

# 📈 Results

Current operational status:

- ✅ Dashboard Available
- ✅ Docker Widget
- ✅ Infrastructure Links
- ✅ Local DNS Integration
- ✅ Automatic Startup

---

# 📸 Screenshots

Future screenshots:

- Main Dashboard
- Docker Widget
- Services
- Bookmarks

---

# 🧠 Lessons Learned

Key takeaways:

- Dashboard customization.
- Docker integration.
- YAML configuration.
- Infrastructure organization.
- Service centralization.

---

# 📚 References

- https://gethomepage.dev/
- https://github.com/gethomepage/homepage

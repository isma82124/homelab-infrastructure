# ❤️ Uptime Kuma

---

> [!NOTE]
>
> **Service:** Uptime Kuma  
> **Status:** ✅ Operational  
> **Platform:** Docker  
> **Hostname:** home-lab  
> **Purpose:** Service Availability Monitoring

---

# 📖 Overview

Uptime Kuma is the monitoring platform used to verify the availability of all services running in the Home Lab.

It periodically checks infrastructure services and provides alerts when one becomes unavailable.

A local status page is also available for quick infrastructure validation.

---

# 🎯 Objectives

- Monitor service availability.
- Detect outages quickly.
- Validate HTTP services.
- Monitor DNS functionality.
- Learn infrastructure monitoring.
- Centralize service status.

---

# 🏗 Environment

| Component | Value |
|-----------|-------|
| Operating System | Debian 12 |
| Platform | Docker |
| Port | 3001 |
| Container | uptime-kuma |
| Restart Policy | Always |

---

# 🌐 Architecture

```text
            Uptime Kuma
                 │
     ┌───────────┼────────────┐
     │           │            │
 Pi-hole      Homepage     Netdata
     │           │            │
     └───────────┼────────────┘
                 │
              Internet
```

---

# ⚙ Installation

Uptime Kuma was deployed as a Docker container.

Main configuration:

- Docker container
- Persistent volume
- Automatic restart
- Published port 3001

Official documentation:

https://github.com/louislam/uptime-kuma

---

# 🔧 Configuration

Configured monitors:

- Homepage
- Pi-hole
- Netdata
- Router
- Internet
- DNS Resolution

Status page:

```

http://192.168.1.10:3001/status/homelab

```

Dashboard:

```

http://192.168.1.10:3001

```

---

# ✅ Validation

Verify container:

```bash
docker ps
```

Check HTTP response:

```bash
curl -I http://192.168.1.10:3001
```

Expected result:

HTTP 302 Redirect

---

# 📈 Results

Current operational status:

- ✅ Homepage Monitor
- ✅ Pi-hole Monitor
- ✅ Netdata Monitor
- ✅ Internet Monitor
- ✅ Router Monitor
- ✅ DNS Monitor

---

# 📸 Screenshots

Future screenshots:

- Dashboard
- Status Page
- Monitor List
- Uptime Graphs

---

# 🧠 Lessons Learned

Key takeaways:

- HTTP monitoring.
- DNS monitoring.
- Infrastructure availability.
- Service health validation.
- Docker monitoring.

---

# 📚 References

- https://github.com/louislam/uptime-kuma

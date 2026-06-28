# 📊 Netdata Monitoring

---

> [!NOTE]
>
> **Service:** Netdata  
> **Status:** ✅ Operational  
> **Platform:** Debian 12  
> **Hostname:** home-lab  
> **Purpose:** Real-Time Infrastructure Monitoring

---

# 📖 Overview

Netdata is the monitoring platform used in this Home Lab to visualize system performance in real time.

It provides detailed information about CPU usage, memory consumption, disk activity, network traffic, running processes and hardware sensors without requiring manual data collection.

The service runs directly on the Debian host to monitor the physical machine instead of only Docker containers.

---

# 🎯 Objectives

- Monitor server health in real time.
- Detect abnormal resource usage.
- Monitor hardware temperatures.
- Simplify troubleshooting.
- Collect performance metrics.
- Learn infrastructure monitoring.

---

# 🏗 Environment

| Component | Value |
|-----------|-------|
| Operating System | Debian 12 |
| Platform | Native |
| Monitoring Software | Netdata |
| Port | 19999 |
| Hostname | home-lab |
| Sensors | lm-sensors |

---

# 🌐 Architecture

```text
            Debian 12
                 │
          Netdata Service
                 │
      ┌──────────┼──────────┐
      │          │          │
     CPU       Memory      Disk
      │          │          │
      └──────────┼──────────┘
                 │
         Network Interfaces
                 │
          Hardware Sensors
```

Netdata collects system metrics directly from the Linux kernel and displays them through a web interface.

---

# ⚙ Installation

Netdata was installed using the official installation script.

Main installation steps:

- Update Debian packages
- Install required tools
- Download official installer
- Install Netdata
- Enable service

Official documentation:

https://learn.netdata.cloud/docs/netdata-agent/installation/linux

---

# 🔧 Configuration

Hardware sensors were enabled using **lm-sensors**.

Netdata was configured to monitor:

- CPU
- RAM
- Disk
- Network
- Running Processes
- Temperatures

Access URL:

```

http://192.168.1.10:19999

```

---

# ✅ Validation

Verify service:

```bash
systemctl status netdata
```

Open dashboard:

```text
http://192.168.1.10:19999
```

Expected result:

- Netdata dashboard loads successfully.
- System metrics update in real time.

---

# 📈 Results

Current operational status:

- ✅ CPU Monitoring
- ✅ Memory Monitoring
- ✅ Disk Monitoring
- ✅ Network Monitoring
- ✅ Hardware Sensors
- ✅ Real-Time Dashboard

---

# 📸 Screenshots

Future screenshots:

- Dashboard
- CPU Graph
- Memory Usage
- Network Statistics
- Temperature Sensors

---

# 🧠 Lessons Learned

During this deployment I learned:

- Linux monitoring fundamentals.
- Hardware sensor integration.
- Performance analysis.
- Infrastructure observability.
- System troubleshooting.

---

# 📚 References

- https://www.netdata.cloud/
- https://learn.netdata.cloud/

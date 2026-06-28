# 🛡️ Pi-hole Deployment

> [!NOTE]
>
> **Service:** Pi-hole  
> **Status:** ✅ Operational  
> **Platform:** Debian 12  
> **Hostname:** home-lab  
> **Purpose:** Local DNS Filtering and Network-wide Advertisement Blocking

---

# 📖 Overview

Pi-hole was deployed as the first infrastructure service of this Home Lab.

Its primary purpose is to provide local DNS resolution, network-wide advertisement blocking and centralized DNS management for every device connected to the laboratory network.

This service also serves as the foundation for future self-hosted applications by providing reliable local name resolution and centralized DNS control.

---

# 🎯 Objectives

- Deploy a local DNS server.
- Block advertisements and tracking domains.
- Centralize DNS resolution.
- Improve network visibility.
- Build a reliable foundation for future infrastructure services.

---

# 🏗️ Environment

| Component | Value |
|-----------|-------|
| Operating System | Debian 12 |
| Hostname | home-lab |
| Service | Pi-hole |
| IP Address | 192.168.1.10 |
| Gateway | 192.168.1.1 |
| Upstream DNS | Cloudflare |
| Installation Type | Native |

---

# 🌐 Network Architecture

```text
                   Internet
                       │
                Cloudflare DNS
                       │
                TP-Link Router
                 192.168.1.1
                       │
              ───────────────────
                       │
              Debian 12 Server
               192.168.1.10
                       │
                 Pi-hole DNS
                       │
      ┌──────────┬──────────┬──────────┐
      │          │          │          │
   Laptop      Desktop     Phone     Other Devices
```

Pi-hole was configured as the primary DNS server for the entire local network through the TP-Link router DHCP configuration.

Every client connected to the network automatically receives Pi-hole as its DNS resolver.

---

# ⚙️ Installation

Pi-hole was installed on a clean Debian 12 server using the official installation script.

Main installation command:

```bash
curl -sSL https://install.pi-hole.net | bash
```

Main installation options:

- Upstream DNS: Cloudflare
- Query Logging: Enabled
- Privacy Mode: Show Everything
- Blocklist: StevenBlack Unified Hosts
- Static IPv4 Address: 192.168.1.10

---

# 🔧 Configuration

After installation, several configurations were applied to integrate Pi-hole into the Home Lab infrastructure.

## Static IP

The server was configured with a static IP address to ensure DNS availability.

```
192.168.1.10
```

---

## Router Configuration

The TP-Link router DHCP server was configured to distribute Pi-hole as both the Primary and Secondary DNS server.

| Setting | Value |
|----------|-------|
| DHCP | Enabled |
| Gateway | 192.168.1.1 |
| Primary DNS | 192.168.1.10 |
| Secondary DNS | 192.168.1.10 |

This guarantees that every client joining the network automatically uses Pi-hole.

---

## Blocklists

The default StevenBlack Unified Hosts list was configured during installation.

The objective is to block:

- Advertisements
- Tracking domains
- Malicious domains

---

## Backups

Two backup strategies were implemented.

- Manual backup
- Pi-hole Teleporter Backup

This allows rapid recovery in case of system failure.

---

# ✅ Validation

Several tests were performed to verify proper operation.

## DNS Resolution Test

```bash
nslookup google.com
```

Expected result:

- Successful DNS resolution

---

## Advertisement Blocking Test

```bash
nslookup doubleclick.net
```

Expected result:

```
0.0.0.0
```

This confirms that Pi-hole is actively blocking known advertisement domains.

---

## Service Status

```bash
pihole status
```

Expected result:

- FTL Running
- DNS Active
- Blocking Enabled

---

# 📊 Results

The deployment was successfully completed.

Current operational status:

- ✅ Local DNS Server
- ✅ Advertisement Blocking
- ✅ Router Integration
- ✅ DHCP Integration
- ✅ Network-wide DNS Filtering
- ✅ Backup Strategy Implemented

---

# 📸 Screenshots

The following screenshots will be added once remote access to the Home Lab is available.

- Pi-hole Dashboard
- Query Log
- DNS Settings
- Blocklists
- Dashboard Statistics

---

# 🧠 Lessons Learned

During this deployment I learned several important concepts regarding Linux server administration and DNS infrastructure.

Key takeaways include:

- Importance of Static IP addressing.
- DNS resolution workflow.
- DHCP and DNS integration.
- Basic Linux service administration.
- Backup and recovery procedures.
- Network-wide advertisement blocking.
- Infrastructure documentation best practices.

---

# 📚 References

- https://pi-hole.net/
- https://docs.pi-hole.net/
- Debian Documentation

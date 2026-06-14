# Kevin Pranata - IT Portfolio

## 📌 Project Overview
This project documents how to install and configure a stable infrastructure using **Debian 13 (Trixie)** in a virtual environment (VMware). The goal is to build a fast, secure, and text-only (CLI) server for school and enterprise labs.

---

## 🗺️ Network Information
* **Hypervisor:** VMware Workstation Pro
* **Operating System:** Debian 13 (Trixie) - Server Mode (No GUI)
* **IP Configuration:** Static IP

| Component | Configuration Value |
| :--- | :--- |
| **Server IP** | `192.168.10.10 /24` |
| **Gateway** | `192.168.10.1` |
| **DNS Server** | `8.8.8.8` |
| **Services** | SSH, Nginx Web Server |

---

## 🛡️ Server Security (Hardening)
To protect the server, I configured these security settings:
1. **Change SSH Port:** Moved the default port from `22` to `2202` to block random attacks.
2. **Disable Root Login:** Disabled direct login for the `root` user via SSH.
3. **Firewall:** Used `UFW` to open only necessary ports (Port 80 for Web and Port 2202 for SSH).

---

## 🛠️ Step-by-Step Configuration

### Step 1: Configure Network Interface
Open and edit the network file at `/etc/network/interfaces`:
```bash
auto ens33
iface ens33 inet static
    address 192.168.10.10
    netmask 255.255.255.0
    gateway 192.168.10.1
```
*Run `systemctl restart networking` to apply changes.*

### Step 2: Install Nginx Web Server
Update the repository and install Nginx:
```bash
apt update && apt upgrade -y
apt install nginx -y
```

---

## 📊 Proof of Concept (Screenshots)
*(Lab screenshots will be added here later)*

---

## 📬 Contact
* **Name:** Kevin Pranata
* **School:** SMK Telkom
* **LinkedIn:** [Insert your LinkedIn link here later]

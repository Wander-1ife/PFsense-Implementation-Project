# 🔐 PFsense Implementation Project


## 📘 Overview

This project demonstrates the end-to-end implementation and configuration of **PFsense**, a powerful open-source firewall/router distribution based on FreeBSD. The goal is to establish a secure and controlled virtual network environment using **Windows 11** and **Oracle VirtualBox**, providing hands-on experience in network security, firewall configuration, user access management, and traffic routing.

---

## 📑 Table of Contents

1. [Abstract](#abstract)  
2. [Introduction](#introduction)  
3. [Policy Implementation](#policy-implementation)  
4. [Configuration](#configuration)  
   - Installation of PFsense  
   - Network Setup (LAN/WAN)  
   - Web Access and Dashboard Customization  
   - Firewall Rules and Routing  
   - SSH and Port Configuration  
   - Package Installation  
   - User Management  
5. [Conclusion](#conclusion)  
6. [References](#references)

---

## 🧩 Abstract

This project simulates the deployment of PFsense to secure and manage a virtualized network. It involves assigning static and dynamic IPs, enabling DHCP, applying firewall rules, configuring port forwarding, activating SSH access, and managing system users. The implementation focuses on enforcing security policies and monitoring network behavior within a contained lab environment.

---

## 🚀 Introduction

PFsense is a robust and feature-rich firewall/router OS used for securing and routing network traffic. Utilizing a Windows 11 VirtualBox environment, this project illustrates how PFsense can enforce customized network policies, manage access control, and monitor system health in a practical, real-world-inspired setup.

---

## 🛡️ Policy Implementation

The following policies were enforced using PFsense:

- **Static IP Configuration:**  
  LAN IP was set to `192.168.88.100/24` using the terminal.

- **DHCP Configuration:**  
  DHCP range set to `192.168.88.151 - 192.168.88.200` for dynamic client IP allocation.

- **Firewall Rules:**  
  Configured via GUI to manage traffic flow and port access.

- **SSH Access & Port Redirection:**  
  Enabled SSH and redirected PFsense GUI to a non-default port `11443`.

- **User Access Control:**  
  A non-admin user "Ayan" was created to demonstrate access limitations and secure login.

- **System Monitoring:**  
  ARPing package installed to test Layer 2 network connectivity and ARP diagnostics.

---

## 🛠️ Configuration

### 4.1 Installation of PFsense
- Used **Guided UFS Disk Setup** with **GPT partitioning**.
- Default WAN and LAN IPs were auto-configured (`192.168.191.132` and `192.168.1.1` respectively).

### 4.2 Network Setup (LAN/WAN)
- Configured **VirtualBox NAT adapter** for WAN and **internal network** for LAN.
- Set LAN IP to `192.168.88.100` and configured DHCP pool.
- Validated network with ping tests and browser access.

### 4.3 Web Access and Dashboard Customization
- Accessed PFsense GUI via `https://192.168.88.100:11443`.
- Customized dashboard with widgets for interface, gateway, and traffic monitoring.

### 4.4 Firewall Rules and Routing
- Created custom rules to control traffic between LAN and WAN.
- Reviewed routing and ARP tables for correct data flow.

### 4.5 SSH and Port Configuration
- Enabled SSH on default port `22`.
- Changed GUI access port to `11443` to reduce attack surface.

### 4.6 Package Installation
- Installed **ARPing** for ARP-level diagnostics to ensure LAN connectivity.

### 4.7 User Management
- Created limited-access user `Ayan` to simulate real-world access control.
- Verified SSH access and logged system activity.

---

## ✅ Conclusion

This project successfully demonstrated the setup, configuration, and policy enforcement using PFsense in a virtual environment. Through systematic network design, firewall rule management, and access control testing, it reflects the real-world applications of PFsense in network security. Potential enhancements include VPN setup, external system monitoring, and advanced traffic shaping.

---

## 📚 References

- [PFsense Official Documentation](https://docs.netgate.com/)  
- [VirtualBox Networking Guide](https://www.virtualbox.org/manual/ch06.html)  
- [PFsense Setup Video](https://www.youtube.com/watch?v=Ayr_av2EX_U&t=296s)

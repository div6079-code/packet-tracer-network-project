# VLAN Configuration using Cisco Packet Tracer 🌐

## 📌 Project Overview

This project demonstrates the configuration of Virtual Local Area Networks (VLANs) using Cisco Packet Tracer. Multiple VLANs are created to logically segment the network into different departments and control communication between devices.

---

## 🧰 Tools Used

* Cisco Packet Tracer

---

## 🏗️ Network Setup

* 2 Switches
* Multiple PCs
* Ethernet (copper straight-through) cables
* Trunk link between switches

---

## 🌐 VLAN Details

| VLAN ID | Department |
| ------- | ---------- |
| VLAN 10 | ECE        |
| VLAN 20 | EEE        |
| VLAN 30 | CSE        |

---

## ⚙️ Configuration Details

### 🔹 VLAN Creation

```bash id="o3pnw9"
enable
configure terminal

vlan 10
name ECE
exit

vlan 20
name EEE
exit

vlan 30
name CSE
exit
```

---

### 🔹 Assign Ports to VLANs

```bash id="czx1fy"
interface fast0/1
switchport mode access
switchport access vlan 10
exit

interface fast0/2
switchport mode access
switchport access vlan 20
exit

interface fast0/3
switchport mode access
switchport access vlan 30
exit
```

---

### 🔹 Trunk Configuration (Between Switches)

```bash id="1dj5l7"
interface fast0/7
switchport mode trunk
exit
```

👉 Allows multiple VLAN traffic between switches

---

## 💻 PC Configuration

Each VLAN uses a different IP range:

| VLAN    | Example IP   |
| ------- | ------------ |
| VLAN 10 | 192.168.10.x |
| VLAN 20 | 192.168.20.x |
| VLAN 30 | 192.168.30.x |

---

## 🧪 Testing

* Devices in same VLAN → ✅ Can communicate
* Devices in different VLAN → ❌ Cannot communicate (without routing)

---

## 🎯 Learning Outcomes

* VLAN creation and management
* Network segmentation
* Trunking between switches
* Improved network security and performance

---

## 📂 Files Included

* `vlan.pkt` → Packet Tracer file
* Screenshots of VLAN topology

---

## 👩‍💻 Author

Divya Sree

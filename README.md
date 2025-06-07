# LAB-NETWORK-USING-CISCO-PACKET-TRACER

---

## 📖 Table of Contents

1. [Project Overview](#project-overview)
2. [Network Topology](#network-topology)
3. [Floor-by-Floor Breakdown](#floor-by-floor-breakdown)
4. [Key Components](#key-components)
5. [Data Flow](#data-flow)
6. [Images](#IMAGES)
7. [Security & Manageability](#security--manageability)
8. [Benefits](#benefits)

---

## 🚀 Project Overview

A four-story college building network:

* Floors 1–3 each have:

  * 1 Admin Office (2–4 PCs + printer)
  * 2 Labs (15–20 PCs + printer each)
* Floor 4 also has a **Server Room** housing file, authentication, backup, and storage servers.
* All floors interconnect via high-speed trunks to a core switch/router.

**Goal:** Provide fast, secure, and segmented connectivity for students, faculty, and servers.

---

## 🌐 Network Topology

```text
                              ┌─────────────────┐  
                              │    Internet     │  
                              └─────────────────┘  
                                       ↓         
                               ┌───────────────┐  
                               │ Core Router   │  
                               └───────────────┘  
                                       ↕         
                               ┌───────────────┐  
                               │ Core Switch   │  
                               └───────────────┘  
             ┌──────┬──────────┴──────────┬──────┐
             │      │                     │      │
         Floor 1  Floor 2              Floor 3  Floor 4
         Switch   Switch               Switch   Switch
          ↓↓        ↓↓                   ↓↓       ↓↓↓
    Adm / Lab1/2  Adm/Lab1/2           Adm/Lab1/2 + Server Room
```

---

## 🏢 Floor-by-Floor Breakdown

### Floors 1–3

* **Admin Office Switch**

  * 2–4 staff PCs
  * Shared printer

* **Lab Switch A & B**

  * 15–20 student PCs each
  * Local lab printer
  * Internet access

### Floor 4

* **Admin Office Switch** (as above)
* **Lab Switches A & B**
* **Server-Room Switch**

  * File Server
  * Authentication Server
  * Backup Server
  * Network Storage Appliance

---

## 🔧 Key Components

| Component                 | Role                                                              |
| ------------------------- | ----------------------------------------------------------------- |
| **Core Router**           | Gateway to campus network & Internet                              |
| **Core & Floor Switches** | High-speed distribution between floors and labs                   |
| **Admin/Lab Switches**    | Create isolated, efficient “mini-networks”                        |
| **Fiber/Copper Trunks**   | 1 Gbps+ links between core and each floor switch                  |
| **Server-Room Switch**    | Dedicated high-speed hub for all servers                          |
| **Servers & Storage**     | Central file storage, authentication, backups, large-file hosting |

---

## 🔄 Data Flow

1. **Local Print Job** (Lab → Printer)
   Stays on the same lab switch.

2. **File Server Access**
   Lab Switch → Floor Switch → Core Switch → Floor 4 Switch → Server Room → Server.

3. **Internet Browsing**
   Lab Switch → Floor Switch → Core Switch → Core Router → Internet.
---

## IMAGES:
**Overall Network**
![Screenshot 2025-06-07 235910](https://github.com/user-attachments/assets/bd6708ec-31e7-4d84-8191-481e2dd611f9)

**FLOOR 1**
![Uploading Screenshot 2025-06-08 000501.png…]()

**FLOOR 2 and 3**
![Screenshot 2025-06-08 000512](https://github.com/user-attachments/assets/a2bdb96c-7458-4079-b2df-209cdcfdb883)

**FLOOR 4**
![Screenshot 2025-06-08 000529](https://github.com/user-attachments/assets/6a08fadf-9e3a-469e-9023-8747761d54d6)

**FlOOR NETWORKING**
![Screenshot 2025-06-08 000539](https://github.com/user-attachments/assets/e8314592-0b40-44cc-b37c-9ff444fdf4b1)

---

## 🔒 Security & Manageability

* **VLANs** separate student, admin, and server traffic.
* **Firewall** rules on the core router block unauthorized access.
* **Network Monitoring** software alerts on abnormal traffic.
* **Redundancy**: Dual uplinks ensure no single point of failure.

---

## 🎯 Benefits

* **Scalable**: Easily add new labs or offices.
* **Fault Isolation**: One lab’s issue won’t affect others.
* **High Performance**: 1 Gbps+ trunks prevent bottlenecks.
* **Secure**: Segmentation and centralized control protect data.

---

## 🛠️ Getting Started

1. **Clone the repo**

   ```bash
   git clone https://github.com/your-username/college-network-project.git
   cd college-network-project
   ```

2. **View Documentation & Diagrams**

   * `/docs/network-diagram.png`

3. **Simulate in Packet Tracer**

   * Open `packet_tracer/network_topology.pkt`

4. **Deploy**

   * Configure core router & switches per `/docs/configs/README.md`

---



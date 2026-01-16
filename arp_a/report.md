#

This file contains the output of the `arp -a` command, which displays the **Address Resolution Protocol (ARP) table** of a host machine.

The ARP table maps:

* **Internet Address (IP address)**
* **Physical Address (MAC address)**
* **Entry Type (dynamic/static)**

### Basic ARP Workflow

1. A device wants to communicate with an IP (e.g., `192.168.68.1`)
2. It checks its ARP cache
3. If not found, it broadcasts an **ARP request**
4. The target device replies with its MAC address
5. The result is stored in the ARP table

---

## Structure of the Given ARP Table

### Interface

* **Interface IP:** `192.168.68.106`
* Indicates the local system whose ARP cache is shown

### Entry Types

* **Dynamic:** Learned automatically via ARP responses
* **Static:** Manually configured or reserved (e.g., broadcast, multicast)

### Address Categories

* **Private IPv4 addresses:** `192.168.68.x`
* **Multicast addresses:** `224.x.x.x`, `239.x.x.x`
* **Broadcast addresses:** `255.255.255.255`

---

## Cybersecurity Significance

The ARP table reveals:

* Active hosts on the network
* MAC address vendors 
* Network size and topology


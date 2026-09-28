2026-09-23
Tags: #networking #ps

# 07 IP Classes overview


| **Class**   | **First Octet Range** | **Default Subnet Mask** | **Default CIDR** | **Network / Host Split** | **Purpose**                                          |
| ----------- | --------------------- | ----------------------- | ---------------- | ------------------------ | ---------------------------------------------------- |
| **Class A** | `1` – `126`           | `255.0.0.0`             | `/8`             | **N**.H.H.H              | Massive networks (huge corporations, ISPs)           |
| **Class B** | `128` – `191`         | `255.255.0.0`           | `/16`            | **N.N**.H.H              | Medium-to-large networks (universities, enterprises) |
| **Class C** | `192` – `223`         | `255.255.255.0`         | `/24`            | **N.N.N**.H              | Small local networks (home routers, small offices)   |
| **Class D** | `224` – `239`         | N/A                     | N/A              | Multicast                | Reserved for Multicast streaming (audio/video feeds) |
| **Class E** | `240` – `254`         | N/A                     | N/A              | Experimental             | Reserved for research and future R&D use             |

**Note on 127:** The IP range starting with `127` (`127.0.0.0` to `127.255.255.255`) is excluded from Class A because it is reserved for **loopback testing** (e.g., `127.0.0.1` refers to `localhost`).

### Breakdown of Primary Classes (A, B, and C)

The key difference between the classes is **how many octets belong to the Network (N)** vs. **how many belong to Hosts (H)**:

#### 1. Class A (Large Networks)

- **First Octet Bits:** Always starts with binary `0`.
    
- **Network vs. Host:** 1 octet for Network, 3 octets for Hosts (**N.H.H.H**).
    
- **Capacity:** 126 networks, each holding up to **16,777,214 hosts** ($2^{24} - 2$).
    

#### 2. Class B (Medium Networks)

- **First Octet Bits:** Always starts with binary `10`.
    
- **Network vs. Host:** 2 octets for Network, 2 octets for Hosts (**N.N.H.H**).
    
- **Capacity:** 16,384 networks, each holding up to **65,534 hosts** ($2^{16} - 2$).
    

#### 3. Class C (Small Networks)

- **First Octet Bits:** Always starts with binary `110`.
    
- **Network vs. Host:** 3 octets for Network, 1 octet for Hosts (**N.N.N.H**).
    
- **Capacity:** 2,097,152 networks, each holding up to **254 hosts** ($2^8 - 2$).
    

### Special Case: Private IP Address Ranges

Inside Classes A, B, and C, specific blocks are set aside for **Private Networks** (your home WiFi, office LAN, or cloud VPC). These cannot be routed directly on the public internet:

- **Class A Private:** `10.0.0.0` – `10.255.255.255` (`10.0.0.0/8`)
    
- **Class B Private:** `172.16.0.0` – `172.31.255.255` (`172.16.0.0/12`)
    
- **Class C Private:** `192.168.0.0` – `192.168.255.255` (`192.168.0.0/16`




### Why Classful Networking is Obsolete (Classless / CIDR)

Classful networking wasted millions of IP addresses. For example, if a company needed 300 IP addresses, a Class C (254 hosts) was too small, so they were given a Class B (65,534 hosts)—wasting over 65,000 IPs!

Today, we use **Classless Inter-Domain Routing (CIDR)**, allowing subnets to be carved into any custom size using slash notation (like the `/28` you saw earlier).


### Usable host IP addresses
You always subtract 2 when calculating usable host addresses because **the very first address and the very last address in any subnet are reserved by default for special networking functions.**

### The Two Reserved Addresses

When you create a subnet, the network requires a way to identify **the group itself** and a way to **talk to everyone in the group at once**.

```
    Subnet Range (e.g., /28 = 16 total IPs)
    ┌──────────────────────────────────────────────┐
1.  │ 10.43.33.32  ───►  Network Address  (Reserved)│
    ├──────────────────────────────────────────────┤
2.  │ 10.43.33.33  ┐                               │
    │ ...          ├─►   Usable Host IPs (14 total)│
    │ 10.43.33.46  ┘                               │
    ├──────────────────────────────────────────────┤
3.  │ 10.43.33.47  ───►  Broadcast Address(Reserved)│
    └──────────────────────────────────────────────┘
```

#### 1. The First IP = Network Address (Network ID)

- **What it is:** All host bits set to **all 0s**.
    
- **Why it's reserved:** It serves as the official "name" or identifier of the subnet. Routers use this address in their routing tables to direct traffic toward the entire network, so no single device (like a PC or phone) can take it.
    
- _Example (`10.43.33.32/28`):_ `10.43.33.32`
    

#### 2. The Last IP = Broadcast Address

- **What it is:** All host bits set to **all 1s**.
    
- **Why it's reserved:** It is used to send a message to **every single device** on that specific subnet simultaneously (a "broadcast"). If a PC sends data to this address, the switch delivers it to all connected hosts.
    
- _Example (`10.43.33.32/28`):_ `10.43.33.47`
    

### The Formula

$$\text{Usable Hosts} = 2^{\text{host bits}} - 2$$

Where:

- $2^{\text{host bits}}$ = Total IP addresses in the block.
    
- $- 2$ = Subtracting **1 Network Address** and **1 Broadcast Address**.
    

### Exception to the Rule

There is one notable exception in modern networking: **`/31` subnets** (defined in RFC 3021).

`/31` subnets only have 2 total IP addresses ($2^1 = 2$). They are used strictly for **point-to-point links** directly connecting two routers together. Because there are only two devices and no other hosts exist on the link, broadcast functionality is disabled, allowing both IPs to be used for the routers ($2 - 0 = 2$ usable hosts).
2026-08-13
Tags: [[cmm]] [[ps]] [[noc]]

# ECM and EMM

On your **Cloud Mobility Manager (CMM)**, these terms refer to the specific states used to manage how a mobile device (User Equipment or UE) interacts with the network for mobility and active data sessions.

**What is ECM? (EPS Connection Management)**

**ECM** describes the connectivity state between the device and the core network (EPC). It focuses on whether a **signaling connection** exists to allow communication between the UE and the MME.

- **ECM-IDLE:** In this state, there is **no active signaling connection** between the UE and the network. To save power and radio resources, the device tears down its radio and S1-U bearers, meaning it is not currently sending or receiving data. However, the network still knows the device's location at a "Tracking Area" level and can "page" the device if a call or message arrives.
- **ECM-CONNECTED:** This state means a **signaling connection is established**. All bearers (Radio, S1-U, and S5) are active, allowing the device to exchange data with the network.

**What is EMM? (EPS Mobility Management)**

**EMM** refers to whether the device is **officially known and authenticated** by the network. It is managed by the Control Plane Processing Service (**CPPS**) within the CMM.

- **EMM-REGISTERED:** The device has successfully completed the **Attach Procedure**. The MME/CMM has authenticated the user, retrieved their profile from the HSS, and established a "context" in its database (**DBS**).
- **EMM-DEREGISTERED:** The device is either powered off, in airplane mode, or has performed a **Detach Procedure**. The CMM no longer holds valid location information for the device, and it is unreachable by the network.

---

**Explaining User Profile Combinations in CMM**

When checking user profiles on the CMM, these states are combined to give a full picture of the subscriber's status:

- **Connected and Registered (ECM-CONNECTED / EMM-REGISTERED):**
    - This is the "active" state.
    - The user is **authenticated** (Registered) and **actively using the network** (Connected).
    - Radio resources are assigned, and data transfer is occurring or can occur immediately.
- **Idle and Registered (ECM-IDLE / EMM-REGISTERED):**
    - This is the most common state for a phone in your pocket.
    - The user is **authenticated** and known to the CMM (Registered), but they are **not currently sending data** (Idle).
    - The device has released its radio connection to save battery, but it maintains its IP address.
    - If someone calls the user, the MME will **page** the device to move it back to "Connected and Registered".
- **Idle and Deregistered (ECM-IDLE / EMM-DEREGISTERED):**
    - This indicates the device is **not on the network**.
    - There is no active signaling (Idle) and the device is not attached (Deregistered).
    - The network has no record of where this device is located and cannot reach it. This happens if the user manually detached or if the **Implicit Detach timer** expired because the device hasn't communicated with the CMM for a long time.
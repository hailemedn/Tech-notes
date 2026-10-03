2026-09-22
Tags: [[cmm]] [[ps]] [[noc]]

# 06 TAC, LAC

**TAC (Tracking Area Code)** and **LAC (Location Area Code)** are geographical grouping identifiers used by core mobile networks to locate and page mobile devices without needing to broadcast messages to every single cell tower in a country.

### Key Comparison

| **Feature**           | **LAC (Location Area Code)**                                              | **TAC (Tracking Area Code)**                                                           |
| --------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **Generations**       | **2G (GSM)** and **3G (UMTS)**                                            | **4G (LTE)** and **5G (NR)**                                                           |
| **Core Network Node** | Managed by **MSC / VLR** (Circuit-Switched) or **SGSN** (Packet-Switched) | Managed by **MME** (4G) or **AMF** (5G)                                                |
| **Size / Range**      | Fixed 16-bit value (`0` to `65,535`)                                      | **4G:** 16-bit (`0` to `65,535`)<br><br>  <br><br>**5G:** 24-bit (`0` to `16,777,215`) |
| **Location Update**   | Device sends **Location Update (LU)** when changing LACs                  | Device sends **Tracking Area Update (TAU)** when changing TACs                         |

### Why Are They Used?

When someone calls or sends data to a phone in standby/idle mode, the core network must **page** (find) the phone.

1. **Without LAC/TAC:** The network would have to broadcast a paging signal across every single cell tower in the entire country, swamping network capacity.
    
2. **With LAC/TAC:** Cell towers are grouped into logical clusters (Tracking/Location Areas). The network tracks which area the phone was last active in and sends the paging signal **only to the towers within that specific TAC/LAC**.
    

### How They Build Full Network IDs

Both TAC and LAC combine with country and operator codes to form globally unique identifiers:

- **LAI (Location Area Identity):**
    
    $\text{MCC} + \text{MNC} + \text{LAC}$ _(Identifies a 2G/3G area globally)_
    
- **TAI (Tracking Area Identity):**
    
    $\text{MCC} + \text{MNC} + \text{TAC}$ _(Identifies a 4G/5G area globally)_
    

_(Where **MCC** = Mobile Country Code and **MNC** = Mobile Network Code)._
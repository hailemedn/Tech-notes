2026-07-23
tags: #cmg

## AGWGTPPMIPEERDOWN ALARM, FOR SY AND TY INTERFACES.

Alarm Text 
Distinguished Name 

AGWGTPPMIPPeerDown 
PLMN-PLMN/SAM-MDC1NSP/CMG-10.44.3.72@MDC2-NK-CMG-UP01/epc-1/eps_peer-39-10.36.136.66-2152-refPtName-s1_MG+Group13-peerTy-7 

 

 

### Get serviceId from MGgroup and refPtName 

```sh
*B:MDC2-NK-CMG-UP01# show service service-using    //refPtName-s1  -> relates with ran, we use coreup  

ServiceId    Type      Adm  Opr  CustomerId Service Name 

------------------------------------------------------------------------------- 

510          VPRN      Up   Up   1          COREUP_MG-Grp10 

511          VPRN      Up   Up   1          COREUP_MG-Grp11 

512          VPRN      Up   Up   1          COREUP_MG-Grp12 

513          VPRN      Up   Up   1          COREUP_MG-Grp13 

```


 

### Get source IP 

```sh
B:MDC2-NK-CMG-UP01# show router 513 interface 

Interface-Name                   Adm       Opr(v4/v6)  Mode    Port/SapId 
    IP-Address                                                  PfxState 
------------------------------------------------------------------------------- 
 
    10.44.100.111/27                                            n/a 
LBK-COREUP-S1u-13                Up        Up/Down     VPRN    loopback 
    10.44.101.205/32                                            n/a 
LBK-COREUP-S5uGnUS2bUs2aU-13     Up        Up/Down     VPRN    loopback 
    10.44.100.141/32                                            n/a 
LBK-COREUP-s8uGpu-13             Up        Up/Down     VPRN    loopback 
    102.208.99.109/32                                           n/a 

```

 

Ping 

```sh
B:MDC2-NK-CMG-UP01# ping router 513 10.36.136.66 source 10.44.101.205   // get destination ip from alarm 
  

---- 10.36.136.66 PING Statistics ---- 
5 packets transmitted, 5 packets received, 0.00% packet loss 
round-trip min = 4.83ms, avg = 4.90ms, max = 4.98ms, stddev = 0.058ms 
```

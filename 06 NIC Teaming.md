
<!-- Your monitor number = #$34T# -->

# 💡 NIC Teaming

### 1. Add Network Adapter
- Name: IAM-m
- Network Adapter:
  - 1: NAT               : 208.8.8.8
  - 2: Bridged / VMNet2  : 10.m.1.8 / 192.168.102.8
  
  - 3: VMNet3            : 192.168.103.8
  - 4: VMNet3            :
  - 5: VMNet3            :


&nbsp;
---
&nbsp;


### 2. Network Connections

~~~
!@Run
Win + R: ncpa.cpl
~~~

Rename the ff:
- Ethernet2 - __T3-1__
- Ethernet3 - __T3-2__
- Ethernet4 - __T3-3__


&nbsp;
---
&nbsp;


### 3. Enable NIC Teaming
`Server Manager` > `Local Server` > `Enable NIC Teaming`


Adapters and Interfaces
> __T3-1__ , __T3-2__ , __T3-3__ : Add to New Team

Additional Properties:
- Teaming Mode:        __Switch Independent__
- Load Balancing Mode: __Address Hash__ / __LACP__
- Standby:             __None__


&nbsp;
---
&nbsp;


### 4. Modify NIC Team Adapter (NIC-T3)
- NIC-T3:
  - IP:      192.168.103.8
  - Mask:    255.255.255.0
  - Gateway: None
  - DNS:     None
 




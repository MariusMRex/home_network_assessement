# Network Audit Scope

At the time of this audit this LAN has two active subnets.  

| Subnet Designation | IP Range | IP segment | Purpose | Notes |
| -----------------: | :------: | :--------: | :-----: | :---: |
| Front end network | 172.18.93.0/24 | NA | Internet facing network | Divided into four logical sub blocks |
| | | 172.18.93.0/26 | infrastructure | Routes to Internet through VPN. Has statically assigned addresses |
| | | 172.18.93.64/26 | user1 | Routes to Internet through VPN. DHCP assigned addresses |
| | | 172.18.93.128/26 | user2 | Routes to Internet through VPN. DHCP assigned addresses |
| | | 172.18.93.192/26 | unmasked | Routes directly to Internet via PAT/NAT Has statically assigned addresses |
| Back end network | 172.18.94.0/24 | backend | Local only network | Statically assigned addresses.  No Internet access |

All devices on both subnets, wired and unwired, are in scope

## Front End network

| Device name | Segment | Note |
| :---------- | :-----: | ---: |
| Janus | infrastructure | Dual homed network gateway |
| Styx | infrastructure | 16 port unifi switch - central switch |
| Thermopyle | infrastructure | Living room wifi access point | 
| Cocytus | infrastructure | 5 port unifi switch in exercise room| 
| freenas | infrastructure | Dual homed NAS server | 
| Phlegethon | infrastructure | 8 port unifi switch in main office | 
| Hippocrene | infrastructure | Wifi access point in second office | 
| Castalian | infrastructure | Wifi access point in exercise room | 
| Lethe | infrastructure | 5 port unifi switch in media console |
| Archeron | infrastructure | 5 port unifi switch in second office |




## Backend Network

| Device name | Segment | Note |
| :---------- | :-----: | ---: |
| Janus | backend | Dual homed network gateway |
| freenas-backend | backend | Dual homed NAS server |
| freenas-ipmi | backend | IPMI for NAS server |
| sony-player | backend | Blueray player |



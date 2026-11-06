# Network Audit Scope

All entities in the following network are considered to be in scope:

| Subnet Designation | IP Range | IP segment | Purpose | Notes |
| -----------------: | :------: | :--------: | :-----: | ----: |
| VLAN A: Front end network | 172.18.x.x/24 | NA | Internet facing network | Divided into four logical sub blocks |
|  |  | 172.18.x.0/26 | infrastructure | Routes to Internet through VPN. Has statically assigned addresses |
|  |  | 172.18.x.64/26 | user1 | Routes to Internet through VPN. DHCP assigned addresses |
|  |  | 172.18.x.128/26 | user2 | Routes to Internet through VPN. DHCP assigned addresses |
|  |  | 172.18.x.192/26 | unmasked | Routes directly to Internet via PAT/NAT.  Has statically assigned addresses |
| VLAN B: Back end network | 172.18.y.x/24 | backend | Local only network | Statically assigned addresses.  No Internet access |
| Router External IP | public | NA | Gateway to network | Management login disabled from all external IPs |

See the [Inventory](inventory.md) file for a detailed list of hosts contained in each network

# Goal

In the language if NIST CSF, the initial goal of this survey is improved governance and understanding.  

1. Identify and understand all existing assets, including hardware, software, services, and sensitive data
1. Identify and assess those assets for potential vulnerabilities
1. Identify a risk management strategy.  What risks are acceptable?  What risks are to be mitigated? Is there residual risk left over?
1. Identify and prioritize what changes should be made to protect the most valuable or vulnerable resources
1. Protect the prioritized assets making modifications where necessary and feasible.  

Future stages may involve setting up monitoring to better detect potential issues, as well as better documented response and recovery procedures.

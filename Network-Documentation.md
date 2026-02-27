# Network Documentation – Final Project

## 1. Objective
Design and implement a secure enterprise network with VLAN segmentation, routing, NAT, and ACL-based traffic control.

---

## 2. IP Addressing & Subnetting

### VLAN Subnets
| VLAN | Subnet | Gateway |
|----|----|----|
| 10 | 10.10.10.0/28 | 10.10.10.1 |
| 20 | 20.20.20.0/28 | 20.20.20.1 |
| 30 | 30.30.30.0/28 | 30.30.30.1 |

### Server Network
| Server | Private IP | Public IP |
|----|----|----|
| WEB1 | 192.168.30.10 | 203.0.113.10 |
| WEB2 | 192.168.30.11 | 203.0.113.11 |
| WEB3 | 192.168.30.12 | 203.0.113.12 |

---

## 3. VLAN Configuration
- VLANs created on access switch
- Ports assigned per department
- Trunk link to Router4
- Inter-VLAN routing via router-on-a-stick

---

## 4. Routing
- Static routing used
- Default route configured on Router4 toward ISP
- All internal networks reachable

---

## 5. NAT Configuration

### PAT (Router4)
- VLAN users translated to Router4 public interface
- Internet access verified

### Static NAT (Router3)
- WEB servers mapped to public IPs
- Services accessible externally

---

## 6. ACL Security

### Implemented Policies
- VLAN 30 blocked from VLAN 10 & 20
- Only HTTP allowed to WEB1 & WEB2
- FTP allowed only to WEB2
- WEB3 restricted to admin PC only
- LAN7 internet access limited to DNS & HTTP

---

## 7. Testing & Verification

### Successful
- Gateway pings
- Inter-VLAN routing (allowed paths)
- Internet access
- NAT translations
- Web & FTP services

### Blocked
- Unauthorized VLAN access
- Restricted server access
- Forbidden internet traffic

---

## 8. Conclusion
This project demonstrates practical enterprise networking skills including segmentation, routing, NAT, and security enforcement using ACLs.

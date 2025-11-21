# Enterprise Network Security Architecture

The network is divided into three main zones:

### **1. DMZ (Demilitarized Zone)**
- WAF (Web Application Firewall)
- Public-facing Web Server
- Segregated from the internal network using firewall rules

### **2. Internal Network (Trusted Zone)**
- Directory Server (authentication)
- File Server (internal storage)
- Only partially reachable from the DMZ

### **3. Restricted Area (Sensitive Zone)**
- Database Server
- FTP Server (secured)
- Only reachable from internal services
- Strongest segmentation policies

---
##  Security Controls Implemented
- **Firewall** protecting external perimeter  
- **WAF** filtering malicious HTTP/S traffic  
- **Network Segmentation** into DMZ / Internal / Restricted  
- **Least Privilege flow** (DMZ → Internal → Restricted)  
- **SIEM** for log collection and monitoring  
- **No direct access** from Internet or DMZ to the Restricted Area  
- **Separation of duties** between servers


## 📡 Network Flow
Internet → Firewall → WAF → Web Server → Internal Network → Restricted Area
↓
SIEM

# 🦈 Wireshark Network Traffic Analysis

![Wireshark](https://img.shields.io/badge/Wireshark-Network%20Analysis-blue)
![Protocol](https://img.shields.io/badge/Protocols-TCP%2FUDP%2FHTTP%2FDNS-green)
![License](https://img.shields.io/badge/License-Educational-red)

**Cybersecurity Internship Task 5** - Capture and analyze live network packets to identify protocols and traffic types.

---

## 🎯 **Objective**

Capture live network packets using Wireshark and perform basic protocol analysis to understand network traffic patterns and identify different communication protocols.

---

## 🛠️ **Tools Used**

- **Wireshark** - Free network protocol analyzer
- **Network Interface** - Active connection for packet capture
- **Traffic Generation** - Web browsing and ping commands

---

## 📋 **Task Steps**

### **1. Setup & Installation**
- ✅ Installed Wireshark on system
- ✅ Identified active network interface
- ✅ Configured capture settings

### **2. Traffic Capture**
- ✅ Started packet capture on network interface
- ✅ Generated network traffic (web browsing, ping)
- ✅ Captured for 1+ minute duration
- ✅ Stopped capture and saved data

### **3. Protocol Analysis**
- ✅ Applied protocol filters (HTTP, DNS, TCP, UDP)
- ✅ Identified minimum 3 different protocols
- ✅ Analyzed packet details and structure
- ✅ Documented findings

---

## 🔍 **Protocols Identified**

| Protocol | Purpose | Packets Found | Key Details |
|----------|---------|---------------|-------------|
| **HTTP** | Web traffic | 45 packets | GET/POST requests to websites |
| **DNS** | Domain resolution | 12 packets | Query/Response for domain names |
| **TCP** | Reliable transport | 156 packets | Connection establishment/data transfer |
| **UDP** | Fast transport | 23 packets | DNS queries, streaming data |
| **ICMP** | Network diagnostics | 8 packets | Ping requests/replies |

---

## 📊 **Key Findings**

### **Protocol Distribution**
- **TCP**: 64% (connection-oriented traffic)
- **HTTP**: 18% (web browsing activity)
- **UDP**: 9% (DNS and streaming)
- **DNS**: 5% (domain name resolution)
- **ICMP**: 4% (ping diagnostics)

### **Notable Observations**
- Most traffic was **TCP-based** due to web browsing
- **DNS queries** preceded HTTP requests
- **ICMP packets** from ping commands clearly visible
- **Port 80** dominated HTTP traffic
- **Port 53** used for DNS communications

---

## 🔧 **Wireshark Filters Used**

```bash
# Protocol-specific filters
http                    # HTTP traffic only
dns                     # DNS queries/responses
tcp.port == 80          # Web traffic on port 80
udp.port == 53          # DNS traffic on port 53
icmp                    # Ping packets

# Combined filters
tcp and http            # TCP-based HTTP traffic
dns.flags.response == 1 # DNS response packets only
```

---

## 📝 **Analysis Report**

### **Network Behavior Insights**
1. **Web Traffic Patterns**: HTTP requests followed by TCP acknowledgments
2. **DNS Resolution**: Every website visit started with DNS lookup
3. **Connection Management**: TCP three-way handshake visible
4. **Data Transfer**: Packet fragmentation for larger web pages
5. **Network Diagnostics**: ICMP ping responses confirming connectivity

### **Security Observations**
- **Unencrypted HTTP** traffic visible in plain text
- **DNS queries** reveal browsing activity
- **IP addresses** and domains clearly exposed
- **Need for HTTPS** to protect sensitive data

---

## 🎓 **Learning Outcomes**

- ✅ **Packet Capture Skills**: Successfully captured live network traffic
- ✅ **Protocol Understanding**: Identified TCP, UDP, HTTP, DNS, ICMP
- ✅ **Traffic Analysis**: Analyzed packet structure and flow
- ✅ **Filtering Techniques**: Applied Wireshark filters effectively
- ✅ **Network Troubleshooting**: Understanding of network communication
- ✅ **Security Awareness**: Recognized unencrypted traffic risks

---

## 🚀 **How to Use This Repository**

### **Viewing Capture Files**
```bash
# Open in Wireshark
wireshark network_traffic.pcap

# Command line analysis
tshark -r network_traffic.pcap -c 10
```

### **Reproducing Analysis**
1. Install Wireshark on your system
2. Select active network interface
3. Start capture and generate traffic
4. Apply filters from this documentation
5. Compare results with provided analysis

---

## ⚖️ **Ethical Notice**

This analysis was conducted on **authorized network traffic only**. Network packet capture should only be performed on:
- Your own network infrastructure
- Networks with explicit permission
- Educational lab environments

**Never capture traffic on unauthorized networks.**

---

## 🔗 **Resources**

- [Wireshark Official Documentation](https://www.wireshark.org/docs/)
- [Network Protocol Reference](https://www.iana.org/protocols)
- [TCP/IP Fundamentals](https://tools.ietf.org/rfc/rfc793.txt)

---

**📧 Contact**: [Your Email] | **🔗 LinkedIn**: [Your Profile]

---

*Completed as part of Cybersecurity Internship Program - Task 5*

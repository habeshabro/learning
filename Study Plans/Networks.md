# **Layer 1 — Physical Layer (Simplest Concepts)**

Focus: _How bits physically travel_

- Signals & Encoding
    
    - Digital vs analog signals
        
    - Line coding (NRZ, Manchester, 4B/5B, 8B/10B)
        
    - Modulation techniques (ASK, PSK, FSK, QAM)
        
- Transmission Impairments
    
    - Attenuation, noise, delay distortion
        
- Bandwidth & Data Rate
    
    - Nyquist theorem
        
    - Shannon capacity
        
- Physical Media
    
    - Copper (UTP, STP)
        
    - Fiber (SM, MM, WDM)
        
    - Wireless spectrum & channels
        
- Networking Hardware Fundamentals
    
    - Repeaters
        
    - Hubs
        
    - Optical amplifiers
        
- Advanced Physical Tech
    
    - OFDM
        
    - MIMO
        
    - 5G NR physical layer concepts
        

---

# **📌 Layer 2 — Data Link Layer**

Focus: _Frames, reliability, MAC control_

- Framing methods (HDLC, PPP)
    
- Error Detection & Correction
    
    - CRC, Hamming codes
        
- Flow Control
    
    - Stop-and-wait
        
    - Sliding window
        
- Medium Access Control (MAC)
    
    - CSMA/CD, CSMA/CA
        
    - Channel allocation
        
- VLANs & Trunking
    
- STP / RSTP / MSTP
    
- Ethernet advanced features
    
    - MAC learning & aging
        
    - Jumbo frames
        
    - Ethernet autonegotiation
        
- Wireless MAC (802.11)
    
    - RTS/CTS
        
    - Frame structure
        
    - Management/control frames
        
- Advanced protocols
    
    - MPLS data-plane behavior
        
    - Deterministic networking (TSN)
        

---

# **📌 Layer 3 — Network Layer**

Focus: _Routing, addressing, forwarding — major advanced topics_

### **IP Addressing**

- CIDR, subnetting, supernetting
    
- IPv4 → IPv6 transition technologies (NAT64, Dual-stack)
    

### **Routing Fundamentals**

- Static vs dynamic routing
    
- Distance vector vs link state
    
- Path selection metrics
    

### **Advanced Routing Protocols**

- OSPF (areas, LSAs, DR/BDR elections, SPF algorithm)
    
- IS-IS (adjacency, TLVs, multi-level hierarchy)
    
- BGP (IBGP/EBGP, route reflectors, communities, AS_PATH, policies)
    

### **Traffic Engineering**

- MPLS (labels, LSPs, LDP, RSVP-TE)
    
- Segment Routing (SR-MPLS, SRv6)
    
- Fast reroute (FRR)
    

### **Tunneling & Encapsulation**

- GRE, IPIP
    
- VXLAN, NVGRE, GENEVE
    
- VPNs (L2VPN, L3VPN)
    

### **Advanced IPv6 Concepts**

- SLAAC vs DHCPv6
    
- Routing specifics (link-local, ULA, RA messages)
    

---

# **📌 Layer 4 — Transport Layer**

Focus: _End-to-end transport behavior and performance_

- TCP mechanisms
    
    - Three-way handshake
        
    - Congestion control (Tahoe, Reno, Cubic, BBR)
        
    - Flow control
        
    - Fast retransmit & fast recovery
        
- UDP advanced behavior
    
- SCTP (multi-homing, multi-streaming)
    
- QUIC protocol
    
- NAT traversal techniques
    
- Performance topics
    
    - RTT, throughput models
        
    - TCP offload engine (TOE)
        

---

# **📌 Layer 5 — Session Layer**

Focus: _Session establishment & management_

(Smaller layer, but study these concepts:)

- Session establishment mechanisms
    
- Checkpointing & recovery
    
- RPC mechanisms
    
- Authentication & session tokens (partly overlaps L6/L7)
    

---

# **📌 Layer 6 — Presentation Layer**

Focus: _Data representation + encryption_

- Data formats
    
    - ASN.1, XDR
        
    - Serialization (JSON, XML, Protobuf, Avro)
        
- Character encoding (Unicode, UTF variations)
    
- TLS/SSL
    
    - Handshake steps
        
    - Certificates
        
    - Cipher suites
        
- Encryption algorithms (AES, RSA, ECC)
    
- Compression formats (gzip, Brotli)
    

---

# **📌 Layer 7 — Application Layer (Most Complex Layer)**

Focus: _High-level protocols & full networked systems_

### **Core Application Protocols**

- HTTP/1.1, HTTP/2, HTTP/3
    
- DNS (records, resolution process, DNSSEC)
    
- DHCP (lease process, options)
    
- SNMP (v1/v2/v3, MIB, OIDs)
    
- SMTP/IMAP/POP3
    

### **Advanced Topics**

- CDN architecture
    
- WebSockets
    
- API architectures (REST, gRPC)
    
- Microservices networking
    
- Load balancing
    
    - L4 vs L7 load balancers
        
    - Reverse proxies (Nginx, Envoy)
        
- Service mesh (Istio, Linkerd)
    
- Zero Trust networking
    
- Cloud network architecture
    
    - VPC, Subnets, Internet Gateways
        
    - Peering, Transit Gateway
        
    - Software-defined networking (SDN)
        

---

# **🚀 Optional Capstone Areas (After OSI Layers)**

These bring everything together:

- Network Security (Advanced)
    
    - IDS/IPS
        
    - Firewalls (L3/L7)
        
    - Zero Trust
        
- Distributed Systems Networking
    
    - Consensus algorithms
        
    - Overlay networks
        
- Data Center Networks (CLOS, Spine-Leaf)
    
- High-Performance Networks
    
    - RDMA
        
    - InfiniBand
        
    - DPDK
## ISP 
- **Core: OSPF + LDP**
- **MP-BGP:**
  - No RR => Full-mesh
  - ASN = 64512
- **CE-PE routing: EBGP**

## DC
**2 DCs | 2 Tenants | All multihomed**  
- **UNDERLAY: EBGP**, ASN-per-device
  -   ASNs: 65001-65008
- **OVERLAY: IBGP**
  - No RRs => Full Mesh
  - ASN = 65500
- **DCI = MPLS L3VPN**
- **VXLAN:**
  - **2 EVIs** (one per-tenant) - **VLAN-Based**
  - **EBR** - GWs on LEAVEs
    - **Virtual GWs everywhere** 
  - **L3VPN for intersubnet routing:**
    - **Symmetric IRB** routing model:
    - **Type5s** for inter-subnet routing within an EVI

- **RED tenant:**
    - L2 VNIs 5010-5011 | RT=65000:100
    - L3 VNI 5100 | RT=65000:1000
- **GREEN tenant:**
    - L2 VNI 5020-5021 | RT=65000:200
    - L3 VNI 5200 | RT=65000:2000

<img width="1244" height="1021" alt="image" src="https://github.com/user-attachments/assets/4553fbd4-5d11-47b0-894b-6e920564839a" />

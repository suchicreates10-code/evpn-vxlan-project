# VXLAN & EVPN Learning Repository

This repository documents my hands-on learning of VXLAN and EVPN.  
All explanations are written in my own words as I study and build labs step-by-step.

---

## 🔰 What is VXLAN?

VXLAN (Virtual Extensible LAN) allows us to extend Layer-2 networks across the data center using an L3 underlay.  
It solves VLAN scaling limits and removes the need for large L2 domains that cause loops.  
By encapsulating Ethernet frames inside UDP/IP, VXLAN builds flexible, scalable virtual networks across the fabric.

---

## 🧠 Key Concepts I Learned Today

### **1. Underlay vs Overlay**
**Underlay:** A pure Layer-3 IP network that provides connectivity between VTEPs using routing protocols.  
**Overlay:** A virtual Layer-2 network built on top of the underlay, using VXLAN tunnels to carry L2 traffic across the fabric.

---

### **2. VNI (VXLAN Network Identifier)**
A VNI is a 24-bit ID that identifies each VXLAN segment.  
It works like a VLAN ID but provides up to 16 million unique segments, allowing VXLAN to scale for large, multi-tenant data centers.

---

### **3. VTEP & Loopback**
A VTEP (VXLAN Tunnel Endpoint) is the device that encapsulates and decapsulates VXLAN traffic.  
It uses a loopback IP as its tunnel source because the loopback is always up and provides a stable, reliable endpoint for VXLAN tunnels.

---

### **4. EVPN Control Plane**
EVPN is a control plane for VXLAN that uses BGP to distribute MAC and IP information between VTEPs.  
This removes flood-and-learn behavior and allows the fabric to make faster, smarter forwarding decisions.

---

## 📌 Status
This README will grow daily as I learn more, add labs, packet captures, configs, and troubleshooting notes.


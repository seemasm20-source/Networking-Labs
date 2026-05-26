🖥️ Network Topology



<img width="1920" height="1080" alt="Screenshot (204)" src="https://github.com/user-attachments/assets/e7285ed4-07ca-492e-b8c2-48b0f8855e6a" />




























🔧 Devices Used

| Device Model      | Quantity | Purpose                       |
| ----------------- | -------: | ----------------------------- |
| Router Cisco 2911 | 1        | Routes Traffic Between 2 LANs |
| Switch Cisco 2960 | 2        | Connects PCs Within Each LAN  |
| PC Generic PC     | 6        | End User Devices — 3 Per LAN  |
















⚙️ Step-by-Step Build Guide
Step 1 — Add Devices to Canvas

Open Cisco Packet Tracer
Drag 1 x Router 2911 → place in the centre
Drag 2 x Switch 2960 → one left, one right of router
Drag 6 x PC → 3 below each switch


Step 2 — Connect Cables
Cable type: Copper Straight-Through for all connections
FromPortToPortPC1FastEthernet0Switch 1any FastEthernetPC2FastEthernet0Switch 1any FastEthernetPC3FastEthernet0Switch 1any FastEthernetPC4FastEthernet0Switch 2any FastEthernetPC5FastEthernet0Switch 2any FastEthernetPC6FastEthernet0Switch 2any FastEthernetSwitch 1GigabitEthernetRouterGigabitEthernet0/0Switch 2GigabitEthernetRouterGigabitEthernet0/1
✅ All cable dots turn green = connected correctly
🔴 Red dot = wrong cable or wrong port — delete and redo

Step 3 — Assign IPs to All PCs
Click each PC → Desktop tab → IP Configuration → Static
PCIP AddressSubnet MaskDefault GatewayPC110.0.0.1255.255.255.010.0.0.4PC210.0.0.2255.255.255.010.0.0.4PC310.0.0.3255.255.255.010.0.0.4PC4192.168.1.1255.255.255.0192.168.1.4PC5192.168.1.2255.255.255.0192.168.1.4PC6192.168.1.3255.255.255.0192.168.1.4

Note: Default gateway is the router's IP on
that PC's side.
LAN 1 PCs (PC1–PC3) → gateway 10.0.0.4
LAN 2 PCs (PC4–PC6) → gateway 192.168.1.4

PC1 IP configuration — LAN 1 (HR):
<img width="1920" height="1080" alt="PC1 IP Config" src="https://github.com/user-attachments/assets/e5011b07-df28-4b9f-8081-0d6956a304ed" />
PC4 IP configuration — LAN 2 (Finance):
<img width="1920" height="1080" alt="PC4 IP Config" src="https://github.com/user-attachments/assets/babcb9ab-42c3-448d-b247-04cc0cd1ce78" />

Same configuration applied to PC2 and PC3 (LAN 1)
and PC5 and PC6 (LAN 2) with their respective IPs
from the table above.

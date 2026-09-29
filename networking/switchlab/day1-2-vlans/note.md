# Day 1-2: VLANs (SwitchLab)

## What I did
- Created VLAN 10 (SALES) and VLAN 20 (IT) on the switch
- Assigned g0/1 to VLAN 10, g0/2 to VLAN 20
- Set static IPs on PCs: Admin PC 192.168.10.10/24, Test PC 192.168.20.10/24

## Commands used
configure terminal
vlan 10
 name SALES
vlan 20
 name IT
interface g0/1
 switchport mode access
 switchport access vlan 10
interface g0/2
 switchport mode access
 switchport access vlan 20

## Verification
- `show vlan brief` confirmed VLAN 10 and 20 active with correct ports
- Ping from TestPC to 192.168.10.10 failed (100% loss) — confirms VLAN isolation, 
  since PCs in different VLANs can't reach each other without routing

## What this proves
VLAN segmentation is working correctly at Layer 2.
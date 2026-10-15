Ticket #1 — Resolution Summary

Issue: Sales VLAN (10) PC1 couldn’t reach IT VLAN (20) PC2
Investigation: Confirmed router gateways reachable, switch VLAN assignments and port status all correct, but router ARP table showed no entry for either PC
Root cause: PC1’s IP configuration wasn’t actually applied to the interface despite displaying correct values in the GUI (a Packet Tracer quirk — likely configured before the interface was fully initialized)
Fix: Re-selected Static mode and retyped IP/subnet/gateway fresh
Verified: Successful ping to gateway and cross-VLAN ping to PC2; router ARP table now populated
# Day 3-4: VLANs + Trunking (Packet Tracer)

Built a 2-switch topology with VLAN 10 (SALES) and VLAN 20 (IT) on both switches,
connected via an 802.1Q trunk link (Fa0/1 on both ends).

# Verified:
- `show interfaces trunk` — Fa0/1 trunking correctly, carrying VLANs 1, 10, 20
- Ping PC1 → PC3 (same VLAN 10, different switch) — succeeded, 0% loss
- Ping PC1 → PC2 (different VLANs) — failed, 100% loss, as expected

# Result:
Trunk correctly carries same-VLAN traffic across switches while
VLAN isolation between VLAN 10 and VLAN 20 still holds.
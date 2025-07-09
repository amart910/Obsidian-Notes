# 🛠️ GL.iNet Flint (GL-AX1800) Router Setup — Full Process with Troubleshooting

## 📘 Objective
To configure the GL.iNet Flint router using OpenWRT via SSH with:
- VLAN segmentation (main, IoT, guest, VPN)
- Multi-band SSIDs
- Secure firewall isolation
- DHCP configuration for each network

---

## 🧭 Network Design Overview

| VLAN  | Purpose          | Subnet            | Band       | SSID Names        |
|-------|------------------|-------------------|------------|-------------------|
| main  | Trusted devices  | 192.168.1.0/24    | 5GHz       | HomeMain-5G       |
| iot   | IoT isolation    | 192.168.20.0/24   | 2.4 + 5GHz | IoT-2.4GHz, IoT-5G |
| guest | Guest access     | 192.168.30.0/24   | 2.4GHz     | HomeGuest         |
| vpn   | VPN traffic only | 192.168.40.0/24   | Optional   | HomeVPN           |

---

## ❌ Issues Encountered and Solutions

### 🚫 Clients could not connect to IoT/Guest SSIDs
**Cause:** VLAN interfaces (`iot`, `guest`) were not defined as bridges. Wireless interfaces cannot support multiple clients unless bridged.  
**Fix:**
```bash
uci set network.iot.type='bridge'
uci set network.guest.type='bridge'
uci commit network && /etc/init.d/network restart
```

### 🚫 5GHz radio disabled or reverted to 2.4GHz
**Cause:** Missing or incorrect `htmode` and `hwmode` settings on `radio0`.  
**Fix:**
```bash
uci set wireless.radio0.hwmode='11a'
uci set wireless.radio0.htmode='HE80'
uci commit wireless && wifi reload
```

### 🚫 Guest network failed to assign IPs
**Cause:** Mislinked SSID or missing DHCP configuration for guest.  
**Fix:** Corrected SSID bindings and added:
```bash
uci set dhcp.guest.interface='guest'
uci commit dhcp && /etc/init.d/dnsmasq restart
```

### 🚫 SSH gave "REMOTE HOST IDENTIFICATION HAS CHANGED"
**Fix:**
```bash
ssh-keygen -R 192.168.1.1
```

### 🚫 SSIDs weren’t binding to interfaces
**Fix:** Ensured all SSIDs included `option network='iot'` or `guest` and were assigned to `radio0`/`radio1`.

---

## ✅ Final Validation
- VLANs isolated with correct IP ranges
- IoT and Guest SSIDs accept multiple clients
- Firewall rules enforced
- DHCP works across all VLANs
- Wireless radios stable on both bands

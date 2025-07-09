# ✅ GL.iNet Flint (GL-AX1800) — Clean OpenWRT Setup Guide

## 🧭 Network Overview

| VLAN  | Subnet          | SSIDs                | Band     |
|-------|------------------|-----------------------|----------|
| main  | 192.168.1.0/24   | HomeMain-5G           | 5GHz     |
| iot   | 192.168.20.0/24  | IoT-2.4GHz, IoT-5G    | 2.4/5GHz |
| guest | 192.168.30.0/24  | HomeGuest             | 2.4GHz   |

---

## 🔧 Interface Configuration
```bash
uci set network.iot=interface
uci set network.iot.proto='static'
uci set network.iot.ipaddr='192.168.20.1'
uci set network.iot.netmask='255.255.255.0'
uci set network.iot.type='bridge'

uci set network.guest=interface
uci set network.guest.proto='static'
uci set network.guest.ipaddr='192.168.30.1'
uci set network.guest.netmask='255.255.255.0'
uci set network.guest.type='bridge'
```

---

## 📶 Wireless SSIDs
```bash
# IoT 2.4GHz
uci add wireless wifi-iface
uci set wireless.@wifi-iface[-1].device='radio1'
uci set wireless.@wifi-iface[-1].mode='ap'
uci set wireless.@wifi-iface[-1].ssid='IoT-2.4GHz'
uci set wireless.@wifi-iface[-1].encryption='psk2'
uci set wireless.@wifi-iface[-1].key='yourpassword'
uci set wireless.@wifi-iface[-1].network='iot'

# IoT 5GHz
uci add wireless wifi-iface
uci set wireless.@wifi-iface[-1].device='radio0'
uci set wireless.@wifi-iface[-1].mode='ap'
uci set wireless.@wifi-iface[-1].ssid='IoT-5G'
uci set wireless.@wifi-iface[-1].encryption='psk2'
uci set wireless.@wifi-iface[-1].key='yourpassword'
uci set wireless.@wifi-iface[-1].network='iot'
```

---

## 📦 DHCP Configuration
```bash
uci set dhcp.iot=dhcp
uci set dhcp.iot.interface='iot'
uci set dhcp.iot.start='100'
uci set dhcp.iot.limit='100'
uci set dhcp.iot.leasetime='1h'

uci set dhcp.guest=dhcp
uci set dhcp.guest.interface='guest'
uci set dhcp.guest.start='100'
uci set dhcp.guest.limit='100'
uci set dhcp.guest.leasetime='1h'
```

---

## 🔥 Firewall Zones
```bash
uci set firewall.iot=zone
uci set firewall.iot.name='iot'
uci set firewall.iot.network='iot'
uci set firewall.iot.input='REJECT'
uci set firewall.iot.output='ACCEPT'
uci set firewall.iot.forward='REJECT'
uci set firewall.iot.masq='1'

uci add firewall forwarding
uci set firewall.@forwarding[-1].src='iot'
uci set firewall.@forwarding[-1].dest='wan'
```

---

## ✅ Final Commands
```bash
uci commit
/etc/init.d/network restart
/etc/init.d/dnsmasq restart
/etc/init.d/firewall restart
wifi reload
```

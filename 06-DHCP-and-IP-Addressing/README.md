
# DHCP and IP Addressing

## 1. Introduction
DHCP (Dynamic Host Configuration Protocol) automatically assigns IP configuration to network devices.

## 2. DHCP DORA Process

DHCP works through four steps:

1. Discover – Client searches for a DHCP server.
2. Offer – DHCP server offers an IP address.
3. Request – Client requests the offered IP.
4. Acknowledgment – Server confirms the IP assignment.

## 3. Static IP vs Dynamic IP

| Static IP | Dynamic IP |
|---|---|
| Manually configured | Automatically assigned |
| Usually remains fixed | May change |
| Used for servers and network devices | Commonly used for client devices |

## 4. Windows IP Configuration Commands

```text
ipconfig
ipconfig /all
ipconfig /release
ipconfig /renew
ipconfig /flushdns
```

## 5. Important IP Information

Example:

- IP Address: 192.168.1.100
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1
- DNS Server: 8.8.8.8

These are sample values.

## 6. Cisco DHCP Verification Commands

```text
show ip interface brief
show vlan brief
show interfaces trunk
show running-config
show ip dhcp binding
show ip dhcp pool
```

Note: DHCP server commands are available only when the switch supports and is configured for the DHCP server role.

## 7. DHCP Troubleshooting

Common problems:
- DHCP server not reachable.
- DHCP scope exhausted.
- Incorrect VLAN assignment.
- DHCP relay (ip helper-address) missing or incorrect.
- Network connectivity issue.

Troubleshooting steps:
1. Check the client's IP configuration.
2. Verify physical connectivity.
3. Check VLAN assignment.
4. Verify DHCP server availability.
5. Check DHCP scope and relay configuration.
6. Renew the client's IP address.

## 8. DNS Troubleshooting

```text
nslookup google.com
ipconfig /displaydns
ipconfig /flushdns
ping 8.8.8.8
```

## Disclaimer
All IP addresses and configurations are fictional examples for educational purposes.

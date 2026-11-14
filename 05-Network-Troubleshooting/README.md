
# Network Troubleshooting

## 1. Introduction
This project covers common network issues and step-by-step troubleshooting methods used by Network Support Engineers.

## 2. No IP Address – 169.254.x.x

Possible reasons:
- DHCP server not reachable.
- Incorrect VLAN assignment.
- Switch port issue.
- Network cable problem.

Troubleshooting commands:

```text
ipconfig /all
ipconfig /release
ipconfig /renew
ping 192.168.1.1
```

Switch commands:

```text
show interfaces status
show vlan brief
show mac address-table
```

## 3. LAN Connectivity Issues

Troubleshooting steps:
1. Check network cable.
2. Check link LED on the switch.
3. Verify switch port status.
4. Check the device IP address.
5. Ping the default gateway.
6. Check VLAN assignment.

## 4. DHCP Troubleshooting

Commands:

```text
ipconfig /all
ipconfig /renew
show vlan brief
show interfaces trunk
```

Check:
- DHCP server availability.
- Correct VLAN.
- DHCP scope availability.
- DHCP relay configuration, if applicable.

## 5. MAC Address Troubleshooting

Commands:

```text
show mac address-table
show mac address-table dynamic
show mac address-table interface gigabitEthernet 1/0/1
```

## 6. Switch Port Troubleshooting

Commands:

```text
show interfaces status
show interfaces gigabitEthernet 1/0/1
show interfaces counters errors
show logging
```

## 7. Ping and Gateway Testing

```text
ping 192.168.1.1
tracert 8.8.8.8
ipconfig /all
```

## 8. Troubleshooting Methodology

1. Identify the issue.
2. Collect IP and connectivity information.
3. Check physical connectivity.
4. Verify VLAN and switch port.
5. Check DHCP and gateway.
6. Test connectivity.
7. Document the resolution.

## Disclaimer
All IP addresses and examples are fictional and provided for educational purposes only.

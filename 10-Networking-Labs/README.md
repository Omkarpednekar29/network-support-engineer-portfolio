
# Networking Labs

## 1. Introduction

This section contains practical networking exercises designed to improve Cisco networking and troubleshooting skills.

## 2. Lab 1 – VLAN Configuration

Objective: Create two VLANs.

```text
configure terminal
vlan 10
name HR
exit
vlan 20
name IT
end
show vlan brief
```

## 3. Lab 2 – Access Port Configuration

Objective: Assign a switch port to VLAN 10.

```text
configure terminal
interface gigabitEthernet 1/0/1
switchport mode access
switchport access vlan 10
end
show vlan brief
```

## 4. Lab 3 – Trunk Port Configuration

Objective: Configure a trunk port.

```text
configure terminal
interface gigabitEthernet 1/0/24
switchport mode trunk
switchport trunk allowed vlan 10,20
end
show interfaces trunk
```

## 5. Lab 4 – STP Verification

Objective: Check spanning-tree status.

```text
show spanning-tree
show spanning-tree summary
show spanning-tree vlan 10
```

## 6. Lab 5 – EtherChannel Verification

Objective: Check EtherChannel status.

```text
show etherchannel summary
show interfaces port-channel 1
```

## 7. Lab 6 – DHCP Troubleshooting

Objective: Troubleshoot a client that is not receiving an IP address.

Windows commands:

```text
ipconfig /all
ipconfig /release
ipconfig /renew
ping 192.168.1.1
```

## 8. Lab 7 – Port Security Verification

Objective: Check port security configuration.

```text
show port-security
show port-security interface gigabitEthernet 1/0/1
show port-security address
```

## 9. Lab Tools

- Cisco Packet Tracer
- EVE-NG
- Draw.io
- Cisco IOS CLI

## 10. Learning Goals

- Practice Cisco switching.
- Understand VLAN and trunking.
- Learn network troubleshooting.
- Improve command-line skills.
- Build practical networking knowledge.

## Disclaimer

All lab examples use fictional values and are intended for educational purposes. Test configurations in a lab environment before applying them to production networks.

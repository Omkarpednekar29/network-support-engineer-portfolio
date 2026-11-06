
# Cisco CLI Commands

## 1. Switch Information
```text
show version
show inventory
show clock
show running-config
show startup-config
```

## 2. Interface Commands
```text
show interfaces status
show ip interface brief
show interfaces gigabitEthernet 1/0/1
show interfaces counters errors
```

## 3. VLAN Commands
```text
show vlan brief
show interfaces trunk
show vlan id 10
```

## 4. MAC Address Commands
```text
show mac address-table
show mac address-table dynamic
show mac address-table address XXXX.XXXX.XXXX
```

## 5. Port Security Commands
```text
show port-security
show port-security interface gigabitEthernet 1/0/1
show port-security address
```

## 6. STP Commands
```text
show spanning-tree
show spanning-tree vlan 10
```

## 7. EtherChannel Commands
```text
show etherchannel summary
show interfaces port-channel 1
```

## 8. Troubleshooting Commands
```text
ping 192.168.1.1
traceroute 192.168.1.1
show logging
show cdp neighbors
show lldp neighbors
```

## Disclaimer
These commands are provided for learning and reference purposes. Interface names, VLAN IDs and IP addresses are examples. Verify the device and environment before running commands.

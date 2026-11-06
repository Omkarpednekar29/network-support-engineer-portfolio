
# VLAN and Trunking

## 1. Introduction
VLAN (Virtual Local Area Network) divides a physical network into multiple logical networks.

Trunk ports carry traffic from multiple VLANs between network devices.

## 2. Create VLANs

Example: Create VLAN 10 and VLAN 20.

```text
configure terminal
vlan 10
name HR
exit
vlan 20
name IT
exit
end
```

## 3. Configure Access Port

Assign interface GigabitEthernet 1/0/1 to VLAN 10.

```text
configure terminal
interface gigabitEthernet 1/0/1
switchport mode access
switchport access vlan 10
no shutdown
end
```

## 4. Configure Trunk Port

Configure interface GigabitEthernet 1/0/24 as a trunk.

```text
configure terminal
interface gigabitEthernet 1/0/24
switchport mode trunk
switchport trunk allowed vlan 10,20
no shutdown
end
```

## 5. Verification Commands

```text
show vlan brief
show interfaces trunk
show interfaces status
show running-config
```

## 6. Troubleshooting

Common issues:
- VLAN is not created.
- Access port assigned to the wrong VLAN.
- VLAN is missing from the trunk allowed list.
- Trunk link is down.
- Incorrect cabling or interface configuration.

## 7. Important Notes
- VLAN IDs 10 and 20 are sample values.
- Interface numbers are examples.
- Verify the switch model and configuration before applying commands.
- Test configurations in a lab environment first.

## Disclaimer
All configurations are sample examples for educational purposes. No actual company or campus network information is included.

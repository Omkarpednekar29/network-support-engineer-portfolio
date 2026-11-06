
# STP and EtherChannel

## 1. Introduction

### Spanning Tree Protocol (STP)
STP prevents Layer 2 switching loops by blocking redundant paths when necessary.

### EtherChannel
EtherChannel combines multiple physical links into one logical link to increase bandwidth and provide redundancy.

## 2. STP Verification Commands

```text
show spanning-tree
show spanning-tree vlan 10
show spanning-tree summary
show spanning-tree root
```

## 3. Configure STP Priority

Example: Set switch priority for VLAN 10.

```text
configure terminal
spanning-tree vlan 10 priority 4096
end
```

## 4. Configure PortFast

Use PortFast on appropriate end-device access ports only.

```text
configure terminal
interface gigabitEthernet 1/0/1
spanning-tree portfast
end
```

## 5. EtherChannel Verification

```text
show etherchannel summary
show etherchannel port-channel
show interfaces port-channel 1
```

## 6. Configure LACP EtherChannel

Example using two physical interfaces:

```text
configure terminal
interface range gigabitEthernet 1/0/1 - 2
channel-group 1 mode active
exit

interface port-channel 1
switchport mode trunk
switchport trunk allowed vlan 10,20
end
```

## 7. Troubleshooting

Common STP issues:
- Unexpected blocked ports.
- Incorrect root bridge selection.
- Layer 2 loops.
- Incorrect STP configuration.

Common EtherChannel issues:
- Interfaces not bundled.
- LACP negotiation failure.
- Speed or duplex mismatch.
- Trunk configuration mismatch.
- Incorrect VLAN allowed list.

## 8. Important Notes
- Use matching configurations on both ends of an EtherChannel.
- Verify interface compatibility before configuration.
- Test in a lab environment before production use.

## Disclaimer
All configurations are sample examples for educational purposes. No actual company or campus network information is included.


# Cisco IP Phones and CUCM

## 1. Introduction

Cisco Unified Communications Manager (CUCM) provides call processing and management for Cisco IP phones.

## 2. Cisco IP Phone Models

Common Cisco IP phone models:

- Cisco CP-8845
- Cisco CP-7821
- Cisco CP-7841
- Cisco CP-8865
- Cisco CP-3905

## 3. How IP Phone Registration Works

1. Connect the IP phone to a PoE switch port.
2. Phone receives an IP address through DHCP.
3. Phone discovers the CUCM TFTP server.
4. Phone downloads its configuration.
5. Phone registers with CUCM.

## 4. Important Troubleshooting Commands

### Check switch interface

```text id="x6k9qr"
show interfaces status
show interfaces gigabitEthernet 1/0/1
show power inline
```

### Find phone MAC address

```text id="5g4r5x"
show mac address-table
show mac address-table dynamic
```

### Check VLAN configuration

```text id="ct0qbs"
show vlan brief
show interfaces trunk
```

## 5. Common IP Phone Issues

### Phone not powering on
- Check PoE availability.
- Check switch port status.
- Test using another known-good PoE port.

### Phone stuck on Cisco logo
- Check power and network connectivity.
- Verify DHCP and TFTP availability.
- Check phone firmware and CUCM registration.

### Phone not registering
- Verify IP address.
- Verify voice VLAN.
- Check TFTP and CUCM connectivity.
- Verify phone MAC address and configuration in CUCM.

### No dial tone
- Check phone registration.
- Verify extension assignment.
- Check CUCM device configuration.

## 6. Phone Replacement Documentation

Maintain these details when replacing a phone:

| Field | Example |
|---|---|
| User | Sample User |
| Model | CP-8845 |
| Old Serial Number | SAMPLE-OLD-001 |
| New Serial Number | SAMPLE-NEW-001 |
| Old MAC Address | 0000.0000.0001 |
| New MAC Address | 0000.0000.0002 |
| Issue | Hardware fault |
| Status | Replaced |

All values above are fictional examples.

## 7. Learning Objectives

- Understand IP phone registration.
- Learn voice VLAN concepts.
- Troubleshoot phone connectivity.
- Understand CUCM device management.
- Maintain replacement records.

## Disclaimer

This documentation is for educational purposes. All device details and examples are fictional. No actual user, phone, or company information is included.

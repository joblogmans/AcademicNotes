# USB
Universal Serial Bus. Multiple generations exist.

## Physical properties
USB 1 and 2 use 4 pins:
- Vcc
- GND
- Data- & Data+ (differential twisted pair)

USB 3 adds another data pair, allowing for [[Duplex#Full Duplex|full duplex]] communication.

## Performance
Data rates per generation:
- USB1.0 - 1.5 Mbit/s
- USB2.0 - 480 Mbit/s
- USB3.0 - 5 Gbit/s
- USB3.1 - 10 Gbit/s

## Structure
In an USB network, there is only one host, possibly with several hubs with several devices. The host polls the hubs for status. Thus the network is polling-based. When a hub detects a new device, the hub will notify the host (via polling?), the new device sends information and gets a new address and is thus added to the network. When unplugged, the hub will notify the host which will remove the unplugged device from its list.

### Device classes
- Audio (01h)
- Human interface devices (03h)
- Mass storage (08h)
- Printer class (07h)
- Communication (02h)

### Protocol
Transfers consists of packets. Multiple transfer types exist:
- Control transfer
- Bulk transfer
- Isochronous transfer
- Interrupt transfer

Packets consists of:
- Start bit synchronization
- Packet ID (PID)
- Content
- CRC - error detecting
Packet types:
- Token - determines a transfer type
- Data
- Handshaking
- Descriptor

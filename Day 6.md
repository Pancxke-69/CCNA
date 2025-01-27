## Router Solicitation and Router Advertisements
* IPv6 routers periodically send out ICMPv6 RA messages, every 200 seconds, to all IPv6-enabled devices on the network.
#### Multicast Addresses
* Router Soliciation (Sent to ALL IPv6 ROUTERS) - FF02::2
* Router Advertisement (Sent to ALL IPv6 NODES) - FF02::1
#### EUI-64 Process
* Ethernet MAC addresses are usually represented in hexadecimal and are made up of two parts:
  * **Organizationally Unique Identifier (OUI)** - The OUI is a 24-bit (6 hexadecimal digits) vendor code assigned by IEEE.
  * **Device Identifier** - The device identifier is a unique 24-bit (6 hexadecimal digits) value within a common OUI.
* Process (fc:99:47:75:ce:eo)
```
    Step 1: Split the MAC Address (1111 1100:1001 1001:0100 0111:                   :1111 0101:1100 1110:1110 0000)
    Step 2: Insert fffe           (1111 1100:1001 1001:0100 0111:1111 1111:1111 1110:1111 0101:1100 1110:1110 0000)
    Step 3: Flip the u/I bit      (1111 1110:1001 1001:0100 0111:1111 1111:1111 1110:1111 0101:1100 1110:1110 0000)
    Modified (fe:99:47:ff:fe:75:ce:e0)
```

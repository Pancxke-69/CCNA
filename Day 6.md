## Router Solicitation and Router Advertisements
* IPv6 routers periodically send out ICMPv6 RA messages, every 200 seconds, to all IPv6-enabled devices on the network.
#### Multicast Addresses
* Router Soliciation (Sent to ALL IPv6 ROUTERS) - FF02::2
* Router Advertisement (Sent to ALL IPv6 NODES) - FF02::1
#### EUI-64 Process
* Ethernet MAC addresses are usually represented in hexadecimal and are made up of two parts:
  * **Organizationally Unique Identifier (OUI)** - The OUI is a 24-bit (6 hexadecimal digits) vendor code assigned by IEEE.
  * **Device Identifier** - The device identifier is a unique 24-bit (6 hexadecimal digits) value within a common OUI.

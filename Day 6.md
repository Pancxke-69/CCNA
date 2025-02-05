## Router Solicitation and Router Advertisements
* IPv6 routers periodically send out ICMPv6 RA messages, every 200 seconds, to all IPv6-enabled devices on the network.
* This whole setup makes it easy to plug and play devices on the network. All you need to do is configure the router and all the nodes on the network will revieve info on how to configure themselves.
* `ipv6 unicast-routing` enables dynamic addressing
#### Multicast Addresses
* Router Soliciation (Sent to ALL IPv6 ROUTERS) - FF02::2
* Router Advertisement (Sent to ALL IPv6 NODES) - FF02::1
## 3 Methods for RA Messages (Router --> Nodes) #2 is Prefered
`RA Contains a bit, and that bit is what says what method it is using`
* **SLAAC** - "I have everything you need including the prefix, prefix length, and default gateway address."
  * SLAAC is a method that allows a device to create its own GUA without the services of DHCPv6. Using SLAAC, devices rely on the ICMPv6 RA messages of the local router to obtain the necessary information.
* **SLAAC with a stateless DHCPv6 server** - "Here is my information but you need to get other information such as DNS addresses from a stateless DHCPv6 server."
  * A stateless DHCPv6 server distributes DNS server addresses and domain names. It does not allocate GUAs.
* **Stateful DHCPv6 (no SLAAC)** - "I can give you your default gateway address. You need to ask a stateful DHCPv6 server for all your other information."
  * A device can automatically receive its addressing information including a GUA, prefix length, and the addresses of DNS servers from a stateful DHCPv6 server.


## Dynamicly created Interface ID vs Randomly Generated ID
#### EUI-64 Process
* Ethernet MAC addresses are usually represented in hexadecimal and are made up of two parts:
  * **Organizationally Unique Identifier (OUI)** - The OUI is a 24-bit (6 hexadecimal digits) vendor code assigned by IEEE.
  * **Device Identifier** - The device identifier is a unique 24-bit (6 hexadecimal digits) value within a common OUI.
* Process
```
    Start:   (fc:99:47:75:ce:eo)
    Step 1: Split the MAC Address (1111 1100:1001 1001:0100 0111:                   :1111 0101:1100 1110:1110 0000)
    Step 2: Insert fffe           (1111 1100:1001 1001:0100 0111:1111 1111:1111 1110:1111 0101:1100 1110:1110 0000)
    Step 3: Flip the u/I bit      (1111 1110:1001 1001:0100 0111:1111 1111:1111 1110:1111 0101:1100 1110:1110 0000)
    Modified (fe:99:47:ff:fe:75:ce:e0)
```
* Example
```
    C:\> ipconfig
    Windows IP Configuration
    Ethernet adapter Local Area Connection:
       Connection-specific DNS Suffix  . :
       IPv6 Address. . . . . . . . . . . : 2001:db8:acad:1:fc99:47ff:fe75:cee0
       Link-local IPv6 Address . . . . . : fe80::fc99:47ff:fe75:cee0
       Default Gateway . . . . . . . . . : fe80::1
    C:\>
```
#### Random 64-Bit Generated ID
* To ensure there are no duplicate IDs, the client will send out a DAD (Duplicate Address Detection) that is similar to ARP. If there is no reply then the address is unique.
* Example
```
    C:\> ipconfig
    Windows IP Configuration
    Ethernet adapter Local Area Connection:
       Connection-specific DNS Suffix  . :
       IPv6 Address. . . . . . . . . . . : 2001:db8:acad:1:50a5:8a35:a5bb:66e1
       Link-local IPv6 Address . . . . . : fe80::50a5:8a35:a5bb:66e1
       Default Gateway . . . . . . . . . : fe80::1
    C:\>
```
## Solicited Node IPv6 Multicast Addresses
* Similar to "All-Nodes Multicast". It allows the nodes to look at the Destination MAC in the layer 2 portion of the header (Ethernet) and immediately know who the multicast is for.
## Data Link Layer
* Enables upper layers to access the media
* Accepts data (Layer 3 packets) and encapsulates them into layer 2 frames
* Controls how data is placed on the media and how it is taken off of the media.
#### LAN/MAN Sublayers
* **Logical Link Control(LLC)** - Commumicates between networking software at the upper layers and the device hardware at the lower layers
* **Media Access Control(MAC)** - Responsible for data encapsulation and media access control. Provides data link layer addressing and it is integrated with various physical layer tech.
#### Providing Access to the Media
* At each hop along the path, the router performs the following layer 2 functions:
  * Accepts a frame from a medium
  * De-Encapsulates the frame
  * Re-Encapsulates the packet into a new frame
  * Forwards the new frame appropriate to the medium of that segment of the physical network








### What are two functions of NVRAM? (Choose two.)
- [ ] to store the ARP table
- [x] to store the startup configuration file
- [ ] to store the routing table
- [x] to retain contents when power is removed
- [ ] to contain the running configuration file

---

### What happens when the `transport input ssh` command is entered on the switch VTY lines?
- [x] Communication between the switch and remote users is encrypted.
- [ ] The switch requires remote connections via a proprietary client software.
- [ ] The switch requires a username/password combination for remote access.
- [ ] The SSH client on the switch is enabled.

---

### The global configuration command `ip default-gateway 172.16.100.1` is applied to a switch. What is the effect of this command?
- [ ] The switch can communicate with other hosts on the 172.16.100.0 network.
- [ ] The switch will have a management interface with the address 172.16.100.1.
- [x] The switch can be remotely managed from a host on another network.
- [ ] The switch is limited to sending and receiving frames to and from the gateway 172.16.100.1.

---

### A new network administrator has been asked to enter a banner message on a Cisco device. What is the fastest way a network administrator could test whether the banner is properly configured?
- [ ] Power cycle the device.
- [ ] Reboot the device.
- [ ] Enter CTRL-Z at the privileged mode prompt.
- [x] Exit privileged EXEC mode and press Enter.
- [ ] Exit global configuration mode.

---

### Which two functions are primary functions of a router? (Choose two.)
- [ ] flow control
- [ ] microsegmentation
- [ ] domain name resolution
- [x] packet forwarding
- [x] path selection

---

### What property of ARP forces all Ethernet NICs to process an ARP request?
- [ ] ARP replies are broadcast on the network when a host receives an ARP request.
- [ ] The type field 0x806 appears in the header of the Ethernet frame.
- [ ] The source MAC address appears in the header of the Ethernet frame.
- [x] The destination MAC address FF-FF-FF-FF-FF-FF appears in the header of the Ethernet frame.

---

### Which term describes a field in the IPv4 packet header that contains a 32-bit binary value associated with an interface on the sending device?
- [x] source IPv4 address
- [ ] TTL
- [ ] protocol
- [ ] destination IPv4 address

---

### Under which two circumstances will a switch flood a frame out of every port except the port that the frame was received on? (Choose two.)
- [ ] The source address in the frame header is the broadcast address.
- [ ] The source address in the frame is a multicast address.
- [x] The frame has the broadcast address as the destination address.
- [ ] The destination address in the frame is a known unicast address.
- [x] The destination address is unknown to the switch.

---

### Which destination address is used in an ARP request frame?
- [ ] AAAA.AAAA.AAAA
- [ ] 0.0.0.0
- [x] FFFF.FFFF.FFFF
- [ ] 255.255.255.255
- [ ] the physical address of the destination host

---

### Which two types of IPv6 messages are used in place of ARP for address resolution?
- [ ] echo reply
- [ ] anycast
- [x] neighbor advertisement
- [ ] broadcast
- [x] neighbor solicitation
- [ ] echo request

---

### What is the effect of using the `Router# copy running-config startup-config` command on a router?
- [x] The contents of NVRAM will change.
- [ ] The contents of flash will change.
- [ ] The contents of ROM will change.
- [ ] The contents of RAM will change.

---

### What are two potential network problems that can result from ARP operation? (Choose two.)
- [x] On large networks with low bandwidth, multiple ARP broadcasts could cause data communication delays.
- [ ] Manually configuring static ARP associations could facilitate ARP poisoning or MAC address spoofing.
- [ ] Multiple ARP replies result in the switch MAC address table containing entries that match the MAC addresses of hosts that are connected to the relevant switch port.
- [x] Network attackers could manipulate MAC address and IP address mappings in ARP messages with the intent of intercepting network traffic.
- [ ] Large numbers of ARP request broadcasts could cause the host MAC address table to overflow and prevent the host from communicating on the network.

---

### Why is NAT not needed in IPv6?​
- [x] Any host or user can get a public IPv6 network address because the number of available IPv6 addresses is extremely large.​
- [ ] Because IPv6 has integrated security, there is no need to hide the IPv6 addresses of internal networks.​
- [ ] The end-to-end connectivity problems that are caused by NAT are solved because the number of routes increases with the number of nodes that are connected to the Internet.
- [ ] The problems that are induced by NAT applications are solved because the IPv6 header improves packet handling by intermediate routers.​

---

### Which statement describes a feature of the IP protocol?
- [ ] IP encapsulation is modified based on network media.
- [ ] MAC addresses are used during the IP packet encapsulation.
- [ ] IP relies on Layer 2 protocols for transmission error control.
- [x] IP relies on upper layer services to handle situations of missing or out-of-order packets.

---

### How do hosts ensure that their packets are directed to the correct network destination?
- [ ] They search in their own local routing table for a route to the network destination address and pass this information to the default gateway.
- [ ] They send a query packet to the default gateway asking for the best route.
- [x] They have to keep their own local routing table that contains a route to the loopback interface, a local network route, and a remote default route.​
- [ ] They always direct their packets to the default gateway, which will be responsible for the packet delivery.

---

### What routing table entry has a next hop address associated with a destination network?
- [x] Remote routes
- [ ] Local routes
- [ ] Directly-connected routes
- [ ] C and L source routes

---

### What is one advantage that the IPv6 simplified header offers over IPv4?
- [ ] Smaller-sized header
- [ ] Little requirement for processing checksums
- [ ] Smaller-sized source and destination IP addresses
- [x] Efficient packet handling

---

### What are two services provided by the OSI network layer? (Choose two.)
- [ ] Performing error detection
- [ ] Placement of frames on the media
- [x] Encapsulating PDUs from the transport layer
- [ ] Collision detection
- [x] Routing packets toward the destination

---

### A computer can access devices on the same network but cannot access devices on other networks. What is the probable cause of this problem?
- [ ] The cable is not connected properly to the NIC.
- [ ] The computer has an invalid IP address.
- [x] The computer has an invalid default gateway address.
- [ ] The computer has an incorrect subnet mask.

---

### When transporting data from real-time applications, such as streaming audio and video, which field in the IPv6 header can be used to inform the routers and switches to maintain the same path for the packets in the same conversation?  
- [ ] Traffic Class  
- [x] Flow Label  
- [ ] Differentiated Services  
- [ ] Next Header  

---

### Within a production network, what is the purpose of configuring a switch with a default gateway address?  
- [ ] Hosts that are connected to the switch can use the switch default gateway address to forward packets to a remote destination.  
- [ ] A switch must have a default gateway to be accessible by Telnet and SSH.  
- [x] The default gateway address is used to forward packets originating from the switch to remote networks.  
- [ ] It provides a next-hop address for all traffic that flows through the switch.  

---

### Which statement describes the treatment of ARP requests on the local link?  
- [ ] They are received and processed only by the target device.  
- [ ] They must be forwarded by all routers on the local network.  
- [x] They are received and processed by every device on the local network.  
- [ ] They are dropped by all switches on the local network.  

---

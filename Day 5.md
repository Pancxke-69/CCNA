## Protocols and Models
#### Message Timing
* Flow Control - Process of managing the rate of data transmission
* Response Timeout - If person asks question and doesnt get an answer, it will react accordingly
* Access Method - Determines when someone can send a message
#### Protocol Types
* Network Communcation - Enable 2 or more devices to communicate with eachother over one or more networks
* Network Security - Secure data to provice authentication, security, and data encryption
* Routing - Enables routers to exchange information (OSPF, BGP)
* Service Discovery - Used for automatic detection of devices or services (DHCP, DNS)
#### Protocol Suits
* Apple Talk - Came out 1985 and ended in 1995 to tcp/ip
* IPX - Switched to tcp/ip in 1985
#### Protocol Sections
* Application Layer - Name system, Host config, Email, File Transfer, Web and Web service
* Transport Layer - TCP/UDP
* Internet Layer - Internet protocol, Messaging (ICMP), Routing protocols
* Network Access Layer - Address Resolution, Data Link protocols (Ethernet, WLAN)
- Open Standard Protocol - Anybody can use it (Publicly available)
- Standards=based protocol suits - Endorsed by networking industry
#### Standards Organizations
* IEEE - Electrical Engineering and Electronics (802.11, 802.3, ect.)
* IANA - IP Address management
* IETF - maintains and updates TCP/IP technologies
* ICANN - Coordinates IP address allocation and the management of domain names (Boss of IANA)
* ITU - Video compression and broadband connections (Oldest open standards body)
* TIA - Cabling Standards and physical equiptment standards (Works together with EIA)
#### OSI Model (Reference) and TCP/IP Model (Working)
* Application  -  Application
* Presentation -  Application
* Session      -  Application (Keeps track of conversations)
* Transport    -  Transport (Creates Segments)
* Network      -  Internet (Creates Packets)
* Data Link    -  Network Access (Creates Frames) 
* Physical     -  Network Access
## IPv6 Addressing
#### IPv4 and v6 Coexistence
* Dual stack - PC with both IPv6 and v4 capabilities
* Tunneling - Encapsulated v6 packet with v4 to go through a v4 network
* Translation - Translates the v6 packet into v4 (Avoid this)
#### IPv6 Representation
* Rule 1 - Omit the leading zeros (Beginning of each hextet)
* Rule 2 - Compress consecutive sets of all zeroes between 2 colons (::), but only once!
#### 3 Cast's
* Unicast - Uniquely identifies an interface on IPv6 device
* Multicast - Sends one packet to multiple destinations
* Anycast - Delivered to the nearest member of the anycast group, unlike muklticast where it sends to every member regardless of location
#### Unicast Addresses
* GLobal (Relevant) 2001: or 3001: Globally routable anywhere in the world (Your organization or Internet). Public address that can be routed internally
* Link-Local (Relevant) - FE80:: Only usable to communicate on the same local network. Cannot be routed. Mandatory for all IPv6 hosts. They are auto-assigned
* Loopback
* Unspecified
* Unique - FC00:: Slightly similar to private IPv4 addresses. They are routable throughout your organization, but not the internet
* Embedded - When you convert an IPv4 address into a v6 address, you can embed it
#### Subnetting IPv6
- Global Routing Prefix - First 48 bits
- Subnet ID - Next 16 bits
- Interface ID - Next 64 bits

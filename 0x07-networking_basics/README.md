0x07. Networking basics #0


0. OSI model

The OSI (Open Systems Interconnection) model is a conceptual framework used to describe how data is transmitted over a network. It was developed by the International Organization for Standardization (ISO) in the 1980s to standardize communication protocols across different network devices.

The OSI model consists of seven layers, each with a specific function and purpose. The layers are:

Physical layer: This layer defines the physical media used to transmit data, such as cables, wireless signals, and connectors.

Data Link layer: This layer is responsible for providing reliable data transfer across a physical link. It is also responsible for detecting and correcting errors in data transmission.

Network layer: This layer is responsible for addressing and routing data between different networks. It uses logical addressing schemes, such as IP addresses, to identify devices on a network.

Transport layer: This layer is responsible for ensuring reliable end-to-end data transmission by providing error checking, flow control, and congestion avoidance.

Session layer: This layer establishes and manages connections between applications on different devices. It is responsible for managing the exchange of data between applications.

Presentation layer: This layer is responsible for data formatting, encryption, and decryption. It is responsible for converting data between different formats so that it can be understood by different applications.

Application layer: This layer is the highest level of the OSI model and provides services to end-users, such as email, web browsing, and file transfer.

The OSI model provides a standardized way of describing how network devices communicate with each other. It is often used as a reference model for understanding how different network protocols, such as TCP/IP, fit together.





1. Types of network


There are several types of networks, including:

LAN (Local Area Network): A LAN is a network that covers a small geographic area, such as a single building or office. It is typically used to connect computers and devices within a single organization.

WAN (Wide Area Network): A WAN is a network that covers a large geographic area, such as a city, country, or even multiple countries. It is typically used to connect LANs together over long distances.

MAN (Metropolitan Area Network): A MAN is a network that covers a larger area than a LAN but smaller than a WAN, such as a city or town. It is typically used to connect multiple LANs together.

WLAN (Wireless Local Area Network): A WLAN is a type of LAN that uses wireless technology, such as Wi-Fi, to connect devices.

PAN (Personal Area Network): A PAN is a network that covers a very small area, typically a few meters. It is typically used to connect personal devices, such as smartphones and laptops, together.

VPN (Virtual Private Network): A VPN is a network that is created over a public network, such as the Internet. It is typically used to provide secure remote access to a private network.

Intranet: An intranet is a private network that is used within an organization. It is typically used to share resources, such as files and applications, among employees.

Extranet: An extranet is a network that is used to provide secure access to resources for external users, such as customers, suppliers, and partners.

These are some of the most common types of networks, but there are other types as well, such as SAN (Storage Area Network) and CAN (Campus Area Network).


2. MAC and IP address


MAC (Media Access Control) address and IP (Internet Protocol) address are two different types of addresses used to identify devices on a network.

A MAC address is a unique identifier assigned to a network interface controller (NIC) by the manufacturer. It is a 48-bit address composed of six pairs of hexadecimal digits, separated by colons or hyphens. MAC addresses are used to identify devices on a local network, such as a LAN. MAC addresses are assigned to the physical hardware of the device and do not change, even if the device is moved to a different network.

On the other hand, an IP address is a logical address assigned to a device on a network, which identifies the network and the specific device on that network. An IP address is a 32-bit or 128-bit address, depending on whether it is an IPv4 or IPv6 address. IPv4 addresses are composed of four decimal numbers, separated by periods, while IPv6 addresses are composed of hexadecimal numbers, separated by colons. IP addresses are used to route data packets between devices on different networks. IP addresses can be assigned dynamically (DHCP) or manually (static) and can change if a device moves to a different network.

In summary, MAC addresses are used to identify devices on a local network, while IP addresses are used to route data packets between devices on different networks. MAC addresses are assigned to the physical hardware of the device and do not change, while IP addresses can be dynamically or manually assigned and can change if the device moves to a different network.



3. UDP and TCP


UDP (User Datagram Protocol) and TCP (Transmission Control Protocol) are two different transport layer protocols used in computer networks.

UDP is a connectionless protocol that is used for sending datagrams (packets) over the network. It provides no error checking or retransmission of lost packets. Therefore, UDP is best suited for applications where speed is important and loss of some packets is tolerable, such as video streaming or online gaming.

TCP is a connection-oriented protocol that provides reliable, ordered, and error-checked delivery of packets. It establishes a connection between two devices and sends data in a series of packets. TCP ensures that packets are delivered in the correct order and can retransmit lost packets to ensure that all data is received. Therefore, TCP is best suited for applications where data integrity is important, such as file transfers, email, and web browsing.

Some of the main differences between UDP and TCP are:

Connection-oriented vs connectionless: TCP establishes a connection between two devices before sending data, while UDP does not.
Reliability: TCP provides reliable delivery of data, while UDP does not guarantee delivery or ensure that packets are delivered in the correct order.
Speed: UDP is faster than TCP because it does not have the overhead of establishing a connection and providing reliable delivery of packets.
Resource usage: TCP uses more resources than UDP because it provides error checking and retransmission of lost packets.
In summary, UDP is a faster, connectionless protocol used for applications where speed is important and some data loss is tolerable. TCP is a slower, connection-oriented protocol used for applications where data integrity is important and reliable delivery of data is necessary.


4. TCP and UDP ports


In computer networking, both TCP and UDP use ports to identify different applications or services running on a network device.

TCP and UDP use 16-bit port numbers to identify the source and destination applications or services on a device. Port numbers range from 0 to 65535, with the well-known ports (0 to 1023) reserved for system services and applications, and the registered and dynamic ports (1024 to 65535) available for use by any application or service.

TCP ports are associated with connection-oriented protocols that require a reliable data delivery mechanism, such as email, file transfers, and web browsing. Some common TCP ports and their associated services include:

Port 20, 21: FTP (File Transfer Protocol)
Port 22: SSH (Secure Shell)
Port 25: SMTP (Simple Mail Transfer Protocol)
Port 80: HTTP (Hypertext Transfer Protocol)
Port 443: HTTPS (HTTP Secure)
Port 3389: RDP (Remote Desktop Protocol)
UDP ports, on the other hand, are associated with connectionless protocols that do not require a reliable data delivery mechanism, such as streaming video and online gaming. Some common UDP ports and their associated services include:

Port 53: DNS (Domain Name System)
Port 69: TFTP (Trivial File Transfer Protocol)
Port 123: NTP (Network Time Protocol)
Port 5060: SIP (Session Initiation Protocol)
Port 5061: SIP-TLS (Session Initiation Protocol over Transport Layer Security)
In summary, both TCP and UDP use port numbers to identify different applications or services running on a network device. TCP ports are associated with connection-oriented protocols that require a reliable data delivery mechanism, while UDP ports are associated with connectionless protocols that do not require a reliable data delivery mechanism.


5. Is the host on the network


To determine whether a host is on a network, you need to perform some type of network discovery or scanning process. This can be done using various network scanning tools that send out packets to detect active hosts on the network.

One commonly used tool for network discovery is called the Ping utility. It sends out an ICMP (Internet Control Message Protocol) echo request packet to a specific IP address and waits for a response. If the host is active and reachable on the network, it should respond with an ICMP echo reply packet.

Another tool for network discovery is called Nmap. It is a network exploration and security auditing tool that can scan networks and identify hosts, services, and operating systems running on them.

In summary, to determine whether a host is on a network, you need to use a network scanning tool such as Ping or Nmap to send out packets and detect active hosts on the network.

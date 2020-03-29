# Network Topic Research :taco:

## IP Networks
Each device on an IP network need 3 different pieces of information to communicate with other devices on the network:
- An IP address
- A subnet Mask
- A broadcast address
This usually looks like this:

```
198.41.12.151
```
Any router can determine the best path for forwarding packets from one group to another by:
- Examining the destination address in an IP packet that should be forwarded
- Using information from other devices or already configured.

There are two major attributes that make up an IP address
- Network: Tells the routers what group of devices a packet should go to

- Host: Tells the routers what specific device in that group the packet should go to.

Each group of devices on an ip network should have a unique network portion and each of the devices need to have a unique host portion. These portions can be obtained by using an NIC (Network information center).

NIC assigns blocks of addresses to ISPs (Internet service providers) who assigns these addresses to the customers.

## What is an IP?

IP stands for Internet Protocol, And an IP address is a unique number which is linked to the online activity of that IP.

Internet Protocol is a set of requirements for addressing and routing data on the internet. IP can be used with several transport protocols, including TCP and UDP. The data sent via the internet is divided into small pieces called packet. IP information is attached to each packet which means that the information is sent to the correct place. Each device or Domain has a unique IP address.

* TCP is Transmission Control Protocol, which is a connection-oriented protocol that computers use to communicate over the internet. It is the main protocol for IP Networks. TCP provides error checking and guarantees delivery of data.
* UDP is User Datagram Protocol, it is a connectionless protocol that works like TCP without error-checing and recovery services. UDP sends datagrams to the recipient whether they recieve them or not.


# IP addresses and Binary

## What is Binary?
Binary is the way a computer thinks. Using 1s and 0s, a computer makes "Decisions" using a series of millions of switches within a CPU. Each switch is either on (1) or off (0)

Binary is a base 2 number system - generally represented as a byte of 8 binary bits to represent numbers up to positive or negative 255 (or up to negative 127 using a floating point number.)

## IP Addresses.
IP is short for Internet Protocol, and is a unique address for each device that utilises the internet in some way, including servers, phones, and smart fridges.

There are two different common versions of IP addresses - <b>IPv4</b> is the older standard, a 32-bit value of 4 bytes represented in denary/decimal numbers. Once these started to run out, they advanced to IPv6, originally in the mid 1990s which can go up to 128-bits. IPv6 also uses an alpha-numeric system, using hexadecimal (base 16) to represent it's characters.

## Converting an IP address to binary.

1- take an IP address (204.132.40.155)
2- take each of the 4 numbers in the address (204, 132, 40, 155)
3- convert each one in to binary

       128  64  32  16  8  4  2  1
204     1    1   0   0  1  1  0  0

## Submask

A Subnet Mask (Submask) is a number that defines a range of IP addresses that can be used in a network. Submasks are used to designate subnetworks, or subnets, which are usually local networks which are connected to the internet. Systems within the same subnet can communicate directly with each other, yet external systems communicate via a router.

A Subnet Mask,hides the network part of a system's IP address and only leaves the host as the machine identifier. An example of this is that for the IP addresses 10.0.1.203 and 10.0.1.234 , they would be in the same subnet, yet 10.0.2.203 would be apart of a different subnet.

A common subnet mask for a class C IP address is 225.225.225.0 which allows for close to 256 unique hosts within a network. Larger networks would use the mask 225.225.0.0 which is class B. And the largest networks, class A would use the mask 225.0.0.0 .

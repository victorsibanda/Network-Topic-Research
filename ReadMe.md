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

## Network Research

### IPv4

IPv4 is the fourth version of the internet protocol (IP).

IPv4 addresses are 32-bit integers that can be expressed in hexadecimal notation. The format is x.x.x.x, where each x can be any value between 0 and 255.

IPv4 still routes most of today’s internet traffic. A 32-bit address space limits the number of unique hosts to 2^32, which is 4,294,967,296 IPv4 addresses for the world to use.

### IPv4 vs IPv6

IPv6 is the sixth version of the internet protocol (IP).

IPv6 moves from 32 bits to a 128-bit address space, with both letters and numbers in identifiers (for example, 2002:db8::8a3f:362:7897). IPv6 has 2^128 uniquely identifying addresses, which is about 340 undecillion.

The key differences between IPv4 and IPv6 are:
- IPv4 is 32-Bit IP address whereas IPv6 is a 128-Bit IP address.
- IPv4 is a numeric addressing method whereas IPv6 is an alphanumeric addressing method.
- IPv4 binary bits are separated by a dot(.) whereas IPv6 binary bits are separated by a colon(:).
- IPv4 offers 12 header fields whereas IPv6 offers 8 header fields.
- IPv4 supports broadcast whereas IPv6 doesn’t support broadcast.
- IPv4 has checksum fields while IPv6 doesn’t have checksum fields
- IPv4 supports VLSM (Virtual Length Subnet Mask) whereas IPv6 doesn’t support VLSM.
- IPv4 uses ARP (Address Resolution Protocol) to map to MAC address whereas IPv6 uses NDP (Neighbour Discovery Protocol) to map to MAC address.

## Limitations of IPv4:



1) lack of addresses space
 - Worth noting that in 1981 when it was created, the 4,294,967,296 possibilities were considered inexhaustible



2) Weak protocol extensibility - does not accommodate required number of additional parameters



3) Security - was never designed for security



4) Service support - placement of information about bandwidth, delays required for smooth operations



5) Geographic - Made in USA so just under 50% of addresses are reserved for the US

## Submask

A Subnet Mask (Submask) is a number that defines a range of IP addresses that can be used in a network. Submasks are used to designate subnetworks, or subnets, which are usually local networks which are connected to the internet. Systems within the same subnet can communicate directly with each other, yet external systems communicate via a router.


A Subnet Mask,hides the network part of a system's IP address and only leaves the host as the machine identifier. An example of this is that for the IP addresses 10.0.1.203 and 10.0.1.234 , they would be in the same subnet, yet 10.0.2.203 would be apart of a different subnet.

A common subnet mask for a class C IP address is 225.225.225.0 which allows for close to 256 unique hosts within a network. Larger networks would use the mask 225.225.0.0 which is class B. And the largest networks, class A would use the mask 225.0.0.0 .

## Finding if 2 ips in the same network are using submasks
Say if we had a mask of:
```
255.255.248.0
```
We will find that cidir (classless inner domain notation) will be...
```
255.255.248.0

to find the 1st octet 255:
128    64    32    16    8    4    2    1
  1     1     1     1    1    1    1    1


to find the 2nd octet 255:

128    64    32    16    8    4    2    1
  1     1     1     1    1    1    1    1

to find the 3rd octet 248:

128    64    32    16    8    4    2    1
  1     1     1     1    1    0    0    0

to find the 4th octet 0:

128    64    32    16    8    4    2    1
  0     0     0     0    0    0    0    0

255 = 11111111
255 = 11111111
248 = 11111000
0   = 00000000

```
altogether this is 11111111 11111111 11111000 00000000
counting only the 1s will make it 21
This is the cidir.

255 usually means every binary value is turned on in the octet as you can see

If we look at the ip 192.168.40.55

then compare it with our submask 255.255.248.0

what will be the network id?
```
As we know 255 is every value turned on so the first 2 octets stay the same

193.168.

Now we have to find the last two octets.

40 in binary is 00101000
so we compare it with the 248 submask octet

40  = 00101000
248 = 11111000

We can see 40 is in the networks that are turned on so it will stay the same: 40
192.168.40

Now the last one:

55 = 00110111
0  = 00000000

the 4th subnet octets are all off making them hosts so they will be 0
Now we have all of the octets for the network id which is 192.168.40.55

Now we need to add the cidir which is /21

We found the network id which is: 192.168.40.0/21

```
using the submask 255.255.248.0 we found the network id of the ip address 192.168.40.55 which was:

```
192.168.40.0/21
```
What if we had the same submask but different ip
if my ip was 192.168.45.55 what will my network id:

```
ip = 192.168.45.55

our submask was 255.255.248.0

we know that the cidir for this submask is /21

we know that since the first 2 octets in the submask are all turned on makes the first 2 octets to be: 192.168

lets find out what is 45

45 = 00101101

compare it to the 3rd octet
45  = 0 0 1 0 1 | 1 0 1
248 = 1 1 1 1 1 | 0 0 0

We can see only the first 5 bits are turned for the 248 octet meaning that the everything after the first 5 octets are hosts. There fore this will become 40
and we already know the last octet is 0

the network id is also 192.168.40.0/21
```

We can find out if two ips in the same network have a subnet by looking at their network id.

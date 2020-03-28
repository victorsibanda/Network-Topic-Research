# Network Topic Research :taco: 

**What is an IP?**

IP stands for Internet Protocol, And an IP address is a unique number which is linked to the online activity of that IP. 

Internet Protocol is a set of requirements for addressing and routing data on the internet. IP can be used with several transport protocols, including TCP and UDP. The data sent via the internet is divided into small pieces called packet. IP information is attached to each packet which means that the information is sent to the correct place. Each device or Domain has a unique IP address.

* TCP is Transmission Control Protocol, which is a connection-oriented protocol that computers use to communicate over the internet. It is the main protocol for IP Networks. TCP provides error checking and guarantees delivery of data. 
* UDP is User Datagram Protocol, it is a connectionless protocol that works like TCP without error-checing and recovery services. UDP sends datagrams to the recipient whether they recieve them or not. 

**Submask**

A Subnet Mask (Submask) is a number that defines a range of IP addresses that can be used in a network. Submasks are used to designate subnetworks, or subnets, which are usually local networks which are connected to the internet. Systems within the same subnet can communicate directly with each other, yet external systems communicate via a router. 

A Subnet Mask,hides the network part of a system's IP address and only leaves the host as the machine identifier. An example of this is that for the IP addresses 10.0.1.203 and 10.0.1.234 , they would be in the same subnet, yet 10.0.2.203 would be apart of a different subnet. 

A common subnet mask for a class C IP address is 225.225.225.0 which allows for close to 256 unique hosts within a network. Larger networks would use the mask 225.225.0.0 which is class B. And the largest networks, class A would use the mask 225.0.0.0 .


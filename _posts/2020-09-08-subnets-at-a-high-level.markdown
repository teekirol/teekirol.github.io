A network can be divided into subnets, which may be isolated from each other. They also allow routers to route traffic more quickly.

# IPv4 addresses

IPv4 addresses contain be split into two parts: The first part defines the network and the second part defines the host/machine.

There are different classes of networks -- primarily A, B, and C but there are also D and E which are less common. 

The number of bits that define the network and the host within an IPv4 address differ depending on the network class. 

Class A networks allow for the most number of hosts, and IPv4 addresses in a Class A network use 24 bits to define the hosts. This means the number of hosts allowed is *around 2^24. Meanwhile, Class C networks allows for less hosts and only use 8 bits to define the host, which means the number of hosts allowed is *around 2^8. 

*I still don't completely understand the detail around why the maximum hosts is less than the largest number that can be represented by the number of available bits.
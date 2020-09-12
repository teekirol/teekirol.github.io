Routers direct data packets to their destinations, i.e. their hosts, as indicated by the IP address contained within. 

Subnet masks are used by routers to determine which subnetwork a packet should go to. This can be done by a human by converting both the subnet mask and the IP into binary, and doing a logical AND between the two.

If a network has not been "subnetted", i.e. it is just one network that has not been divided into smaller networks, the default subnet for the network would be one of the following:

Network Class | Default Subnet
--- | ---
A   | 255.0.0.0
B   | 255.255.0.0
C   | 255.255.255.0

If a person wanted to create subnets, i.e. the process of "subnetting", they would need to go through some steps to come up with a custom subnet mask. Instead of the using the default subnet mask, the router would use the custom subnet mask to determine the subnet of a data packet.

# Networking Fundamentals. Task 4.4

### Part 1

We take network from task 4.3, and add a router as per assignment:

![Network topology](./images/topology.png "Network")

Router0 is a gateway for 192.168.0.0/24, Router1 is a gateway to 192.168.1.0/24, and both routers have interconnected interfaces in 10.0.0.0/8 network.

Configuring RIP routing between networks for Router0 and Router1 respectively:

![R0](./images/router0.png "Router0")

![R1](./images/router1.png "Router1")

The devices from different networks can successfully communicate:

![ICMP](./images/success.png "ICMP")

The respective Packet Tracer file is 4.4.1.pkt

### Part 2

Building the network, including 2 subnets, and 2 DNS zones: 192.168.0.0/24 for epam1.com, and 192.168.1.0/24 for epam2.com.
Two DNS servers serve the respective zones, and the router *gw* provides the L3 cummunication between networks.

![Network topology](./images/dns_network.png "Network")

Adding A and NS records to DNS servers, so we can communicate with PCs by their FQDN:

epam1.com DNS server:

![DNS1](./images/epam1.png "Zone 1")

epam2.com DNS server:

![DNS2](./images/epam2.png "Zone 2")

The PCs can communicate with the hosts in their zone by querying DNS server for A records stored directly on the server, and with hosts from other zone by querying DNS server for A records stored on another server, that can be queried due to the respective NS record.

Using pc1.epam1.com to reach hosts that belong to epam1.com and epam2.com:

![ICMP2](./images/success2.png "Success"

As we can see, the host can reach the hosts in both zones by their FQDN.

The respective Packet Tracer file is 4.4.2.pkt


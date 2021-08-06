# Networking fundamentals

### Building a small hub network

Built a hub-based network, assigned IP addresses (192.168.0.1-4 MASK 255.255.255.0) to PCs:

![Hub](./images/hub_network.png "Hub network")

Checked the connection using ICMP:

![ICMP](./images/icmp_ping.png "Connection check")

To send IP packet from PC0 to PC3, ARP protocol is used to discover target MAC address:

![ARP](./images/pc_arp.png "ARP discovery")

After the source device knows target device's link layer address, ICMP echo request is sent:

![Echo request](./images/pc_icmp.png "ICMP ping")

The target device repiles with ICMP echo reply. While the devices that process IP packets de-encapsulate them up to L3 (no higher layers are involved in this task), hub simply retransmits an electric signal, so no layers higher than L1 are shown in CPT:

![L1](./images/hub.png "L1")

After deleting IP addresses, PDU fails since ICMP needs L3 to function.

Added more devices as per assignment:

![Hub network](./images/hub_network_2.png "Hub network")

The connection functions in a similar fashion:

![ICMP ping](./images/net2.png "Hub network")

### Switch network

Built a switch-based network, used ICMP to verify connection. The switch works differently, storing the relation between MAC addresses and ports, sending frames only to target port after the discovery:

![ICMP ping](./images/switch.png "Switch network")

Added an additional switch and more PCs. The ICMP works in the same fashion, using the transit switch to commute with PCs attached to a different switch:

![Two switch network](./images/2sw.png "Two switch network")

Added a router, making 2 separate subnets:

![ICMP ping](./images/network.png "Router connecting two switch networks")

The router here connects networks 192.168.0.0/24 and 192.168.1.0/24. A PC0, for instance, having an ICPM packet with destiantion 192.168.1.3, sends the packet to the default gateway defined (192.168.0.200), since the adddress 192.168.1.3 is outside the PC0's broadcast domain. The router, having a route to 192.168.1.0/24, forwards the packet, and then forwards back an ICMP echo reply, thus allowing PCs from different subnets exchange packets.

![2 networks](./images/2sw1r.png "Packet exchange between two switch networks")







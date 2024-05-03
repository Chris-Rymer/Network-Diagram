# Home Network Diagram
My current home network setup represents my most ambitious networking project to date. I've virtualized everything from my home router to gaming on the couch using one main home server. Repurposing an old gaming PC into a home server running Proxmox was the cornerstone. With a dual network adapter NIC, Pfsense was seamlessly integrated, utilizing PCI pass-through for the network firewall, default gateway, and secure VPN connection to my home network from the outside.

From Pfsense, traffic flows out of the server, through a switch, and back into the server to connect various VMs and container services. A dedicated graphics card powers a Windows VM, utilizing PCIe pass-through and outputting to my living room TV for gaming.

The wireless network consists of a mesh network with three access points, ensuring seamless coverage throughout the house. Additionally, I've implemented two VLANs to provide separation between trusted and less-than-trusted wireless devices, enhancing security.

To bolster security further, all DNS traffic is routed through a DNS sinkhole (Pi-hole), blocking suspected malicious URLs and preventing tracking services.

This project has not only been enjoyable but also immensely educational. Overcoming numerous challenges along the way, it has significantly expanded my skills and understanding of networking. Future plans include incorporating Snort as a network intrusion detection and prevention system, further enhancing the security posture of my home network. 

## Diagram:
<img src="https://i.imgur.com/uiaY9uY.png" height="80%" width="80%" alt="Home Network Diagram"/>

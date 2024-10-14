## 1. What is MPLS?
Multiprotocol Label Switching (MPLS) is a routing technique in telecommunications networks. It is a data forwarding technology that increases the flow and speed of the network traffic. It provides a way to process packets based on their labels. 

It uses labels instead of routing table lookups to allow high-end network communications from one network node to the other. MPLS uses the LFIB/forwarding table to transfer labels from one node to the other. 

2. What are the benefits of using MPLS?
   
The benefits of using MPLS are as follows:

Multiple degrees of QoS:  Multiple degrees of QoS is supported. They check latency, jitter, and packet loss for various types of traffic such as voice, video, email, and bulk file transfers, etc.
Label-based switching:  Convergence is fast due to label-based switching. It cuts the need for routing tables.
IP VPNs:  IP VPNs are expandable.
MPLS TE:  Network congestion is minimum by using MPLS TE.
Reliable:  MPLS is reliable, safe, and trustworthy.

3. What are the MPLS router types?
   
The following are the MPLS router types:

C – Customer Router
CE – Customer Edge Router
PR – Provider Router
PE – Provider Edge Router

4. What is the difference between a P and a PE router?
5. 
P router does not contain customer network routes. These routes are, however, available on the PE router. Also, P routers do not need MP-iBGP. For PE routers, MP-iBGP is a must.

6. Name the types of labels.
   
The types of labels are:

Explicit Null
Implicit Null
Aggregate Label

6. What are the types of MPLS available?
   
There are three types of MPLS available:

Layer 2 point to point
Layer 3 IP VPN
Layer 2 VPLS
a. MPLS Layer 2 Point to Point:
The layer 2 point to point MPLS is the best suited for companies that need high bandwidth between a small number of sites.
It is economical.
It is an excellent alternative to high bandwidth leased lines.
Many network operators depend on Layer 2 and Ethernet for their core network infrastructure.
This protocol allows anything running over the LAN to be sent to the WAN without the need for routers to convert packets to Layer 3 (Network Layer).
b. MPLS Layer 3 IP/VPN:
The Layer 3 IP/VPN is best suited for large multi-site enterprises such as retail chains.
They deploy a large number of low bandwidth sites or large corporates
It is the best fit for companies that are:
In the process of merging: IP/VPNs are scalable for fast deployment.
Need ‘any to any’ connectivity: a shorter hop count between two local sites is more efficient than -’tromboning’ back into a central point. It is best suited for global networks where latency is increased.
Preparing for voice and data convergence: to implement a blanket ‘class of service’. It is made simple across multi-site networks.
Migrating from traditional ATM to IP: ATM has very high maintenance charges.
Low bandwidth needs at small branch offices.
Need of only a secure dial-up capability in smaller locations
c. Layer 2 Virtual Private LAN Services (VPLS):
The VPLS services are popular for delivering Ethernet services.
They combine both MPLS and Ethernet for customer and carrier benefits.
IP backbones have been used to provide Internet access as well as IP VPN access.
VPLS is also known as transparent Ethernet services.
It works over MPLS and gives benefits of two network types:
Ability to operate a multipoint network
Pass all traffic at Layer 2 over the WAN
VPLS is popular among TV broadcasters, the financial sector and media houses.


7. What is the difference between VPN and MPLS?
   
VPN:

VPN is referred to as Virtual Private Network. 
It could be configured using GRE tunnels. 
If you want a full mesh then the administrator needs to set u n*n-1 tunnels.
MPLS:

In the case of MPLS VPN, CPE works in the full mesh by default.
It works in full mesh form because of the route-target.

8. Can you make your PE router a P?
   
You need to remove the Border Gateway Protocol (BGP) configurations to make your PE a P. After you do that, it will not participate with the customer network.

9. If your LDP router ID, OSPF router ID and BGO router ID are different, will it work to forward the traffic of customers or not?
    
The BGP router ID and the LDP router ID should be the same if SP is using labels only for loopbacks. If labels are generated for each and every route then there is no problem at all.

10. What protocol is used by MPLS?
    
MPLS uses the Tag Distribution Protocol (TDP) or Label Distribution Protocol (LDP) protocols. 

Tag Distribution Protocol (TDP):

Tag Distribution Protocol (TDP) is a two-party protocol. It runs over a connection-oriented transport layer with guaranteed sequential delivery. 

Label Distribution Protocol (LDP):

Label Distribution Protocol (LDP) is a protocol used to establish MPLS transport LSPs when there is no need for traffic engineering. It establishes LSPs that follow the existing IP routing table. It is best suited for establishing a full mesh of LSPs between all of the routers on the network. 

11. What is penultimate hop popping?
    
Penultimate hop popping is a method of reducing label lookups on the egress router. It is done by the one-hop before the egress router.

12. What are the functions done by MPLS?
    
The following are the functions done by MPLS:

PUSH (Adding the Label)
POP (Removing the Label)
SWAP (Changing the Label)

13. What is downstream on demand?
    
The downstream router is responsible to advertise the label first to the upstream router when the downstream on-demand method is selected. 

The upstream router is the router that advertises the labels to its downstream router after receiving label bindings from it.

14. What is the difference between VPNv4 and IPv4 address families?
    
We use the IPv4 address family to always accept and forward IP packets to customers. 

When the customers’ packets are being received by PE, they become labeled and forward packets to different PE/RR. For this, an address family VPNv4 is needed.

In other words, we can say that IPv4 address-family is being used for customers. VPNv4 address-family is used by SP core.

15. What is SYSVOL?
    
The SysVOL folder has the server’s copy of the domain’s public files. The contents such as users, group policy, etc. of the SysVOL folders are replicated to all domain controllers in the domain. 

17. MPLS works on which layer?
    
It works between layer 2 and layer 3.

18. What is the difference between RD and RT?
    
RT is an extended community. RD is not an extended community.

19. How to filter MPLS labels?
    
MPLS filters can be labeled by using ACLs.

20. Two routers are having 4 equal-cost links, how many LDP sessions will be established?
    
Only one session will be established between the two routers having 4 equal-cost links.

# CCNA-LABS
My CCNA networking labs and troubleshooting practice
Built and configured a 3-router static routing topology in Cisco Packet Tracer to achieve end-to-end connectivity between two LANs across multiple networks. 

 What I configured 

 -IP addressing on PCs and router interfaces 

 -Default gateways on end devices 

 -Static routes on all routers 

 -End-to-end ICMP testing using ping 

-Troubleshooting connectivity issues using ARP and routing verification 

  

Issue encountered 

Initial ping attempts failed even though the routing configuration was correct. After troubleshooting in simulation mode, the issue was identified as incomplete ARP table population across the routers. 

Root cause 

When the first ICMP packet was sent: 

 -Devices did not yet know the destination MAC addresses 

 -Routers had to perform ARP requests before forwarding traffic 

 -Some ICMP packets were dropped while ARP resolution completed hop-by-hop 

 As a result: 

 -First few pings failed 

 -Final ping succeeded once all ARP tables were populated 

-Subsequent pings completed successfully with full connectivity 

 Key concepts reinforced 

 -Static routing configuration 

 -ARP resolution process 

 -ICMP packet flow 

-Router forwarding behaviour 

 -Troubleshooting Layer 2 vs Layer 3 connectivity 

 -Using Packet Tracer simulation mode for packet analysis 

  Outcome 

Successfully established full connectivity across all networks and gained a deeper understanding of how ARP impacts initial packet delivery in routed environments. 
## Verification Commands Used

- show ip interface brief
- show ip route
- ping
- tracert

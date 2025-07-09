- **Bridge Basics:**
    
    - A bridge is a network device that operates at the data link layer (Layer 2) of the OSI model.
    - It connects and segments LANs into smaller collision domains, improving overall network performance.
    ![Pasted image 20230812170725](../Images/Pasted%20image%2020230812170725.png)
- **Functionality:**
    
    - **Segmentation:** Bridges divide a network into smaller segments, reducing collision domains and improving network efficiency.
    - **Filtering:** Bridges analyze MAC addresses in data frames to determine whether to forward or filter the frames.
    - **Collision Domain Isolation:** Bridges isolate collision domains, preventing collisions from propagating across the entire network.
- **Types of Bridges:**
    
    - **Local Bridge:** Connects two or more segments of the same LAN.
    - **Remote Bridge:** Connects segments in different physical locations, often using WAN links.
- **Advantages:**
    
    - **Improved Performance:** Bridges reduce collisions and improve bandwidth utilization.
    - **Segmentation:** Bridges can help isolate network issues to specific segments, easing troubleshooting.
    - **Legacy Support:** Bridges can connect different LAN technologies and speeds.
- **Limitations:**
    
    - **Broadcast Traffic:** Bridges still forward broadcast traffic, which can lead to unnecessary traffic on interconnected segments.
    - **Limited Scalability:** In large networks, the number of bridges and their configuration can become complex.
- **Usage Scenarios:**
    
    - Bridges were more common in the past when Ethernet networks were simpler.
    - They were used to expand network coverage and alleviate collision-related performance issues.
- **Transition to Switches:**
    
    - Bridges paved the way for switches, which offer more advanced and efficient data forwarding based on MAC addresses.
    - Switches provide more granular control over traffic and are better suited for modern network demands.
- **Legacy Considerations:**
    
    - While switches are now the standard for LANs, bridges might still be encountered in older network setups.
- **Spanning Tree Protocol (STP):**
    
    - STP is a protocol used with bridges (and switches) to prevent loops in redundant network topologies.
    - It selectively disables redundant links to avoid broadcast storms and loops.

In summary, bridges are network devices operating at the data link layer that segment LANs to improve network efficiency and performance. They analyze MAC addresses to make forwarding decisions, and while they were widely used in the past, they have largely been replaced by more advanced devices like switches that offer better control over data forwarding and network management.
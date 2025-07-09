[[Open Systems Interconnection (OSI)]]

**7 Layers of OSI for Network Security**

1. **Physical Layer (Layer 1)**: Focuses on the physical medium that connects computers, like wiring. Vulnerabilities like wiretapping are a concern due to electronic eavesdropping capabilities on certain cables. The best defense is physical security measures, like locks.
    
2. **Data Link Layer (Layer 2)**: Deals with logical connections and how computers share access to a network medium, such as Ethernet or Wi-Fi. Layer 2 attacks include radio jamming, wireless deauthentication, ARP poisoning, and VLAN hopping. Using protective measures like WPA3 wireless security and strict VLAN configuration can help deter such attacks.
    
3. **Network Layer (Layer 3)**: Facilitates data exchange across different networks using IP and ICMP protocols. Attacks here include ping flood DoS attacks and spoofing attacks. Defense measures include packet-filtering firewalls and intrusion prevention systems (IPS).
    
4. **Transport Layer (Layer 4)**: Features protocols like TCP and UDP. This layer refines addressing further using port numbers, establishing either connection-based or connectionless sessions. Port scanning attacks target this layer, which can be defended against using packet-filtering firewalls. Security through obscurity, like port redirection, isn’t reliable.
    
5. **Session Layer (Layer 5)**: Helps differentiate between multiple connections within a service on a single host. Remote procedure call (RPC) is a typical protocol in this layer. Regular OS and application updates can prevent most attacks targeting this layer.
    
6. **Presentation Layer (Layer 6)**: Acts as a bridge between applications, allowing data encoding and encryption. While this layer deals with data encryption using TLS, it's also prone to man-in-the-middle attacks. Measures to counter these threats include IPS and user training regarding fake security certificates.
    
7. **Application Layer (Layer 7)**: Defines user interaction with application services, such as HTTP. This layer is prone to numerous attacks due to the vast number of applications. Crucial defenses include API authentication, vulnerability scanning, and reverse proxy systems to scan incoming packets.
    

In summary, each OSI layer has specific threats, and understanding these threats can guide the implementation of appropriate security measures.
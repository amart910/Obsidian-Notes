![Pasted image 20230819115442](../Images/Pasted%20image%2020230819115442.png)**Intrusion Detection and Prevention Systems (IDS/IPS): Overview**

- Both IDS and IPS are advanced security solutions that detect malicious traffic based on known behaviors and payload signatures.
- **IDS** monitors the network for threats, while **IPS** intercepts and blocks threats.

**Operating Modes:**

1. **Tap Mode:**
    
    - Both IDS and IPS can operate in tap mode.
    - This mode involves attaching to the network merely as listening devices.
    - Named after wiretapping, because they eavesdrop on traffic flow.
    - Ideal for IDS as they are passive listeners. They alert administrators upon detecting suspicious behavior.
    - However, tap mode is not as effective for IPS systems because they need to intercept and block traffic.
2. **In-line Mode:**
    
    - Used for IPS devices to stop traffic.
    - Positioned in the middle of the traffic stream.
    - IPS devices have multiple network ports, meant for input/output pairs. This allows administrators to route cables through the IPS, creating choke points in the network.
    - IPS bridges traffic and appears invisible yet inspects every packet, moving it from one cable to another.

**Anomaly Detection and Actions:**

- IPS devices can detect anomalies like unknown packet types or unusual traffic patterns.
- Actions upon detection:
    1. Alert the administrator.
    2. Block the traffic immediately.
    3. Automatically block malicious traffic.
    4. Reputation-based protection: Block files known to carry viruses/malware, e.g., blocking EXE attachments/downloads.

**Physical vs. Virtual Appliances:**

- Not always physical devices.
- Can be virtual appliances.
- Available as host-based IPS/IDS applications installed on servers or workstations.

**Use Cases and Examples:**

- For instance, when securing a network of public web servers, an IPS can be positioned between the network switch and the firewall. This positioning ensures the IPS scans all traffic entering and leaving that network. If there’s suspicious or malicious activity, the IPS can act accordingly.

In essence, IDSs and IPSs serve as vital tools in network security, with each offering distinct methods for monitoring and managing potential threats. Whether physical or virtual, they play a key role in ensuring the protection of digital assets.
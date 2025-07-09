**Ping:**

- **Use:** It tests network connectivity between devices using ICMP.
- **Operating Systems:** Windows, macOS, Linux.
- **Example:** `ping google.com`
- **Process:** The command sends multiple ICMP echo requests to the target and awaits its echo replies. By doing this, it helps ascertain the connectivity and latency between the two devices.

---

**Ipconfig:**

- **Use:** Displays the current TCP/IP configuration of the machine.
- **Operating Systems:** Windows.
- **Example:** `ipconfig /all`
- **Process:** This command fetches and displays all current TCP/IP network configuration values, including IP addresses, subnet masks, and default gateways.

---

**Ifconfig:**

- **Use:** Interface configurator; used for displaying and setting up network interface parameters.
- **Operating Systems:** Linux, Unix, macOS (but deprecated in favor of `ip` command).
- **Example:** `ifconfig eth0`
- **Process:** Shows the configuration of the `eth0` network interface, including IP address, broadcast address, and other related details.

---

**Traceroute/Tracert:**

- **Use:** Determines and displays the path a packet takes through the network.
- **Operating Systems:** `traceroute` for Linux/macOS and `tracert` for Windows.
- **Example:** `tracert google.com`
- **Process:** It sends packets with incrementing TTL values and listens for ICMP timeout replies, effectively mapping out the network hops between the source and destination.

---

**Tracepath:**

- **Use:** Similar to traceroute but doesn't require root privileges and can detect the MTU along the path.
- **Operating Systems:** Linux.
- **Example:** `tracepath google.com`
- **Process:** Determines the network path and MTU to the destination without requiring special permissions.

---

**ARP:**

- **Use:** Displays and modifies the ARP cache, which maps IP addresses to MAC addresses.
- **Operating Systems:** Windows, Linux, macOS.
- **Example:** `arp -a`
- **Process:** Lists the current ARP table entries, showing IP to MAC mappings on the local network.

---

**Netstat:**

- **Use:** Displays active network connections and listening ports.
- **Operating Systems:** Windows, Linux, macOS.
- **Example:** `netstat -an`
- **Process:** Shows all active network connections and listening ports in numerical format.

---

**Nslookup:**

- **Use:** Queries DNS servers for domain name or IP address mapping.
- **Operating Systems:** Windows, Linux, macOS.
- **Example:** `nslookup openai.com`
- **Process:** Sends a DNS query to the default or specified DNS server and returns the IP address associated with `openai.com`.

---

**Dig:**

- **Use:** Another tool for querying DNS information, providing more detailed data than nslookup.
- **Operating Systems:** Linux, macOS.
- **Example:** `dig openai.com`
- **Process:** Fetches and displays detailed DNS information about the domain `openai.com`.

---

**Whois:**

- **Use:** Queries domain registration and availability information.
- **Operating Systems:** Windows (with software), Linux, macOS.
- **Example:** `whois openai.com`
- **Process:** Retrieves and displays domain registration details, including ownership, creation date, and expiration.

---

**Route:**

- **Use:** Displays and modifies IP routing tables.
- **Operating Systems:** Windows (as `route`), Linux (as `route`, but deprecated in favor of `ip route`).
- **Example:** `route print`
- **Process:** Displays the IP routing table of the machine, showing how packets get directed based on their destination.

---

**SCP:**

- **Use:** Secure copy protocol; transfers files securely over SSH.
- **Operating Systems:** Linux, macOS.
- **Example:** `scp file.txt user@remote:/path/`
- **Process:** Copies `file.txt` securely to the specified path on a remote machine using SSH for the transfer.

---

**FTP:**

- **Use:** File Transfer Protocol; used for transferring files between machines over a network.
- **Operating Systems:** Windows, Linux, macOS.
- **Example:** `ftp openai.com`
- **Process:** Initiates an FTP session with the specified server (in this case, `openai.com`).

---

**TFTP:**

- **Use:** Trivial File Transfer Protocol; a simpler version of FTP with no authentication.
- **Operating Systems:** Windows, Linux, macOS.
- **Example:** `tftp -i openai.com get sample.txt`
- **Process:** Fetches the file `sample.txt` from the server without authentication.

---

**Finger:**

- **Use:** Retrieves information about a user on a network system.
- **Operating Systems:** Linux, macOS, Windows (with software).
- **Example:** `finger user@openai.com`
- **Process:** Fetches and displays details about the user `user` on the domain `openai.com`.

---

**Nmap:**

- **Use:** Network mapper; scans networks for device discovery and security auditing.
- **Operating Systems:** Windows, Linux, macOS.
- **Example:** `nmap -sP 192.168.1.0/24`
- **Process:** Performs a ping scan on the specified IP range to discover live hosts.

---

**Tcpdump:**

- **Use:** Packet analyzer; captures and analyzes network traffic.
- **Operating Systems:** Linux, macOS.
- **Example:** `tcpdump -i eth0`
- **Process:** Captures packets flowing through the `eth0` interface, allowing analysis of live network data.

---

**Telnet/SSH:**

- **Use:** Remote connection tools; Telnet is plaintext, while SSH is secure.
- **Operating Systems:** Windows, Linux, macOS.
- **Example:** `ssh user@openai.com`
- **Process:** Initiates a secure shell (SSH) connection to the `openai.com` domain with the specified username, providing encrypted remote access.
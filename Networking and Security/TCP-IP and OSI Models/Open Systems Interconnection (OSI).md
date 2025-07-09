The OSI (Open Systems Interconnection) model is a conceptual framework used to standardize and understand the various functions and layers involved in networking and communication protocols. The model is divided into seven distinct layers, each responsible for specific tasks and interactions. Here's an overview of each layer along with examples to help illustrate their functions:

1. **Physical Layer**:
	- The Physical Layer deals with the physical medium over which data is transmitted, such as cables, switches, and connectors. It's concerned with the actual transmission and reception of raw binary data.
	- Layer is implemented through the use of devices such as: hubs, repeaters, modem devices, and physical cabling

	- Example: Ethernet cables, fiber-optic cables, wireless signals.

2. **Data Link Layer:
	- The Data Link Layer provides error detection and correction and organizes raw bits into frames. It also manages access to the physical medium to avoid collisions.

	- Example: Ethernet frames, MAC addresses, switches, bridge devices, anything with a wired or wireless network interface cards (NIC).

3. **Network Layer:
	- The Network Layer is responsible for routing data packets from the source to the destination across different networks. It deals with logical addressing and routing decisions.

	- Example: IP packets, IP addresses, routers.

4. **Transport Layer:
	- The Transport Layer ensures end-to-end communication, reliability, and error recovery. It breaks down larger messages into segments and reassembles them on the receiving end. Layer often called the heart of OSI.

	- Example: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).

5. **Session Layer:
	- The Session Layer establishes, manages, and terminates communication sessions between two devices. It handles session synchronization and checkpointing.

	- Example: Remote desktop sessions, file transfer sessions.

6. **Presentation Layer:
	- The Presentation Layer is responsible for data translation, encryption, and compression. It ensures that data is presented in a readable format for the application layer.

	- Example: Data encryption, data compression, character encoding.

7. **Application Layer:
	- The Application Layer provides user interfaces and network services directly to end-users. It includes various application protocols that enable communication and data exchange between software applications.

	- Example: HTTP (Hypertext Transfer Protocol), FTP (File Transfer Protocol), SMTP (Simple Mail Transfer Protocol).

Now, let's use a common example to illustrate how the OSI model works:

Imagine you're sending an email (using SMTP) with an attachment (using FTP) over the internet:

1) Application Layer (Layer 7): Your email client (e.g., Outlook) initiates an SMTP session to send the email.

2) Presentation Layer (Layer 6): The presentation layer might encode your email data and attachment in a format suitable for transmission.

3) Session Layer (Layer 5): A session is established between your email client and the email server to ensure proper communication.

4) Transport Layer (Layer 4): The transport layer segments your email and attachment into smaller packets. TCP ensures reliable delivery, so if a packet is lost, it's retransmitted.

5) Network Layer (Layer 3): IP routing comes into play as the packets are routed through various routers across the internet to reach the recipient's email server.

6) Data Link Layer (Layer 2): The data link layer encapsulates the packets into frames, adding source and destination MAC addresses.

7) Physical Layer (Layer 1): The frames are transmitted over physical media such as cables or wireless signals.

The recipient's email server receives and processes the data in the reverse order until the email is presented to the recipient in their email client.

![[OSI MODEL.png]]
![[OSI MODEL Example.png]]
![TCP-IP and OSI models](TCP-IP%20and%20OSI%20models.jpg)

[Open Systems Interconnection (OSI)](Open%20Systems%20Interconnection%20(OSI).md) Model

The OSI model is a conceptual framework that standardizes the functions of a communication system or network into seven distinct layers. Each layer is responsible for specific tasks related to data communication, and they build upon each other to facilitate end-to-end communication.

1. **Physical Layer:** Deals with physical connections, cabling, and signaling methods for transmitting raw binary data over a physical medium.
    
2. **Data Link Layer:** Ensures reliable point-to-point communication between neighboring devices, framing data and managing errors.
    
3. **Network Layer:** Manages logical addressing, routing, and path determination for data packets across multiple networks.
    
4. **Transport Layer:** Provides end-to-end communication and ensures data reliability through flow control, error detection, and retransmission.
    
5. **Session Layer:** Establishes, manages, and terminates communication sessions between devices.
    
6. **Presentation Layer:** Focuses on data format translation, encryption, compression, and other transformations for data exchange between different systems.
    
7. **Application Layer:** Provides application services directly to users and supports network services such as email, file transfer, and remote access.
    

**[TCP-IP](TCP-IP.md) Model (Transmission Control Protocol/Internet Protocol):**

The TCP/IP model is a practical, four-layer framework that serves as the basis for the internet and most modern networking protocols. While it's often compared to the OSI model, the TCP/IP model is more closely aligned with real-world networking implementations.

1. **Link Layer (Network Interface Layer):** Concerned with data link and physical network aspects, including addressing, framing, and media access control.
    
2. **Internet Layer:** Corresponds to the OSI Network Layer. It handles IP addressing, routing, and packet forwarding.
    
3. **Transport Layer:** Manages end-to-end communication, offering reliability and data flow control. It includes protocols like TCP and UDP.
    
4. **Application Layer:** Combines aspects of the OSI Session, Presentation, and Application layers. It provides application-specific protocols for services such as HTTP, FTP, and SMTP.
    

In summary, the OSI model is a theoretical framework with seven layers that standardizes communication functions, while the TCP/IP model is a practical networking model with four layers, closely aligned with the protocols that power the internet and modern networks.
# Outline
- Web Security Threats
- Transport Layer Security (TLS)
- Secure Socket Layer (SSL)
- HTTP Over SSL (HTTPS)
- Secure Shell (SSH)
- Virtual Private Channel (VPN)
<hr>

# Transport Layer Security (TLS)
The **transport layer** is one of the layers in the OSI Model, which is a conceptual framework that standardizes the functions of a telecommunications system into seven abstraction layers. The **transport layer** in particular focuses on ensuring that data is delivered error-free, in the correct order, and with proper flow control between the sender and the receiver. Simply put, the **transport layer** manages the transfer of data between one computational device and another computational device over the Internet. 

If we refer to the CIA triad, the **confidentiality**, **integrity**, **availability**,  and **authentication** of our data is of upmost importance when it comes to network security. Data must be transported from one device to another, and the transport of that data must adhere to the CIA triad to ensure strong network security.

## TLS Architecture
Two important concepts for TLS are the **TLS connection** and the **TLS session**. 

The **TLS connection** is the secure communication link established between a client and a server using the TLS protocol. It represents the entire process of setting up the connection between the client and the server. The **TLS connection** encompasses a handshake phase where the client and server exchange cryptographic parameters, authenticate each other, and establish the encryption algorithms and keys that are to be used.
- These connections are peer-to-peer relationships.
- These connections are transient.
- Every connection is associated with one **session**.

The **TLS session** is more specific, referring to the ongoing securing that takes place within the **TLS connection**. Once a TLS connection is established, then it can facilitate multiple secure interactions between the client and the server without repeating the full handshake process that occurs when the TLS connection is established. 
- These sessions are the association between the client and the server.
- The **TLS session** is created by the handshake protocol of the **TLS connection**.
- The **TLS session** defines a set of cryptographic security parameters which can be shared among multiple connections.
- The **TLS session** is used to avoid the expensive negotiation of new security parameters for each connection.
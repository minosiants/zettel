# 📘 QUIC Protocol Glossary  

## A
- **ACK (Acknowledgment Frame)**  
  A QUIC frame type used to signal receipt of packets. Unlike TCP cumulative ACKs, QUIC ACKs can acknowledge ranges of packets and support more efficient loss detection.  

- **AEAD (Authenticated Encryption with Associated Data)**  
  Encryption mode (e.g., AES-GCM, ChaCha20-Poly1305) that QUIC uses to provide confidentiality, integrity, and authentication of both payload and headers.  

---

## C
- **CID (Connection ID)**  
  An identifier chosen by each endpoint to allow packets to be routed correctly, even if the underlying IP address or port changes (e.g., during NAT rebinding or mobility).  

- **CRYPTO Frame**  
  Frame type used to carry TLS handshake messages inside QUIC packets.  

- **Congestion Control**  
  QUIC implements congestion control (typically CUBIC, BBR, or Reno), similar in spirit to TCP, to avoid network overload.  

---

## E
- **ECN (Explicit Congestion Notification)**  
  An IP-layer mechanism QUIC can use to detect congestion without waiting for packet loss.  

- **Endpoint**  
  Either side of a QUIC connection (client or server).  

---

## F
- **Flow Control**  
  Mechanism to ensure a sender does not overwhelm a receiver with too much data at once. QUIC applies flow control at both the stream and connection levels.  

- **Frame**  
  The smallest unit of structured data in QUIC. Multiple frames can be packed into a single QUIC packet.  

---

## H
- **Handshake**  
  Initial process where client and server negotiate cryptographic keys and connection parameters, carried out using TLS 1.3 inside QUIC’s CRYPTO frames.  

- **Header Protection**  
  QUIC applies additional lightweight encryption to hide packet numbers and some header fields, making traffic analysis harder.  

---

## I
- **Idle Timeout**  
  Time period after which a connection is closed if no packets are exchanged.  

- **Initial Packet**  
  The first type of packet sent by the client to initiate a connection. It contains TLS handshake data inside CRYPTO frames.  

---

## K
- **Key Update**  
  Mechanism to periodically refresh encryption keys during a long-lived connection for improved security.  

- **Keep-Alive**  
  A packet sent to prevent idle timeout when no application data is transmitted.  

---

## L
- **Loss Detection**  
  Algorithm that determines when packets are lost and should be retransmitted, based on ACKs, timers, and packet numbers.  

---

## M
- **Migration**  
  QUIC supports client or server changing their IP address/port (e.g., switching from Wi-Fi to mobile) without breaking the connection, enabled by CIDs.  

---

## O
- **0-RTT (Zero Round Trip Time)**  
  Mechanism allowing a client to send early data before the handshake completes, using cached session keys from a previous connection. Faster but replayable.  

- **1-RTT (One Round Trip Time)**  
  Normal encrypted data transmission after the handshake completes.  

---

## P
- **Packet Number**  
  Monotonically increasing identifier assigned to each sent packet; unlike TCP sequence numbers, they don’t wrap around.  

- **Path**  
  The combination of IP address and port used by a QUIC connection. A single connection can migrate across paths.  

- **PN (Packet Number Space)**  
  QUIC maintains separate number spaces for Initial, Handshake, and 1-RTT packets, each protected by different keys.  

---

## Q
- **QUIC (Quick UDP Internet Connections)**  
  A transport protocol built on UDP, designed to reduce latency compared to TCP + TLS, with built-in encryption, multiplexing, and faster connection setup.  

---

## R
- **Retransmission**  
  QUIC does not retransmit packets directly; instead, lost data (frames) are retransmitted in new packets.  

- **Retry Packet**  
  A packet sent by a server to validate a client’s source address before proceeding with the handshake.  

---

## S
- **Spin Bit**  
  An optional bit in QUIC packets that can be used by network operators to measure round-trip time without decryption.  

- **Stream**  
  An independent, ordered sequence of bytes within a QUIC connection. Multiple streams can run concurrently without blocking each other (unlike TCP’s head-of-line blocking).  

- **Stream ID**  
  A unique identifier for a QUIC stream, encoding initiator (client/server) and type (unidirectional/bidirectional).  

---

## T
- **TLS 1.3**  
  The mandatory security layer inside QUIC, used for key exchange, authentication, and encryption setup.  

- **Token**  
  A value provided by a server (via Retry or NEW_TOKEN frames) to validate a client’s IP address and prevent amplification attacks.  

---

## V
- **Version Negotiation**  
  Process where client and server agree on which QUIC version to use, since QUIC is versioned for extensibility.  

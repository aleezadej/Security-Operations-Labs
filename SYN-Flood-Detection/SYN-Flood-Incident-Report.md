# Cybersecurity Incident Report: SYN Flood Attack

## Section 1: Identify the Type of Attack

A potential explanation for the timeout response is that a malicious actor is conducting a SYN flood attack. The log shows a high number of requests being made from the same source within milliseconds. The TCP protocol accounts for the majority of the log, further reinforcing the likelihood of a SYN flood attack, as the logs display issues with half-open connections.

## Section 2: How the Attack Causes the Website to Malfunction

When website visitors attempt to establish a connection with the web server, a three-way handshake occurs using the TCP protocol:

1. **SYN:** The visitor's device sends a request to the server to synchronize.
2. **SYN-ACK:** The server receives the request, sends a SYN-ACK back, and allocates resources to track the connection while awaiting the final ACK.
3. **ACK:** The visitor's device sends an acknowledgment (ACK) to confirm the connection.

### What Happens When a Malicious Actor Sends a Large Number of SYN Packets at Once

When a malicious actor sends a large number of SYN packets all at once, the three-way handshake is overwhelmed by the volume of requests. This is well-known as the TCP SYN Flood Attack. Since the connections are unable to be completed without the final ACK, the server accumulates a large number of half-open connections, resulting in the inability to process legitimate requests.

### What the Logs Indicate and How That Affects the Server

The logs indicate that SYN requests are continuously being sent from an unfamiliar IP address. The server responds with SYN-ACK but never receives the final ACK, leaving connections half-open. Eventually, the server sends RST-ACK packets, resetting these incomplete connections. As the backlog of half-open connections accumulates, the server becomes unable to process legitimate requests, causing the connection timeout error for real visitors.

# Cybersecurity Incident Report: Network Traffic Analysis

## Part 1: Summary of the Problem Found in the DNS and ICMP Traffic Log

The UDP protocol reveals that the UDP packet was undeliverable to port 53 of the DNS server. As part of the DNS protocol, the UDP protocol is used to contact the DNS server to retrieve the IP address. Port 53 indicates that there is an issue in translating the domain name into the machine-readable IP address necessary to access the website. The ICMP protocol is used to respond with an error message, and the ICMP error messages reinforce that the DNS server was unable to process requests, as indicated in the repeated ICMP error responses from the server.

## Part 2: Analysis of the Data and Cause of the Incident

The incident first occurred at 13:24:32.192571 (1:24 PM). The incident was reported to the IT team through several customers of the client, reporting the issue of not being able to access the client company website and instead being met with the error message "destination port unreachable." To investigate the incident, a network analyzer tool was used to attempt to load the page. The information gathered was then analyzed to discover the issue. Key findings in the investigation revealed that there was an issue with reaching port 53 — indicating an issue in translating the domain name into the machine-readable IP address. The likely cause of this issue is that the DNS service crashed, because "unreachable" in the error message indicates the request did not go through and no service was listening to receive. The issue is currently being investigated by the cybersecurity team. The team's next step in troubleshooting is finding out whether the DNS server is down or traffic is being blocked by the firewall.

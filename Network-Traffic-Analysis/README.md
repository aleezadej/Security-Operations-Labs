# DNS Connectivity Failure Analysis

## Overview
Investigated network traffic logs following reported website connectivity failures for yummyrecipesforme.com. Using a network analyzer tool (tcpdump), I identified undeliverable UDP requests to DNS port 53 and repeated ICMP "port unreachable" error responses, then traced the issue to a likely DNS service failure.

## Approach
1. Reviewed customer-reported symptoms and the "destination port unreachable" error message.
2. Analyzed tcpdump logs to identify the protocols involved and trace the UDP request/ICMP error pattern.
3. Interpreted log details (query ID, flags, port 53) to determine the root cause and documented findings in an incident report.

## Skills Demonstrated
- tcpdump log analysis
- DNS/UDP/ICMP protocol troubleshooting
- Root cause analysis
- Incident documentation

## Deliverable
[Network-Analysis-Incident-Report.md](./Network-Analysis-Incident-Report.md)

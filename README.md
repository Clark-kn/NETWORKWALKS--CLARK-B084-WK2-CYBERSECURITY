# NETWORKWALKS--CLARK-B084-WK2-CYBERSECURITY

## Overview
This repository documents my **Week 2 cybersecurity practical work** completed as part of the Networkwalks cybersecurity program. The work focused on two main areas:
1. **Footprinting** the authorized `networkwalks.com` domain.
2. **Scanning** my own private local network using Zenmap.

The purpose of this project was to practice information gathering, understand what technical details are visible from public services, identify live devices on a private network, and record results in a clear and responsible way.

---

## Objectives
* Collect publicly available information about the authorized domain.
* Identify web technologies, DNS records, HTTP headers, and WAF information.
* Discover live hosts on a private local network.
* Document observations, possible impact, and defensive recommendations.
* Perform all activities within an authorized educational scope.

---

## Tools Used
* Kali Linux
* WHOIS
* WhatWeb
* Nslookup
* Curl
* Wafw00f
* DNSRecon
* Zenmap / Nmap
* Windows `ipconfig`

---

## Activities Completed

### 1. Footprinting and Reconnaissance
I used **WHOIS**, **WhatWeb**, **Nslookup**, **Curl**, **Wafw00f**, and **DNSRecon** to review the public footprint of `networkwalks.com`. 

**Key observations included:**
* Domain registration details and name servers.
* The resolved web-service IP address.
* Visible web technologies and HTTP response headers.
* The WordPress REST API endpoint and WAF information.
* DNS service records.

### 2. Local Network Scanning
I used Windows network information and **Zenmap** to scan my private local network. 
* The **Ping Scan** identified one live host at `10.0.0.7`.
* The available scan evidence did not expose an additional MAC address, and no exploitation or vulnerability validation was performed.

---

## Key Observations
* Public-facing technology and version information can assist security review.
* DNS and HTTP metadata can reveal details about hosting and application structure.
* A local discovery scan can help identify unexpected or unauthorized devices.
* An observation (such as a software version, IP address, or DNS record) is not by itself proof of a vulnerability.
* Further testing must be authorized and carefully controlled.

---

## Privacy and Address Disclosure
* **Local IP:** The IP address used for the Zenmap scan (`10.0.0.7`) was a private local-network address, not my public Internet IP address. 
* **MAC Addresses:** Any MAC address referenced in the local scan was a private/local network identifier.
* **Public Infrastructure:** Public IP addresses shown in the footprinting evidence relate strictly to the authorized target domain’s infrastructure.

---

## Limitations
This project covered reconnaissance, footprinting, and basic host discovery only. It did not include exploitation, password attacks, vulnerability validation, or unauthorized access. Some evidence may be represented through screenshots or command output rather than a complete raw-data export.

---

## Ethical and Legal Notice
> All testing described in this repository was performed against systems within an authorized educational scope or on systems and networks that I own or control. Do not use these techniques against third-party systems without clear permission. This material is provided for learning, defensive security, and responsible documentation.

---
Author
Clark Nshuti
## Commands Practiced
```bash
whois networkwalks.com
whatweb networkwalks.com
nslookup networkwalks.com
curl -I [https://networkwalks.com](https://networkwalks.com)
wafw00f networkwalks.com
dnsrecon -d networkwalks.com
nmap -sn 10.0.0.7

# NEWORKWALKS-FOOTPRING-W2-B084

# 🔐 Penetration Testing Report: Footprinting & Network Scanning (Week 2)

**Program:** Cybersecurity & Ethical Hacking Internship, Networkwalks
**Batch:** B084
**Report ID:** W2-PM-FINAL
**Author:** Kwanele
**Date:** 13 November 2026

---

## 📌 Overview

This repository contains my Week 2 penetration testing report and the evidence that supports it. The work covers the first two phases of a penetration test:

1. **Reconnaissance & Footprinting**: collecting public information about a target.
2. **Scanning & Network Discovery**: finding live hosts on a network and mapping them.

Together they show how an attacker moves from gathering public information to mapping a live network, and what a defender can do about it.

Phases 3 to 5 are still in progress and will be added in later weeks.

---

## ⚠️ Legal & Ethical Notice

All activities in this repository were performed **only** on:

- **Networkwalks** systems, with secured written permission from the client, and
- **My own local network**, which I own.

This material is for **education and research only**. Do not use anything here against systems you do not own or do not have written permission to test. Unauthorised access is a crime in most countries, even when nothing is damaged. You are fully responsible for your own actions.

---

## 🎯 Scope

| Item | Detail |
|---|---|
| Targets | 1. Networkwalks (written permission secured) 2. My own local LAN |
| Modules | W2-PM1 (Multiple Kali Tools), W2-PM2 (Footprinting with GHDB), W2-PM3 (Footprinting with Maltego), W2-PM5 (Zenmap Scanning) |
| Phases covered | Phase 1: Reconnaissance & Footprinting, Phase 2: Scanning & Network Discovery |
| Exploitation | **None.** No exploitation or vulnerability validation was performed |

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Kali Linux & Windows | Operating systems used for the activities |
| WHOIS | Domain registration details (owner, dates, name servers) |
| WhatWeb | Fingerprint web technologies (server, CMS, plugins) |
| Nslookup | Resolve the domain name to its IP address |
| curl -I | Read the HTTP response headers |
| Wafw00f | Detect whether a Web Application Firewall is present |
| DNSRecon | Enumerate DNS records (NS, MX, SPF, TXT, SRV) |
| Maltego | Map email addresses related to the target domain |
| Google Hacking Database (GHDB) | See what sensitive information is publicly indexed |
| Zenmap (Nmap GUI) | Discover live hosts, IP and MAC addresses on a local subnet |
| Windows CMD (`ipconfig`) | Identify the local IP address and subnet |

---

## 🔎 What I Did

### 1. Footprinting & Reconnaissance
- **WHOIS** to get public domain registration info and name servers.
- **WhatWeb** to identify the website's technologies (CMS and plugins).
- **Nslookup** to resolve the domain to its IP address.
- **curl -I** to inspect HTTP response headers and see what technical info they expose.
- **Wafw00f** to check whether a Web Application Firewall protects the site.
- **DNSRecon** to enumerate DNS records (name servers, mail servers, SPF/TXT and service records).
- **Maltego** installed and configured on Kali Linux to map email addresses related to the target domain.
- **GHDB** to see how exposed devices and downloadable documents show up in public search results. I only ran searches and looked at the listings. I did not access any device.

### 2. Network Scanning with Zenmap
- Used `ipconfig` to find my local IP address and subnet.
- Ran a **Ping Scan** in Zenmap to find live hosts.
- Recorded the IP and MAC addresses of the discovered hosts.
- Generated and saved the **network topology** as a PDF.

---

## 📊 Key Findings (Summary)

These are **observations, not confirmed vulnerabilities**. Seeing a software version, IP address or DNS record does not by itself mean a system is vulnerable. Further authorised testing would be needed to confirm that.

| # | Observation | Risk Level |
|---|---|---|
| 1 | Web technology (CMS and plugin) information was visible | Medium |
| 2 | The server IP address could be identified | Low |
| 3 | HTTP headers exposed technical information | Low |
| 4 | WAF technology could be identified | Low |
| 5 | DNS, mail and service records were publicly visible | Medium |
| 6 | Multiple live hosts were visible on the local network | Medium |

---

## ✅ Recommendations

- Review what technology information is publicly visible.
- Keep the CMS, plugins and other web technologies up to date.
- Review HTTP headers and remove unnecessary technical information.
- Review DNS records regularly.
- Keep the WAF enabled, tuned and monitored.
- Scan your own network regularly and investigate unknown devices.
- Keep network documentation and topology up to date.
- Only perform security testing with authorisation.

---

## 📁 Repository Contents

> Update the names below so they match the files in this repo.

```
├── W2-PM-FINAL_Sample_Report_v2.docx   # Full penetration testing report
├── screenshots/                        # Evidence screenshots for each tool
├── network-topology.pdf                # Zenmap topology (saved from Zenmap)
└── README.md
```

---

## 💡 What I Learned

- Public information adds up fast. Small details that look harmless on their own can give an attacker a clear picture of an organisation.
- A good report separates **what was observed** from **what is a confirmed vulnerability**, and rates risk honestly.
- Every test must stay inside an **authorised scope**, and permission always comes first.
- Findings must be documented clearly: what was done, what was found, what it means, the risk, and how to reduce it.

---

## 👤 Author

**Kwanele**
Cybersecurity & Ethical Hacking Intern, Networkwalks (Batch B084)

🔗 LinkedIn[:(https://lnkd.in/p/eYznfXvw)

---

## 🙏 Acknowledgements

Thanks to **Networkwalks** and my trainer for the hands-on program and guidance.

---

*Educational use only.

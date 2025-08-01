# dns-pcap-analysis
it's DNS-focused, a beginner-friendly pcap analysis


# DNS PCAP Analysis using Wireshark

This repository contains a basic triage-level analysis of a DNS packet capture (`dns.cap`) file using **Wireshark**. It demonstrates how to inspect DNS queries and responses, apply filters, identify anomalies, and document findings — a foundational skill in **SOC** and **Digital Forensics** workflows.

---

## 📁 Files Included

- `dns.cap` — Original DNS packet capture file
- `analysis/dns_analysis_notes.md` — Step-by-step analysis with findings
- `filters.txt` — Wireshark filters used during analysis

---

## 🔧 Tools Used

- [Wireshark](https://www.wireshark.org/) – for packet inspection
- Basic Linux commands (optional)
- Git & GitHub – version control and repo hosting

---

## 🧪 Analysis Performed

- Extracted and examined all DNS packets
- Differentiated DNS queries and responses
- Observed domain name queries and resolved IPs
- Checked for repeated queries and anomalous responses
- Identified potential triage flags (e.g., multiple responses to a single query)

---

## 🧠 Key Learnings

- How DNS queries and responses work
- How to use Wireshark filters for DNS analysis
- How to identify basic indicators of compromise (IOCs) in DNS traffic
- Importance of triage in SOC workflows

---

## 🔍 Wireshark Filters Used

| Purpose                  | Filter Syntax                    |
|--------------------------|----------------------------------|
| All DNS traffic          | dns                           |
| DNS Queries only         | dns.flags.response == 0        |
| DNS Responses only       | dns.flags.response == 1        |
| Specific domain lookup   | dns.qry.name contains "example|

---

## 📊 Summary (based on current PCAP)

- 📦 Total Packets: 38
- 🧾 Queries Observed: 12
- ✅ Responses Seen: 26
- 🔁 One query had 3 responses (potential retry or multiple servers)
- 💡 No critical malicious activity, but useful for learning packet-level DNS inspection

---

## 📌 Use Case

This repo can help:
- Students learning cybersecurity fundamentals
- Beginners practicing packet analysis
- SOC Level 1 aspirants trying triage basics
- Anyone exploring DNS packet behavior

---

## 📬 Contact

If you're also learning cyber forensics or SOC tools and want to collaborate or ask questions:
> 📧 Email: nitinnsharma48@gmail.com 
> 🐦 Twitter: https://x.com/cyberNSharma
> 🔗 LinkedIn: www.linkedin.com/in/cybernsharma

---

## ⭐ Give a Star!

If you found this project helpful, consider giving it a ⭐ to support more beginner-friendly cybersecurity repos.

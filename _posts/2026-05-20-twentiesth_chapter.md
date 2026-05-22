---
title: Phile 20. Infrastructure tracking
date: 2026-05-20 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

Collecting indicators is a crucial part of threat intelligence.It help organizations to make better decisions in daily security operations whether enriching SIEM alerts or investigating phishing emails. It is essential but in a mature cyber security strategy it is not enough on its own.
The real value comes from connecting the dots and understanding how adversaries build and operate their infrastructure.
Threat actors rarely use a single IP address or domain. They operate entire ecosystems involving hosting providers, phishing domains, VPS servers, redirectors, malware delivery infrastructure, and command-and-control systems. Mapping these connections is one of the most valuable capabilities in modern cyber threat intelligence.

In the next chapters, we will move beyond simple indicators and take a closer look at how analysts track and investigate adversary infrastructure in the wild.

## Phile 20. Infrastructure tracking

When an analyst discovers a suspicious IP address or domain name during an investigation, the first obvious step is searching in WHOIS databases, reviewing Passive DNS records or using plaforms like Virustotal. It is a good starting point but the problem is these methods often lead to dead ends. 
So what comes next? Stop the investigation? Absolutely not. 
There are numerous advanced techniques that help uncover hidden infrastructure and connect the dots.
Ultimately, the analyst’s goal is to identify patterns and reveal the threat actor behind the operation.

### Passive DNS

Adversary infrastructure is rarely static. Threat actors constantly rotate domains, IP addresses and hosting providers.
These changes leave behind historical records that can be leveraged by defenders. It enables to uncover operational patterns and infrastructure relationships.

Passive DNS is the collection and storage of DNS resolution data over time. Unlike active DNS queries, which return the current resolution for a domain, passive DNS can answer questions such as:
- Which IP addresses resolved to a specific domain over time?
- Which domains have pointed to a given IP address at different points in time?

Passive DNS supports two major investigation methods:
- **Forward resolution:** review the historical IPs associated with a domain.
- **Reverse resolution:** identifing other domains hosted on the same IP address.

Passive DNS provides several major advantages:
- **Broader the detection scope:** starting from a single IOC, defenders can identify related domains or IP clusters and expand visibility
- **Attribution Support:** infrastructure reuse can link new campaigns to previously observed activity by the same adversary.

---

### WHOIS

WHOIS databases are centralized directories that store registration data for internet resources including domain names, IP addresses, and autonomous systems.
Typical records may include:
- registrant’s name
- email address
- phone number
- creation/expiration dates
- nameserver information.

Much of this information is publicly accessible. However, privacy protection services frequently mask registrant details, and most professional threat actors stopped using real identifying information long ago.

Because of these limitations, WHOIS searches are useful for enrichment and pivoting, but they rarely tell the full story on their own.

---

### Final takeaway

Infrastructure tracking is where threat intelligence starts to move beyond isolated indicators and into real operational analysis. Instead of looking at single IP addresses or domains independently, analysts begin uncovering relationships, patterns, and infrastructure reuse across campaigns.

Techniques such as Passive DNS and WHOIS analysis provide valuable visibility into how adversaries operate and evolve over time. While individual indicators may disappear quickly, infrastructure patterns often leave traces behind that defenders can still follow.

In modern CTI, the goal is not simply collecting indicators — it is understanding the ecosystem behind them.

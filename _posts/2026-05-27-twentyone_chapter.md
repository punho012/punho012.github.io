---
title: Phile 21. Advanced infrastructure tracking
date: 2026-05-27 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

## Phile 21. Advanced infrastructure tracking

Today we take a closer look at infrastructire tracking and explore advanced techniques as a continuation of the previous episode.

The primary concept behind infrastructure tracking is identifying pivot points. Pivot points are artifacts or characteristics that can connect multiple infrastructure elements to a specific threat actor or campaign.  Threat actors often reuse certain parts of their infrastructure. The more overlapping patterns analysts discover, the higher the confidence that the infrastructure is tied to the same adversary.
In the previous chapter, we discussed Passive DNS and WHOIS databases.
DNS pivot is simple: analysts use DNS history and domain relationships to identify patterns and related infrastructure that threat actors reused during operations.

But what happens when these techniques lead to a dead end?

This is where more advanced infrastructure tracking methods become important.

---

### Autonomous System & Hosting patterns

Threat actors frequently reuse the same hosting providers, VPS services, or Autonomous Systems (ASNs) when deploying infrastructure.

Infrastructure deployed by the same actor often shares operational similarities:
- identical hosting regions
- recurring providers
- similar server deployment templates
- matching server configurations

These patterns can help analysts cluster infrastructure and identify previously unknown malicious assets.

However, analysts should also remain cautious. Many actors intentionally abuse large cloud providers or compromised infrastructure to blend into normal traffic and make attribution more difficult.

---

### Services

Threat actors sometimes expose services on uncommon ports in an attempt to evade basic scanning and detection.

Examples include:

- SSH running on high-numbered ports
- RDP exposed through unusual ports
- non-standard web service configurations

While unusual ports alone are weak indicators, repeated patterns across multiple systems may become valuable pivot points during investigations.

---

### Common x509 Certificates

TLS/SSL certificates can provide extremely valuable infrastructure correlations.

When looking at the certifate we are basically looking at a SHA-256 hash of the server's TLS/SSL certificate.  This hash acts like a unique fingerprint for that specific certificate.

Several certificate-related artifacts can be reused across infrastructure:
- certificate SHA-256 hashes
- subject fields
- issuer values
- common names
- certificate validity periods

Another useful technique is JARM fingerprinting. JA3 and JARM are TLS fingerprinting methods used to identify similarities in how systems handle SSL/TLS communication. While JA3 primarily fingerprints clients, JARM fingerprints servers.They are often used as pivot points. A JARM fingerprint acts like a behavioral signature for how a server negotiates TLS connections. Even when certificates change, similar server configurations may still generate matching JARM fingerprints.

This makes JARM extremely valuable for infrastructure tracking and threat hunting.

---

 ### SSH Configuration Commonalities

 It is common among threat actors they run protocols especially SSH on a higher port number. Commonalities between ssh host key and port numbers indicate that the hosts was provisioned by the same actor. SSH host key is the primary artifact.

---

 ### HTML patterns

Web content itself can become a powerful pivot point.

Useful artifacts include:

- default web banners
- HTML page titles
- favicon hashes
- HTTP response headers
- unique content returned in HTTP bodies

Favicon hashing has become a particularly popular technique in infrastructure tracking because many threat actors unintentionally reuse web templates across operations.

Individually, these artifacts may appear insignificant. Combined together, they can reveal large infrastructure clusters.

---

### Cross-correlation

The real strength of infrastructure tracking comes from combining multiple weak signals into stronger evidence.

A single reused certificate or unusual port is rarely enough for attribution. But when analysts correlate artifacts a much clearer operational picture begins to emerge.

Like every other area of CTI, infrastructure tracking should never rely on a single source or indicator. Strong intelligence comes from cross-correlation, validation, and context.

---

### Final takeaway

Advanced infrastructure tracking allows defenders to move beyond isolated indicators and start uncovering the operational habits of threat actors. Infrastructure reuse, deployment patterns, TLS fingerprints, and web artifacts can all reveal hidden relationships between campaigns and malicious systems.

Most individual indicators are weak on their own. The real value comes from correlating multiple small observations into a larger intelligence picture. This investigative mindset is one of the most important skills in operational cyber threat intelligence.

Modern adversaries constantly evolve and rotate infrastructure, but operational mistakes and reused patterns still leave traces behind. The analyst’s job is to find those traces and connect them before the next attack happens.
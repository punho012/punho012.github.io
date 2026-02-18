---
title: Phile 7. MITRE ATT&CK
date: 2026-02-18 +/-TTTT 
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

### Phile 7. MITRE ATT&CK framework

Everyone who works in the cybersecurity industry has met with the term: **MITRE ATT&CK**. What does it actually mean?
ATT&CK stands for adversarial tactics, techniques, and common knowledge. It is a commonly used framework that categorizes real-world adversary tactics, techniques, and procedures (TTPs)  based on observed behaviour in the wild. It is a big knowledge base maintaning by Mitre Corporation, a non-profit organization.

The framework provides a structured approach to understand and mitigate adverserial behaviour and cyber threats.

MITRE ATT&CK is widely used in across various cyber security fields such as threat intelligence analysis, adversary emulation, red teaming and security operations. It helps organizations strengthen their security posture and improve detection and response capabilities. Security solutions such as SIEM, SOAR, and XDR platforms apply the framework to provide greater visibility into the stage and progression of an intrusion.

---

#### Framework structure

The framework is organized into three domains:
- **Enterprise**: focuses on tradtional IT systems and cloud environments.
- **Mobile**: covers threats targetin mobile devices.
- **ICS**: addresses threats targetin industrial control systems.

Each domains consists of tactics, techniques, sub-techniques and procedures.

**Tactics**

Tactics represent the "why" of an ATT&CK technique or sub-technique. They describe the adversary’s tactical objective — the reason for performing a specific action. Each tactic has a unique ID.
One example of a tactic is Reconnaissance (TA0043).

**Techniques**

Techniques describe 'how' an adversary achieves a tactical goal by performing an action. Each technique also has a unique ID.
An example within the Reconnaissance tactic is Active Scanning (T1595).

**Sub-techniques**

Sub-techniques provide more detail within a technique. For example, within the Active Scanning technique, one sub-technique is Vulnerability Scanning (T1595.002).

**Procedures**

Procedures refer to the real-world implementation of techniques and sub-techniques as observed in actual cyber incidents. They describe how a specific threat actor executes a technique in practice.



### Final thoughts

MITRE ATT&CK focuses on adversary behavior instead of chasing low-level indicators such as hashes, IP addresses, or domain names that can be outdated within hours. 
Collecting and analyzing TTPs provides a significant advantage for defenders. It is costly and complex for attackers to change their fundamental methods, while organizations can continuously improve detection and response by applying this knowledge.

This makes the MITRE ATT&CK framework a practical, valuable, and essential tool for cybersecurity professionals.




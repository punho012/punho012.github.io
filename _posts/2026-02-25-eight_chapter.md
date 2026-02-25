---
title: Phile 8. Cyber Kill Chain
date: 2026-02-18 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

### Phile 8. Cyber Kill Chain

Cyber Kill Chain is a cybersecurity framework developed by Lockheed Martin in 2011. It is based on the military concept called Kill Chain. The framework consists of 7 stages. Each stage describes a step of a cyber attack.

**Stage I: Reconaissance**
In the first step the attackers search for information about the potential victim such as harvesting email addresses or conducting a port scan. The main goal of an actor collecting as much information as they can. It increases the likelihood of a successful attack.

**Stage II: Weaponization**
During the weaponization the attacker creates the malicious vector such as a ransomware or remote access trojan.

**Stage III: Delivery**
In this stage the attackers deliver the weapinzed bundle. They can achieve it via a vulnerable public-facing application or social engineering.

**Stage IV. Exploitation**
During the exploitation phase the malicios code is executed in the victim's environment.

**Stage V. Installation**
After the exploitation malware or other attack vector will be installed on the victim’s system.

**Stage VI: Command-and-Control**
After the adversaries successfully gained access to a large number of assets within the victim's system, their goal to set up a c2c channel they can control their malware or access the system remotely.

**Stage VII: Actions on Objective**
At this point the attackers carry out their main objective such as data encryption, data exfiltration or data destruction.

#### Concerns

One of the biggest crisism of the framework is its limitations. In focuses mainly on perimeter security and malware-related attacks. The framework misses to detect other attack vectors such as insider threats or DDOS.

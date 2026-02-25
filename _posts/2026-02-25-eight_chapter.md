---
title: Phile 8. Cyber Kill Chain
date: 2026-02-25 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

### Phile 8. Cyber Kill Chain

Cyber Kill Chain is a cybersecurity framework developed by Lockheed Martin in 2011. It is based on the military concept known as the Kill Chain. The framework consists of seven stages, each representing a step in a cyber attack lifecycle.

**Stage I: Reconaissance**
In the first step the attackers gather information about the potential victim, such as harvesting email addresses or conducting port scans. The main goal is to collect as much intelligence as possible to increase the likelihood of a successful attack.

**Stage II: Weaponization**
During the weaponization phase the attacker creates the malicious payload such as ransomware or a remote access trojan.

**Stage III: Delivery**
In this stage the attackers deliver the weapinzed payload to the victim. This can be achieved through vulnerable public-facing application or social engineering.

**Stage IV. Exploitation**
During the exploitation phase the malicios code is executed within the victim's environment. This often involves exploiting a vulnerability in software, the operating system, or user behavior.

**Stage V. Installation**
After the exploitation malware or other attack tools are installed on the victim’s system.

**Stage VI: Command-and-Control**
Once access is established, the adversary sets up a command-and-control (C2) channel. Through this communication channel, the attacker can remotely control the compromised system, issue commands, and move laterally within the environment.

**Stage VII: Actions on Objective**
At this stage, the attacker carries out their primary objective. This may include data exfiltration, data encryption (ransomware), data destruction, espionage, or disruption of services.

#### Benefits

Understanding the Cyber Kill Chain helps security professionals detect and respond to threats more effectively. It provides a structured way to analyze incidents and identify where defensive controls may have failed. The model also serves as a useful educational tool to explain attack progression to employees and management.

#### Concerns

Although the framework has significant value, it also has limitations. One of the main criticisms is that it focuses heavily on perimeter-based defenses and malware-driven attacks. It does not fully address other attack vectors such as insider threats, credential abuse, or distributed denial-of-service (DDoS) attacks. Additionally, modern threat actors often operate in more complex and less linear ways than the model suggests.

#### Final Takeaway

The Cyber Kill Chain provides a clear and structured way to understand how cyber attacks unfold step by step. While modern threats are often more complex and less linear, the model remains a valuable foundation for improving detection, response, and defensive strategy. Knowing where you are in the chain can make the difference between stopping an intrusion early and responding to a full-scale compromise.

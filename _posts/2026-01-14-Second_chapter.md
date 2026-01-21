---
title: Chapter 2. A Practical Breakdown of Threat Intelligence Types
date: 2026-01-14 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

### The 4 Types of Threat Intelligence

Threat intelligence is often talked about as if it were a single thing, but in practice, it comes in different forms and serves different purposes. Not all intelligence answers the same questions, and not all intelligence is useful to the same audience. Understanding the different types of threat intelligence helps ensure that the right information reaches the right people at the right time. Without this distinction, even high-quality intelligence can miss its mark. In this chapter, we’ll break down the main types of threat intelligence and how they’re actually used.

1. **Technical**
    - IP addresses  
	- File hashes  
	- Malicious domains  
	- URLs  
	- Email headers  
	- Registry keys  

	These are the kinds of indicators you’d find in an IOC feed or blocklist — and they’re often easy to automate into your defenses. 
	
	**Strength:** Fast, easy to deploy in tools like EDRs, SIEMs, or firewalls.  
	**Weakness:** Short lifespan. An IP address that’s malicious today might be clean tomorrow.
	
	**Use Cases:**
	
	- Blocking known malicious domains  
	- Alerting on known malware hashes
	- Feeding data into threat-hunting tools

2. **Tactical**

	Information about how attackers operate — their tools, techniques, and procedures (TTPs). This is what maps directly into frameworks like **MITRE ATT&CK**. Tactical intel connects the “what” to the “how.”
	
    - How an attacker gains access (e.g., spear phishing with macro-laced Word docs)  
	- How they move laterally (e.g., using PsExec)  
	- How they persist (e.g., registry autoruns)  
	- How they avoid detection (e.g., living off the land)
	
	**Strength:** Helps defenders build better detections.  
	**Weakness:** Doesn’t give immediate indicators — it’s about behavior.
	
	**Use Cases**
	- Writing SIEM rules  
	- Building behavior-based detections  
	- Adversary emulation by red teams
	
3. **Operational**

    Intel about specific, ongoing attacks or adversary infrastructure — often real-time or near real-time. This is the kind of intel you’d get from underground forums, malware sandboxes, or Telegram channels used by attackers, often before it becomes public. 
    It answers:
    - Who is being targeted right now?  
	- Are there phishing sites actively impersonating the company?
	- Are employee credentials currently being offered for sale on dark web forums?
	- Is the company’s logo or brand being actively impersonated?
	
	**Strength:** Can provide early warning before an attack hits.  
	**Weakness:** Fragile — infrastructure and tactics can change rapidly.

	**Use Cases**
	- Early detection  
	- Preventing attacks before they fully deploy  
	- Short-term alerting and monitoring

4. **Strategic**

High-level analysis meant to inform long-term security planning and decision-making. This type of intel is consumed by CISOs, executives, policy-makers, and threat analysts.

It focuses on:
- Motives of threat actors  
- Targeting trends across sectors or geographies  
- Risk forecasting  
- National-level threat behavior

**Strength:** Provides long-term value, helps shape security strategies.  
**Weakness:** May lack technical details and isn’t immediately actionable.

**Use Cases**
- Budget and resource allocation  
- Business risk assessments  
- Security policy decisions

---


**Summary Table**

| **Type**    | **Focus**                      | **Audience**          | **Lifespan** | **Example Use** |
| ----------- | ------------------------------ | --------------------- | ------------ | --------------- |
| Technical   | Raw indicators (IPs, hashes)   | SOC, EDR, SIEM        | Hours–Days   | IOC blocking    |
| Tactical    | TTPs and behavior patterns     | Blue teams, red teams | Weeks–Months | Detection logic |
| Operational | Campaign-specific activity     | IR teams, hunters     | Days–Weeks   | Rapid response  |
| Strategic   | Long-term trends & motivations | CISOs, execs          | Months–Years | Risk planning   |
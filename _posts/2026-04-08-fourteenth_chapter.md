---
title: Phile 14. Insider threats
date: 2026-04-08 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

## Phile 14: Insider threats

Today's topic is an underrated but an extremely dangerous threat type: insiders.

Insider is any person who has or had  authorized access to or knowledge of an organization’s resources, including personnel, facilities, information, equipment, networks, and systems. It includes employees, organization members, contractors, vendors or any person to whom the organization has supplied a computer and/or network access.

Insider threat is the potential for an insider to use their authorized access or understanding of an organization to harm that organization.

Insider threat definition according to CISA:

"Insider threat as the threat that an insider will use their authorized access, intentionally or unintentionally, to do harm to the department’s mission, resources, personnel, facilities, information, equipment, networks, or systems."

---

### Types of Insider Threats
#### Unintentinal threat
**Negligence:** 

- When an insider has the knowledge of applied policies and rules but choose to ignore them. 
- Usage of compromised personal accounts (email, social media) on work devices.

**Accidental:** 

When an insider cause unintended risk to the organization. Examples including sending sensitive information to a third-party or clicking on a malicious link on a phising email. It can happen because of the lack of proper security awareness and education in the organization.

#### Intentional Threats
When an insider cause intended harm for their personal benefit to the organization. The motivations can be diverse: 
- Unsatisfied, underpaid employees
- Financial gain
- Vendetta

#### Hybrid threat
In reality it often occurs that threat actors hires internal stuff to conduct cyber operations within an organization. It can be cybercriminals or nation-state actors as well. There are several well-documented cases when russian and north-korean actors tries to hires staff in western countries and offer huge payout for meaningful information. It often happens in regions with active geopolitical conflicts. This tactic is especially relevant during elections when a party tries to access the opponents system to ruin them.

---

### Detections and mitigations

Detecting of internal threats is extremely difficult. Most security monitoring systems are designed to detect external threats. That is why security tools can often miss harmful insider activities becuase it appears legitimate many times. Preventing internal threat requires layered defense strategy that combines monitoring, access management, user behavior analysis.
Defenders need to implement both technical and behavioral controls that may indicate insider activity.

**Implement User and Entity Behavior Analytics (UEBA)**
UEBA platforms use baselines and statistical models to detect anomalies such as:
- Unusual login times or from unexpected geolocation
- Sudden access of large volumes of sensitive data
- Email account sending unusual volume of emails to external addresses
Modern SIEMs like Splunk, Microsoft Sentinel offer built-in UEBA modules that can correlate these events across users and systems.

**Enforce Strict Data Loss Prevention (DLP) Controls**
It is essential to implement DLP controls preventing insiders to leak data.
- Block or alert on uploads to personal drives
- Block or alert repeates acces to sensitive data without business needs
- Monitor data copied to USB or external devices
- Detect mass data access and export events

**Privileged access management**
Limit privileged access to only those who truly need it, and enforce strict policies around its use like enforcing multi-factor authentication (MFA), recording and auditing admin sessions and creating strong authorization rules.


Security is not only about logs. Personal and emotional factors are crucial as well. Management must pay attention to stress indicators among staff members and report any suspicious activity. These indicators are:
- Employees recently denied promotions
- Staff experiences strong financial stress
- Employee has a conflict with the management


### Takeaway
Understanding the signs of collusion between internal and external actors is a key part of modern threat detection. These are not isolated incidents they are part of an evolving threat model that requires a fusion of behavioral monitoring, technical visibility, and strategic analysis.





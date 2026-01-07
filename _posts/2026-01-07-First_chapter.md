---
title: Chapter 1. The foundations
date: 2026-01-07 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

I am starting a new blog series focusing on Cyber Threat Intelligence, operational security and privacy. My goal is to provide a general overview of these topics in 50 distinct chapters throghout 2026. A new chapter will be released every week on Wednesday. The first 25 chapters focus on CTI and the remaining 25 chapters are cover OPSEC and various privacy topics.
So, Let's get started.

---

## Part I. : The Analyst’s View: A Deep Dive into Cyber Threat Intelligence

### Chapter 1. The foundations

Let's start at the beginning: what is Cyber Threat Intelligence? There are plenty of defintions, different organizations and security vendors explain it in different ways. One of the most frequently cited definitions comes from Gartner:

> **"Threat intelligence is evidence-based knowledge, including context, mechanisms, indicators, implications and actionable advice, about an existing or emerging menace or hazard to assets that can be used to inform decisions regarding the subject's response to that menace or hazard."**

The exact definition also depens on perspective.

From my point of view - as a SOC Analyst - is collecting, processing and analyzing data related to existing and emerging threats targeting our organization.
Threat Intelligence helps mitigate and prevent cyber threats that may impact the business. More importantly, it enables us to shift from purely reactive detection to a more proactive security workflow.

---

#### What is the difference between threat data, threat information, and threat intelligence?

These terms are often used interchangeably, but they actually represent different levels of refinement:

- **Threat Data** → raw, unprocessed observations. For example: a single suspicious IP address or a file hash. On its own, it may not mean much.
- **Threat Information** → processed data with some context. For example: 'This IP address is associated with a phishing campaign targeting financial institutions.'
- **Threat Intelligence** → fully analyzed and contextualized information that is **actionable**. For example: 'Based on recent campaigns, this IP is linked to APT29. They are currently targeting government agencies in Europe, and the TTPs suggest they may attempt credential theft. We recommend blocking the IP and monitoring for related lateral movement techniques.'

In short, the progression is from raw → contextualized → actionable, and that final step is what makes threat intelligence useful for decision-making.

---

CTI is not just about collecting IOCs - it is much more than that. It is investigation, research, and understanding adversaries. Without these components we are just collecting data - we are not doing real CTI.

Every small datasets can play a crucial role in the larger story. The analyst's job is to connect the dots and reveal the bigger picture. That requires curiosity, enthusiasm, analytical thinking, asking the right questions and a lot of hard work. It is a mindset.

It is not easy, but when you do it right, it is a real level up.

That’s enough for today. Next week, I’ll continue with the **Threat Intelligence lifecycle**.

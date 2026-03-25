---
title: Phile 12. APT Names Don’t Matter: Why TTPs Tell the Real Story
date: 2026-03-25 +/-TTTT
categories: [Blog_series]
tags: [CTI] # TAG names should always be lowercase
---

### Phile 12.APT Names Don’t Matter: Why TTPs Tell the Real Story
Let’s take a closer look at APT groups and how they are named.

#### Quick refresher on APTs
APT stands for Advanced Persistent Threats. As we discussed earlier these groups are typically  state-backed with significant resources and access to advanced capabilities such as zer-day exploits. 
They operate on behlf of nation states and conduct cyber espionage as well as high-impact operations targeting government networks, defense contractors and critical infrastructures. Monitoring these groups are essential for cyber defenders because they pose serious and long-term risks.
Frameworks like Mitre Attack document the TTPs of htese threat actors. However, before analyzing behavior, analysts often encounter a more basic challenge: naming.

#### The naming problem
In reality, different security vendors use different naming conventions for the same threat group.
For example:
APT28 → Fancy Bear → Sofacy → STRONTIUM
These all refer to the same group. Microsoft calls them STRONTIUM, while CrowdStrike refers to them as Fancy Bear.

There are no univeral standard agreement for naming these groups. Each vendor and research organization sees only part of the activity and builds its own tracking and naming system.
Naming is also part of branding. Vendors often create unique names to distinguish their research and reporting from others.

This incosistency can be confusing for analysts especially for those who are new to CTI. However, the name itself is just a label. What matters are tactics, techniques and tools. These elements provide a reliable insight into how they operate and describe the behaviour of the threat actor.
Instead of focusing on names, CTI professionals should focus on patterns. Look at how the attacker behaves, what infrastructure they use and how their operations evolve. 

**Do not focus on the name - Focus om what is behind**

#### Final Takeaway

APT names can be confusing, inconsistent, and sometimes misleading. Different vendors may use different labels for the same group, but the underlying behavior remains the same.

For defenders, the real value lies in understanding TTPs, not memorizing names. If you focus on patterns instead of labels, you gain a much clearer and more reliable view of the threat landscape.







---
title: Wannacry analysis
date: 2025-05-23 +/-TTTT
categories: [Malware analysis]
tags: [malware]     # TAG names should always be lowercase
---

### Overview
The Wannacry ransomware appeared in 2017 and caused serious damage. By analysing the
code we can understand the mechanisms of its inner workings and how it spread. This helps us
understand why it was so effective. We can gain a deeper knowledge about cyberattacks and
how malware utilizes system vulnerabilities.

File name: lhdfrgui.exe
SHA256: 24d004a104d4d54034dbcffc2a4b19a11f39008a575aa614ea04703480b1022c

### Static analysis
#### File analysis using Virustotal
In the first step, I aimed to determine whether we are dealing with malicious code. The best tool for this initial assessment is VirusTotal. I uploaded the file’s hash value, and the results can be
seen in the screenshot below:

The result is quite clear: 69 out of 73 security vendors flagged the sample as malicious. The
most common detection label is "Trojan.WannaCry/Wanna". Several vendors also identified it
with labels such as "ransom" or "ransomware". Based on this information, it is reasonable to
suspect that the sample is a ransomware variant.
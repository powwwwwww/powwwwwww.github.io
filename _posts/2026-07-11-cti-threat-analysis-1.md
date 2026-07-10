---
layout: post
title: "CTI Example: Campaign X — Part 1"
date: 2026-07-11 09:00:00 +00:00
categories: [CTI]
tags: [malware, triage]
image: https://via.placeholder.com/800x400
description: Initial notes on a simulated malware campaign.
---

![campaign]({{ page.image }})

A brief analysis of Indicators of Compromise for Campaign X.

```python
# sample yara-like rule (illustrative)
rule suspicious_string {
    strings:
        $a = "suspicious_domain.com"
    condition:
        $a
}
```

---
layout: post
title: "CTI Example: Campaign X — Part 2"
date: 2026-07-10 12:00:00 +00:00
categories: [CTI]
tags: [ioc, analysis]
image: https://via.placeholder.com/800x400
description: Follow-up with yara and traffic analysis.
---

![traffic]({{ page.image }})

Network traffic snippets and host indicators.

```bash
# tcpdump example filter
tcpdump -n -r capture.pcap 'tcp and host 1.2.3.4'
```

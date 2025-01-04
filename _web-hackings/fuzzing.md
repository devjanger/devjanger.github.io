---
title: Fuzzing
author: janger
date: 2025-01-04
category: Web Hacking
layout: post
---

## FFUF

~~~ bash
ffuf -w /usr/share/wordlists/wfuzz/general/common.txt -u http://target.com/FUZZ
~~~

---
title: Fuzzing
author: janger
date: 2025-01-04
category: Web Hacking
layout: post
---

## FFUF path fuzzing

~~~ bash
ffuf -w /usr/share/wordlists/wfuzz/general/common.txt -u http://target.com/FUZZ -mc 200
~~~

## FUFF subdomain fuzzing

~~~ bash
ffuf -u http://target.com/ -w ./fuzzDicts/subdomainDicts/main.txt -H "Host:FUZZ.target.com" -mc 200
~~~

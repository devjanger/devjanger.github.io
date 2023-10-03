---
title: HTTP Request Splitting
author: janger
date: 2023-10-02
category: Web Hacking
layout: post
---

## HTTP Request Splitting이란?
공격자가 HTTP Header를 조작이 가능한 경우 Carriage Return (CR), Line Feed (LF)를 삽입해 새로운 HTTP Request를 발생시켜 외부에서 접근 불가능한 자원에 접근하거나 SSRF를 가능하게 하는 테크닉이다.  


## 전제 조건
1. HTTP agent가 HTTP/1.0 또는 HTTP/1.1 사용과 Keep Alive 옵션, Chunked 인코딩을 허용
2. 사용자가 HTTP 헤더 조작이 가능
3. 서로 동일한 네트워크의 사용자 응답을 처리하는 두 호스트(프론트엔드, 백엔드)가 있음
4. 프론트엔드와 백엔드가 HTTP request와 Header 구문을 서로 다르게 해석


## cheat sheet
~~~ 
/post?token=f4c4c6d0%0D%0AContent-Length: 1%0D%0A%0D%0AT%0D%0AGET /admin HTTP/1.1%0D%0AX-Forwarded-For: 127.0.0.1
~~~

## 참고

[https://capec.mitre.org/data/definitions/105.html](https://capec.mitre.org/data/definitions/105.html)

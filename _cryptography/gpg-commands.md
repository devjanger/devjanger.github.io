---
title: GPG(GNU Privacy Guard) Commands
author: janger
date: 2023-09-28
category: cryptography
layout: post
---

## Check the list of keys
~~~ bash
gpg --list-keys
~~~

## Check the key signature (KEY-ID)
~~~ bash
gpg --list-signatures
~~~

## Export public and private keys With --armor option
~~~ bash
gpg --armor --export KEY-ID > public.key
gpg --armor --export-secret-keys KEY-ID > private.key
~~~

## Delete a key (public, private)
~~~ bash
gpg --delete-keys KEY-ID
gpg --delete-secret-keys KEY-ID
~~~

## Import a key (public, private)
~~~ bash
gpg --import public.key
gpg --allow-secret-key-import --import private.key
~~~


## Encrypt a message
~~~ bash
gpg --armor --encrypt -r KEY-ID message.txt
echo "Hello World" | gpg --armor --encrypt -r KEY-ID > message.txt.asc
~~~


## Decrypt the message
~~~ bash
gpg --decrypt message.txt.asc
~~~

## Verify the fingerprint
~~~ bash
gpg --fingerprint KEY-ID
~~~


## Verify signature
~~~ bash
gpg --verify message.txt.asc message.txt
~~~

## Sign message
~~~ bash
gpg --armor --sign message.txt
~~~

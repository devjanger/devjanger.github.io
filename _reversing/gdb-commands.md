---
title: GDB(GNU Debugger) Commands
author: janger
date: 2023-09-25
category: reversing
layout: post
---


## start

~~~ bash
gdb-peda$ start
gdb-peda$ start arg
~~~


## next(next line)

~~~ bash
gdb-peda$ next
gdb-peda$ n
gdb-peda$ n 2
~~~

## step(into function)

~~~ bash
gdb-peda$ step
gdb-peda$ s
gdb-peda$ s 2
~~~

## continue(to next breakpoint)

~~~ bash
gdb-peda$ continue
gdb-peda$ c
~~~

## set breakpoint

~~~ bash
gdb-peda$ break
gdb-peda$ b
gdb-peda$ b *main
gdb-peda$ b *0x401306
~~~

## list breakpoint

~~~ bash
gdb-peda$ info breakpoints
~~~

## remove breakpoint

~~~ bash
gdb-peda$ delete
gdb-peda$ delete 11
gdb-peda$ del
~~~


# show information

~~~ bash
gdb-peda$ info functions
gdb-peda$ info main
gdb-peda$ context
~~~

# show sassemble code

~~~ bash
gdb-peda$ disassemble
gdb-peda$ disas
gdb-peda$ context code
~~~



# show memory

~~~ bash
gdb-peda$ x/1x $rip+0xcc9
~~~










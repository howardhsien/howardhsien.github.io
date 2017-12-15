---
layout:post
title:Bit size of 64bits - OS system
---
Type           ILP64   LP64   LLP64
char              8      8       8
short            16     16      16
int              64     32      32
long             64     64      32
long long        64     64      64
pointer          64     64      64

most unix system uses LP64 (long & pointer are 64bits)
microsoft system uses LLP64 (long long & pointer are 64bits)

---
layout: post
title: 'Warning: gulp version mismatch Fix'
published: true
---

```bash
$ bower install
```
```bash
$ gulp update
[10:31:22] Warning: gulp version mismatch:
[10:31:22] Global gulp is 3.9.0
[10:31:22] Local gulp is 3.8.11
```
```bash
$ gulp -v
[10:39:05] CLI version 3.9.0
[10:39:05] Local version 3.8.11
```
```bash
$ npm install gulp@3.9.0 --save
```
